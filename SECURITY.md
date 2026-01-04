# Security Policy

## Reporting a Vulnerability

The NovelPaper team takes security seriously. We appreciate your efforts to responsibly disclose your findings.

### How to Report a Security Vulnerability

**Please do NOT report security vulnerabilities through public GitHub issues.**

Instead, please report them through one of the following methods:

1. **GitHub Security Advisories** (Preferred)
   * Go to the [Security tab](https://github.com/Hostilian/novelpaper/security)
   * Click "Report a vulnerability"
   * Fill out the form with details

2. **Email**
   * Contact the maintainers directly
   * Provide a detailed description of the vulnerability
   * Include steps to reproduce if possible

### What to Include

When reporting a vulnerability, please include:

* **Type of vulnerability** (e.g., XSS, injection, authentication issue)
* **Location** (file path, URL, or affected component)
* **Step-by-step instructions** to reproduce the issue
* **Potential impact** of the vulnerability
* **Suggested fix** (if you have one)
* **Your contact information** for follow-up questions

### What to Expect

* **Acknowledgment**: We'll acknowledge your report within 48 hours
* **Updates**: We'll keep you informed about the progress
* **Resolution**: We'll work to patch the vulnerability promptly
* **Credit**: With your permission, we'll acknowledge your contribution

### Safe Harbor

We support safe harbor for security researchers who:

* Make a good faith effort to avoid privacy violations and service disruption
* Only interact with accounts you own or with explicit permission
* Do not exploit a security issue beyond what is necessary to demonstrate it
* Report vulnerabilities promptly
* Keep vulnerability details confidential until we've had a chance to address them

## Supported Versions

| Version | Supported          |
| ------- | ------------------ |
| Latest  | :white_check_mark: |
| Older   | :x:                |

## Security Best Practices

For users deploying NovelPaper:

### When Deploying

* **Use HTTPS**: Always serve the website over HTTPS
* **Content Security Policy**: Implement CSP headers
* **Update Dependencies**: Keep any dependencies up to date
* **Secure Headers**: Use security headers (X-Frame-Options, X-Content-Type-Options, etc.)

### For Contributors

* **No Secrets**: Never commit secrets, API keys, or credentials
* **Sanitize Inputs**: Always validate and sanitize user inputs
* **Review Dependencies**: Check dependencies for known vulnerabilities
* **Follow Best Practices**: Use secure coding practices

## Known Security Considerations

### Client-Side Form

The contact form in NovelPaper is client-side only. When implementing a backend:

* **Validate all inputs server-side**
* **Implement rate limiting** to prevent abuse
* **Use CAPTCHA** to prevent spam
* **Sanitize data** before processing
* **Use HTTPS** for form submissions

### Static Website

NovelPaper is a static website with no backend by default:

* **No server-side vulnerabilities** in the default configuration
* **No database** to secure
* **Limited attack surface** compared to dynamic applications

However, users should still:

* **Keep hosting platform secure**
* **Use HTTPS**
* **Monitor for unauthorized changes**

## Security Updates

Security updates will be released as soon as possible after a vulnerability is confirmed and patched. Updates will be announced through:

* GitHub Security Advisories
* GitHub Releases
* README updates

## Acknowledgments

We appreciate the security research community and will acknowledge security researchers who report valid vulnerabilities (with their permission).

## Questions?

If you have questions about this security policy, please create an issue or contact the maintainers.

---

*Thank you for helping keep NovelPaper safe!* 🛡️
