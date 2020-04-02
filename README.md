# html-email-template
A common use responsive HTML email template

## Note
* `email-boilerplate.html` is an adapted version based on `email-origin.html` from [Cerberus](https://github.com/TedGoas/Cerberus/edit/master/cerberus-hybrid.html)

## Inline your CSS before sending
Email is notorious for inconsistent CSS support. Therefore you should always inline your CSS before sending.

### Sending emails directly from your codebase or using a developer service?
For an API service (like Mailgun, SendGrid, Postmark) **you need to inline the CSS before sending**. See `email-inlined.html` for an example.
You can use this [Email CSS Inliner](https://htmlemail.io/inline/) or a module like [Juice](https://github.com/Automattic/juice) to do this automatically.

* Copy all of email.html
* Paste the HTML as the source into the inliner
* Copy the HTML output and use this as the email template you send

### Sending emails using a marketing service like Mailchimp?
Use the template `email-boilerplate.html` as is. They'll put the CSS inline for you when you put together your campaign.

## Images in email
When inserting images remember to include the following attributes or risk them breaking in different clients:

* `src`
* `alt`
* `width`
* `height`
* `border`

Example:
`<img src="https://absolute-path-to-image.jpg" alt="Useful alt text" width="500" height="300" border="0" style="border:0; outline:none; text-decoration:none; display:block;">`
[More information here](https://www.smashingmagazine.com/2017/01/introduction-building-sending-html-email-for-web-developers/)
