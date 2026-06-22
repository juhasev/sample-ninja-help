# Newsletter Communication Content - Basic Settings

## Overview
The Basic settings section allows you to configure the fundamental properties of your newsletter communication content.

## How to Use

1. **Select Template**: Choose an appropriate template from the Template dropdown that matches your newsletter design requirements
2. **Set Locale**: Select the correct locale to ensure proper language and formatting for your target audience
3. **Enter Subject**: Write a clear, compelling subject line that will encourage recipients to open your newsletter
4. **Add Preheader**: Include preview text that works together with your subject line to provide context and encourage engagement

## Content

The advanced editor provides a comprehensive visual interface for creating professional newsletter content. Here's how to use it effectively:

The editor workspace is divided into three main areas:
- **Left panel**: Contains template settings, subject line, and language options
- **Center area**: Shows a live preview of your newsletter as you build it
- **Right panel**: Provides design elements and layout components you can add

### Building Your Newsletter Layout

1. **Choose a Layout Structure**:
   - Select from 1, 2, or 3-column layouts depending on your content needs
   - Drag your chosen layout from the right panel into the center preview area
   - Multiple layouts can be combined for complex newsletter designs

2. **Add Content Elements**:
   - **Text**: For articles, announcements, and written content
   - **Image**: Add photos, graphics, or visual elements
   - **Button**: Create call-to-action buttons for links and engagement
   - **Social**: Add social media icons and links
   - **Divider**: Separate sections visually
   - **Spacer**: Control spacing between elements

### Content Editing

- **Text Editing**: Click directly on any text element to edit content inline
- **Personalization**: Use data variables in square brackets like `[FIRST_NAME]` and `[LAST_NAME]` to personalize content
- **Links**: Add links through the editor's built-in controls and pick from ready-made URL presets (such as the unsubscribe and privacy policy pages) - see **Adding Links** below

### Adding Links (opt-out, privacy policy, and more)

The newsletter uses the same link controls as the invitation and reminder email editor. The key thing to know is that the unsubscribe and policy links are **presets**: you pick them from a dropdown and the system fills in the correct, up-to-date address automatically. You should **not** paste a personal opt-out link by hand (see the note below).

There are two ways to add a link, depending on whether you want a text link or a button.

**To turn text into a link**

1. Click into a **Text** block and select the words you want to link (for example "Unsubscribe" or "Privacy policy")
2. Click the **Link** tool in the small pop-up toolbar that appears above the block
3. In the link settings on the right, either:
   - **Href**: type a full web address (for example `https://example.com`), or
   - **URLs**: pick a ready-made destination from the dropdown

**To link a button**

A button is itself the link, so you set where it goes from the **Component settings** panel on the right, not by adding a link inside the button text.

1. Click the button to select it (double-clicking it opens its settings automatically)
2. In **Component settings**, choose one of:
   - **Href**: type a web address, or
   - **URLs**: pick a ready-made destination from the dropdown

**The ready-made URL presets**

The **URLs** dropdown offers these presets. Each one is replaced with the correct address when the newsletter is sent:

- `[unsubscribe_url]` - the recipient's personal unsubscribe (opt-out) link
- `[community_url]` - your community page
- `[faq_url]` - your FAQ page
- `[terms_and_conditions_url]` - your terms and conditions page
- `[privacy_policy_url]` - your privacy policy page
- `[cookie_policy_url]` - your cookie policy page
- `[extra_policy_url]` - your extra (for example GDPR or CCPA) policy page

> **Important - don't paste a personal opt-out link.** A single opt-out link contains one panelist's unique ID and signature, so if you paste it into the template every recipient gets *that one person's* link. Always use the `[unsubscribe_url]` preset instead - the system generates the correct personal link for each recipient automatically.

> **Where the privacy policy link points.** The `[privacy_policy_url]` preset uses the Privacy Policy URL configured for your subpanel (in its **Policy URLs** settings), and falls back to the built-in privacy page when no custom one is set. So you don't need to paste the address into the newsletter: set it once in Policy URLs and the preset stays correct everywhere it is used.

### Preview and Testing

- **Device Preview**: Use the toolbar buttons to preview your newsletter on desktop, tablet, and mobile devices
- **Test Email**: Click "EMAIL TO ME" to send a test version to yourself before publishing
- **Visual Components**: Toggle component boundaries to see your newsletter structure clearly

### Design Controls

- **Style Manager**: Access color schemes, fonts, and spacing options
- **Toolbar Features**: Use undo/redo, fullscreen mode, and settings for advanced customization
- **Responsive Design**: The editor automatically ensures your newsletter looks good across all devices

### Matching Your Brand Colors and Fonts

The newsletter editor works differently from the invitation and reminder email template editor. Those templates have a single **Colors** panel that restyles the whole template at once. The newsletter is built in the drag-and-drop editor, so colors and fonts are set **per element** through the **Style Manager** rather than from one global panel. There is no single "apply my colors everywhere" button — you style each block to match your branding.

To make your newsletter match your panel's look:

1. Click the element you want to restyle (a text block, button, or section)
2. Click **Open Style Manager** on the right
3. Under **Typography**, set the **Font color**, **Font**, and **Font size**
   - For a **button**, also set its **background color** and **text color**
   - For a **section** or the **page background**, select that area and set its **background color**
4. Repeat for each element until everything matches

> **Tip:** To match your branding exactly, open one of your existing branded email templates, note the color codes you used there (for example `#1A2B3C`), and enter those same codes in the newsletter's Style Manager. This guarantees the newsletter and your other emails look identical.

### Best Practices for Newsletter Content

- Keep your design consistent with your brand colors and fonts
- Ensure good contrast between text and background colors
- Use clear headings to organize content sections
- Include compelling call-to-action buttons
- Test thoroughly before sending to your audience

## Best Practices

- **Subject Line**: Keep it under 50 characters for optimal display across email clients
- **Preheader**: Use 35-90 characters to ensure it displays properly in most email clients
- **Locale**: Match the locale to your content language and target geographic region
- **Template**: Choose a template that aligns with your brand and content structure