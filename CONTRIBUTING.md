# Contributing to NovelPaper

First off, thank you for considering contributing to NovelPaper! It's people like you that make NovelPaper such a great project.

## Code of Conduct

This project and everyone participating in it is governed by the [NovelPaper Code of Conduct](CODE_OF_CONDUCT.md). By participating, you are expected to uphold this code. Please report unacceptable behavior through the project's issue tracker.

## How Can I Contribute?

### Reporting Bugs

This section guides you through submitting a bug report for NovelPaper. Following these guidelines helps maintainers and the community understand your report, reproduce the behavior, and find related reports.

**Before Submitting A Bug Report:**

* Check the documentation for common issues and solutions
* Perform a cursory search to see if the problem has already been reported
* Ensure you're using the latest version

**How Do I Submit A Good Bug Report?**

Bugs are tracked as GitHub issues. Create an issue and provide the following information:

* **Use a clear and descriptive title**
* **Describe the exact steps which reproduce the problem**
* **Provide specific examples to demonstrate the steps**
* **Describe the behavior you observed after following the steps**
* **Explain which behavior you expected to see instead and why**
* **Include screenshots if applicable**
* **Include your browser, OS, and screen resolution**

### Suggesting Enhancements

This section guides you through submitting an enhancement suggestion for NovelPaper, including completely new features and minor improvements to existing functionality.

**Before Submitting An Enhancement Suggestion:**

* Check if the enhancement has already been suggested
* Determine which part of the project the enhancement relates to

**How Do I Submit A Good Enhancement Suggestion?**

Enhancement suggestions are tracked as GitHub issues. Create an issue and provide the following information:

* **Use a clear and descriptive title**
* **Provide a step-by-step description of the suggested enhancement**
* **Provide specific examples to demonstrate the steps**
* **Describe the current behavior and explain the behavior you expected to see**
* **Explain why this enhancement would be useful**
* **Include mockups or design ideas if applicable**

### Pull Requests

**Process:**

1. Fork the repo and create your branch from `main`
2. Make your changes
3. Test your changes thoroughly
4. Ensure your code follows the existing style
5. Update documentation if necessary
6. Submit a pull request

**Pull Request Guidelines:**

* Follow the existing code style
* Write clear, concise commit messages
* Include comments for complex logic
* Update the README.md if needed
* Keep pull requests focused on a single feature or fix

## Development Setup

### Prerequisites

* Modern web browser (Chrome, Firefox, Safari, Edge)
* Text editor or IDE
* Basic knowledge of HTML, CSS, and JavaScript
* (Optional) Local web server for testing

### Local Development

1. **Clone the repository**
   ```bash
   git clone https://github.com/Hostilian/novelpaper.git
   cd novelpaper
   ```

2. **Open the project**
   * You can open `index.html` directly in a browser
   * Or use a local server:
     ```bash
     # Python 3
     python -m http.server 8000
     
     # Node.js
     npx http-server
     ```

3. **Make your changes**
   * Edit HTML, CSS, or JavaScript files
   * Refresh your browser to see changes
   * No build process required!

### Project Structure

```
novelpaper/
├── index.html          # Main HTML file
├── styles.css          # All styling
├── script.js           # Interactive features
├── README.md           # Project documentation
├── LICENSE             # MIT License
├── CODE_OF_CONDUCT.md  # Community guidelines
└── CONTRIBUTING.md     # This file
```

## Style Guidelines

### HTML

* Use semantic HTML5 elements
* Include proper ARIA labels
* Maintain proper heading hierarchy
* Keep markup clean and readable

### CSS

* Follow the existing naming conventions
* Use CSS custom properties for colors and spacing
* Write mobile-first responsive styles
* Comment complex selectors

### JavaScript

* Use modern ES6+ syntax
* Write clear, descriptive function names
* Comment complex logic
* Avoid unnecessary dependencies
* Follow the existing code style

### Code Formatting

* Use 4 spaces for indentation
* Use meaningful variable and function names
* Add comments for complex logic
* Keep functions focused and small
* Use consistent naming conventions

## Testing

Before submitting a pull request:

1. **Browser Testing**
   * Test in Chrome, Firefox, Safari, and Edge
   * Test on mobile devices (iOS and Android)
   * Verify responsive behavior at different screen sizes

2. **Accessibility Testing**
   * Test keyboard navigation
   * Verify screen reader compatibility
   * Check color contrast ratios
   * Test with reduced motion enabled

3. **Performance Testing**
   * Check page load speed
   * Verify smooth animations
   * Test on slower devices/connections

## Documentation

* Update README.md for new features
* Add inline comments for complex code
* Update this CONTRIBUTING.md if process changes
* Keep documentation clear and concise

## Commit Messages

* Use clear and meaningful commit messages
* Start with a verb in present tense (Add, Fix, Update, etc.)
* Keep the first line under 50 characters
* Add detailed description if needed

**Examples:**

```
Add parallax effect to hero section

Fix mobile menu not closing on link click

Update color palette with warmer tones
```

## Questions?

Feel free to create an issue with your question, or reach out through the contact form on the website.

## Recognition

Contributors will be acknowledged in the project. Thank you for making NovelPaper better!

---

*Thank you for contributing to NovelPaper! Where Stories Take Shape.* ✨
