## Survey exit redirects

When a panelist has completed a survey, you will send panelists back to these links with the survey outcome or status code. If your survey solution supports **exit link hashing**, you should always use it to prevent tampering with exit links.

**Sample Ninja** supports a total of 6 different survey outcomes:

- Complete (Panelist has completed the survey)
- Profile (Panelist was terminated in screening questions)
- Quota (Panelist was terminated because a quota bucket was full)
- Non actionable (Panelist was returned back to SampleNinja because no action was taken)
- Quality (Survey software has detected straight-lining or other quality issues)
- Duplicate (Survey software has detected this panelist as a duplicate participant)
- Security (Hash validation failed or some other security mechanism triggered)

The **security** -status should be used if the hash validation fails (See below **Signing and security** section for more details). 

The **duplicate** status is intended to be used if the survey software detects that the panelist is a duplicate i.e., using fingerprints or other techniques. 

The **quality** status should be used when a panelist is straight-lining and otherwise doesn't pay attention to the survey questions.

The **Non actionable** status can be used in some special cases. For example, if you utilize a router, fail to find any opportunities for your panelist.

### Return status parameters

**Sample Ninja** supports multiple return statuses
- c (completed)
- p (profile)
- q (quota)
- na (non actionable)
- s (security)
- dup (duplicate)
- qua (quality)

Example of returning complete back along with the panelist ID
```
https://sampleninja.app/p/exit?s=c&session=d4454aa4-4690-4a8a-bc51-66d30072a87f
```

> **IMPORTANT:** Always use the correct status as these statuses are used to calculate panelist's **Quality Score**

## Session ID Redirects

The session parameter is required when “session param name” is defined (default), and it has to be passed back in “session” -parameter (fixed parameter name on exit, configurable when sending into surveys).

## Signing and security
Signing should always be used when redirecting panelists to **Sample Ninja** exit links. The following algorithms are supported:

The Full URL hashing algorithms: (Recommended)

- SHA256 Full URL (recommended)
- SHA1 Full URL (recommended)
- MD5 Full URL (weak security)

Legacy algorithms: (Not recommended, challenging to program)

- SHA256 Legacy
- SHA1 Legacy 
- MD5 Legacy (weak security)

> The Legacy hash algorithms use URL path + params, while the Full URL hashing uses the entire URL, including protocol and hostname. In addition, the Full URL hashing is easier to implement as no parameter sorting is required.

> **IMPORTANT:** You must configure exit links with selected algorithm + secret in the **Sample Ninja UI -> Edit Project -> Survey Links -> Exit links** otherwise the hash value supplied **WILL NOT BE VALIDATED**!!! 

### Hash Calculator
Use the **Hash Calculator** tool below while testing. Replace your installations domain (customer.panelservice.io) with your own or access the tool by clicking your Avatar and then selecting Hash Calculator. 

https://customer.panelservice.io/hash-calculator

> You do not have to authenticate to use the **Hash Calculator**; therefore, you can easily share the **Hash Calculator** web address with the developers and survey programmers.

### Example A (SHA-1 Full URL or SHA-256 Full URL)

Choose one of these methods if adding hashing the first time. These are by far the simplest to implement while being secure.

Returning to **SampleNinja** as completed

```
https://yourcompany.panelservice.io/p/exit?s=c&session=9bb379a3-7831-4a55-8036-085aeff18790
```
#### Step 1
Append the secret to the end of the URL

```
https://yourcompany.panelservice.io/p/exit?s=c&session=9bb379a3-7831-4a55-8036-085aeff18790MySecretPasscode
```

#### Step 2
Calculate the hash (PHP Example)

```
// SHA1
echo hash('SHA1','https://yourcompany.panelservice.io/p/exit?s=c&session=9bb379a3-7831-4a55-8036-085aeff18790MySecretPasscode');

821583aed0d889bb37ec2995fb6b18837f254650

// SHA 256
echo hash('SHA256','https://yourcompany.panelservice.io/p/exit?s=c&session=9bb379a3-7831-4a55-8036-085aeff18790MySecretPasscode');

7c8c681ec01dfcc4b8c99849417832c242c8bf18ae0891a1e780d3385eba4821
```

Calculate the hash (JavaScript running in a browser)
```
// SHA 256
async function hash(string) {
  const utf8 = new TextEncoder().encode(string);
  const hashBuffer = await crypto.subtle.digest('SHA-256', utf8);
  const hashArray = Array.from(new Uint8Array(hashBuffer));
  return hashArray
    .map((bytes) => bytes.toString(16).padStart(2, '0'))
    .join('');
}

hash('https://yourcompany.panelservice.io/p/exit?s=c&session=9bb379a3-7831-4a55-8036-085aeff18790MySecretPasscode).then((hex) => console.log(hex));

7c8c681ec01dfcc4b8c99849417832c242c8bf18ae0891a1e780d3385eba4821

```

#### Step 3
Append the calculated hash to the end of the URL

```
// SHA1
https://yourcompany.panelservice.io/p/exit?s=c&session=9bb379a3-7831-4a55-8036-085aeff18790&hash=821583aed0d889bb37ec2995fb6b18837f254650

// SHA256
https://yourcompany.panelservice.io/p/exit?s=c&session=9bb379a3-7831-4a55-8036-085aeff18790&hash=7c8c681ec01dfcc4b8c99849417832c242c8bf18ae0891a1e780d3385eba4821
```

### Example B (SHA-1 Legacy and SHA-256 Legacy, Not recommended)

Returning to **SampleNinja** as completed

```
https://yourcompany.panelservice.io/p/exit?s=c&session=9bb379a3-7831-4a55-8036-085aeff18790
```

#### Step 1 - Remove protocol and host
```
/p/exit?s=c&session=9bb379a3-7831-4a55-8036-085aeff18790
```
#### Step 2 - Sort URL params alphabetically
```
/p/exit?session=9bb379a3-7831-4a55-8036-085aeff18790&s=c
```
#### Step 3 - Append secret
```
/p/exit?session=9bb379a3-7831-4a55-8036-085aeff18790&s=cMySecretPasscode
```
#### Step 4 - Calculate the hash
When using SHA-1
```
echo hash('SHA1','/p/exit?session=9bb379a3-7831-4a55-8036-085aeff18790&s=cMySecretPasscode'); // PHP example

5b0cc76a56f0ee660dcf72ecca4706bec1981c10
```

When using SHA-256
```
echo hash('SHA256','/p/exit?session=9bb379a3-7831-4a55-8036-085aeff18790&s=cMySecretPasscode'); // PHP example

bbc0ce056845647071b3a5aa82a478ac65885ba81c2671f01482fb5e5df3c011
```

#### Step 5 - Append hash to the exit link

Example result using **SHA-1** algorithm with secret **MySecretPasscode**
```
https://yourcompany.panelservice.io/p/exit?session=9bb379a3-7831-4a55-8036-085aeff18790&s=c&hash=5b0cc76a56f0ee660dcf72ecca4706bec1981c10
```

Example result using **SHA-256** algorithm with secret **MySecretPasscode**.
```
https://yourcompany.panelservice.io/p/exit?session=9bb379a3-7831-4a55-8036-085aeff18790&s=c&hash=bbc0ce056845647071b3a5aa82a478ac65885ba81c2671f01482fb5e5df3c011
```

### Python example:
The following Python example is Decipher compatible. You cannot enter & in Decipher as it will be rejected when you submit your code. The following example illustrates how to go around this validation issue:

```
import hashlib 

AMPERSAND = chr(38)
SECRET = "OmLXcVR"

#----------------------------------
# Minimal example
#----------------------------------

url = "/p/exit?s=c"
urlWithSecret = "/p/exit?s=c" + SECRET
hash = hashlib.sha256(urlWithSecret.encode()).hexdigest()

print("\nMinimal example\n")
print("Original with params sorted alphabetically:\n" + url + "\n");
print("Url with secret hashed:\n" + urlWithSecret + "\n")
print("Redirect with hash:\n" + url + AMPERSAND + "hash=" + hash + "\n");

#--------------------------------------------------------
# Example with panelist ID
# IMPORTANT: Param names must be in alphabetical order
#--------------------------------------------------------
panelistId = "48dc5f0c-e453-4c40-9952-8204bdedfc61"

url = "/p/exit?id=" + panelistId + AMPERSAND + "s=c"
urlWithSecret = "/p/exit?id=" + panelistId + AMPERSAND + "s=c" + SECRET
hash = hashlib.sha256(urlWithSecret.encode()).hexdigest()

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

