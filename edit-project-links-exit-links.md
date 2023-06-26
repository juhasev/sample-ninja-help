## Survey exit redirects

When panelist has completed a survey you will send panelists back to these link with the survey outcome or status code. If you survey solution supports **exit link hashing** you should always use it to prevent tampering with the exit links.

**Sample Ninja** support total of 6 different survey outcomes:

- Complete (Panelist has completed the survey)
- Profile (Panelist was terminated in screening questions)
- Quota (Panelist was terminated because a quota bucket was full)
- Quality (Survey software has detected straightlining or other quality issues)
- Duplicate (Survey software has detected this panelist as a duplicate participant)
- Security (Hash validation failed or some other security mechanism triggered)

The **security** -status should be used if the hash validation fails (See below **Signing and security** section for more details). 

The **duplicate** status is intended to be used if the survey software detects that the panelist is duplicate i.e. using fingerprints or other techniques. 

The **quality** status should be used when panelist straight lines and otherwise don't pay attention to the survey questions.

### Return status parameters

**Sample Ninja** supports multiple return statuses
- c (completed)
- q (quota)
- p (profile)
- s (security)
- dup (duplicate)
- qua (quality)

Example of returning complete back along with the panelist ID
```
https://sampleninja.app/p/exit?s=c&pid=d4454aa4-4690-4a8a-bc51-66d30072a87f
```

> **IMPORTANT:** Always use the correct status as these statuses are used to calculate panelist's **Quality Score**

## Signing and security
Signing should always be used when returning panelist back to **Sample Ninja** exit links. The following algoritms are supported:

- MD5 (not recommended)
- SHA1 
- SHA256 (recommended)

> **IMPORTANT:** You must configure exit links with selected algorithm + secret in the **Sample Ninja UI -> Edit Project -> Survey Links -> Exit links** otherwise the hash value supplied **WILL NOT BE VALIDATED**!!! 

### Example survey exit redirects (back to SampleNinja)
To make the exit redirect and the resulting hash more complex, we recommend you add some additional parameter that is random to the exit redirect links. The only reserved parameters are "s" for status and "session" for session ID.

In this example we are using **SHA-1** and ***SHA-256** algorithms with secret **MySecretPasscode** to compute hash parameter.

Returning back to **SampleNinja** as completed

```
https://yourcompany.panelservice.io/p/exit?s=c&id=9bb379a3-7831-4a55-8036-085aeff18790
```

#### Step 1 - Remove protocol and host
```
/p/exit?s=c&id=9bb379a3-7831-4a55-8036-085aeff18790
```
#### Step 2 - Sort URL params alphabetically
```
/p/exit?id=9bb379a3-7831-4a55-8036-085aeff18790&s=c
```
#### Step 3 - Append secret
```
/p/exit?id=9bb379a3-7831-4a55-8036-085aeff18790&s=cMySecretPasscode
```
#### Step 4 - Calculate hash
When using SHA-1
```
echo hash('SHA1','/p/exit?id=9bb379a3-7831-4a55-8036-085aeff18790&s=cMySecretPasscode'); // PHP example

17637eac2a8bbd056bb31b19a31768846474b5fa
```

When using SHA-256
```
echo hash('SHA256','/p/exit?id=9bb379a3-7831-4a55-8036-085aeff18790&s=cMySecretPasscode'); // PHP example

f9c2db85f0d4644b4f8e187bea2bd2c62d4aa216af5f42c4c4a4b9b153bc1bd0
```

#### Step 5 - Append hash to the exit link

Example result using **SHA-1** algorithm with secret **MySecretPasscode**
```
https://yourcompany.panelservice.io/p/exit?id=9bb379a3-7831-4a55-8036-085aeff18790&s=c&hash=17637eac2a8bbd056bb31b19a31768846474b5fa
```

Example result using **SHA-256** algorithm with secret **MySecretPasscode**.
```
https://yourcompany.panelservice.io/p/exit?id=9bb379a3-7831-4a55-8036-085aeff18790&s=c&hash=f9c2db85f0d4644b4f8e187bea2bd2c62d4aa216af5f42c4c4a4b9b153bc1bd0
```

### Python example:
The following Python example is Decipher compatible. You cannot enter & in Decipher as will be rejected when you submit your code. The following example illustrated how go around this validation issue:

```
import hashlib 

AMPERSAND = chr(38)

#----------------------------------
# Minimal example
# Produces correct hash
#----------------------------------
secret = "OmLXcVR"

url = "/p/exit?s=c"
urlWithSecret = "/p/exit?s=c" + secret
encoded = url.encode()
hash = hashlib.sha256(encoded).hexdigest()

print("\nMinimal example\n")
print("Original with params sorted alphabetically:\n" + url + "\n");
print("Url with secret hashed:\n" + urlWithSecret + "\n")
print("Redirect with hash:\n" + url + AMPERSAND + "hash=" + hash + "\n");

#----------------------------------
# Skate around amp; issue
# Produces correct hash
#----------------------------------
secret = "OmLXcVR"
panelistId = "48dc5f0c-e453-4c40-9952-8204bdedfc61"

url = "/p/exit?id=" + panelistId + AMPERSAND + "s=c"
urlWithSecret = "/p/exit?id=" + panelistId + AMPERSAND + "s=c" + secret
encoded = urlWithSecret.encode()
hash = hashlib.sha256(encoded).hexdigest()

print("\nWith panelist ID example\n")
print("Original with params sorted alphabetically:\n" + url + "\n");
print("Url with secret hashed:\n" + urlWithSecret + "\n")
print("Redirect with hash:\n" + url + AMPERSAND + "hash=" + hash + "\n");
```
The following will output:

```
Minimal example

Original with params sorted alphabetically:
/p/exit?s=c

Url with secret hashed:
/p/exit?s=cOmLXcVR

Redirect with hash:
/p/exit?s=c&hash=70066f17bfa9d3bfa3346e15694c30d0735ba6b6fcc45bc31957031f150d83f8

With panelist ID example

Original with params sorted alphabetically:
/p/exit?id=48dc5f0c-e453-4c40-9952-8204bdedfc61&s=c

Url with secret hashed:
/p/exit?id=48dc5f0c-e453-4c40-9952-8204bdedfc61&s=cOmLXcVR

Redirect with hash:
/p/exit?id=48dc5f0c-e453-4c40-9952-8204bdedfc61&s=c&hash=e644fb896d823392ececa7158ee6c8b8b4e28b8a772de6dad6adf9730934b534
```

