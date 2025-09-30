# Contributing to AWS Account Creation Workshop

Thank you for your interest in contributing to the AWS Account Creation Workshop! This document provides guidelines and information for contributors.

## 🤝 How to Contribute

### Types of Contributions

1. **Content Updates**
   - Update screenshots to reflect current AWS interface
   - Fix typos and grammatical errors
   - Improve explanations and clarity
   - Add missing information

2. **Translations**
   - Improve existing Vietnamese translations
   - Add new language translations
   - Ensure cultural appropriateness

3. **Technical Improvements**
   - Fix bugs in Hugo configuration
   - Improve site performance
   - Enhance mobile responsiveness
   - Add new features

4. **Documentation**
   - Improve README and documentation
   - Add code comments
   - Create troubleshooting guides

## 🚀 Getting Started

### Prerequisites

- Git installed on your machine
- Hugo Extended v0.131.0 or later
- Basic knowledge of Markdown
- Familiarity with AWS services (for content contributions)

### Setup Development Environment

1. **Fork the Repository**
   ```bash
   # Fork on GitHub, then clone your fork
   git clone https://github.com/YOUR-USERNAME/000001-CreateAWSAccount.git
   cd 000001-CreateAWSAccount
   ```

2. **Install Hugo**
   ```bash
   # Download Hugo Extended from https://github.com/gohugoio/hugo/releases
   # Or use package manager:
   
   # macOS
   brew install hugo
   
   # Ubuntu/Debian
   sudo apt install hugo
   
   # Windows
   choco install hugo-extended
   ```

3. **Start Development Server**
   ```bash
   hugo server -D
   ```

4. **Access Local Site**
   - Open browser to `http://localhost:1313`

### Making Changes

1. **Create a Branch**
   ```bash
   git checkout -b feature/your-feature-name
   # or
   git checkout -b fix/issue-description
   ```

2. **Make Your Changes**
   - Follow the style guidelines below
   - Test your changes locally
   - Ensure the site builds without errors

3. **Commit Your Changes**
   ```bash
   git add .
   git commit -m "Brief description of changes"
   ```

4. **Push and Create Pull Request**
   ```bash
   git push origin your-branch-name
   ```
   - Create a pull request on GitHub
   - Provide a clear description of your changes

## 📝 Content Guidelines

### Writing Style

- **Clear and Concise**: Use simple, direct language
- **Step-by-Step**: Break complex processes into numbered steps
- **Consistent Terminology**: Use AWS official terminology
- **Inclusive Language**: Ensure content is accessible to all users

### Screenshot Guidelines

- **Current Interface**: Use the latest AWS console interface
- **High Quality**: Minimum 1920x1080 resolution
- **Consistent Browser**: Use Chrome with clean interface
- **Highlight Important Elements**: Use red boxes or arrows when needed
- **File Naming**: Use descriptive names (e.g., `create-account-step-1.png`)

### Markdown Standards

```markdown
# Main Heading (H1) - One per page
## Section Heading (H2)
### Subsection Heading (H3)

**Bold text** for emphasis
*Italic text* for terms
`Code snippets` for technical terms

{{% notice note %}}
Use notice shortcodes for important information
{{% /notice %}}

![Alt text](/images/folder/filename.png?featherlight=false&width=90pc)
```

### Image Management

- Store images in appropriate `/static/images/` subdirectories
- Use descriptive alt text for accessibility
- Optimize images for web (WebP format preferred)
- Keep file sizes under 500KB when possible

## 🌐 Translation Guidelines

### Vietnamese Translation

- Maintain technical accuracy while ensuring cultural appropriateness
- Use consistent terminology throughout
- Preserve formatting and structure
- Include Vietnamese-specific considerations when relevant

### Adding New Languages

1. Create new language section in `config.toml`
2. Create corresponding content directories
3. Translate all content files
4. Update navigation and menus
5. Test thoroughly

## 🔧 Technical Guidelines

### Hugo Configuration

- Follow existing configuration patterns
- Test changes with `hugo server -D`
- Ensure builds complete without errors
- Validate generated HTML

### CSS/JavaScript

- Use existing theme variables when possible
- Follow responsive design principles
- Test on multiple browsers and devices
- Minimize custom code

### Performance

- Optimize images before committing
- Use Hugo's built-in optimization features
- Test page load times
- Ensure mobile performance

## 🧪 Testing

### Before Submitting

- [ ] Site builds without errors (`hugo`)
- [ ] All pages load correctly
- [ ] Images display properly
- [ ] Links work correctly
- [ ] Mobile responsiveness verified
- [ ] Search functionality works
- [ ] Multi-language navigation works

### Testing Checklist

1. **Content Testing**
   - Follow workshop steps with fresh AWS account
   - Verify all instructions are current
   - Check for broken links

2. **Technical Testing**
   - Test on Chrome, Firefox, Safari, Edge
   - Verify mobile responsiveness
   - Check page load times
   - Validate HTML/CSS

3. **Accessibility Testing**
   - Use screen reader to test navigation
   - Verify keyboard navigation works
   - Check color contrast ratios
   - Ensure alt text is descriptive

## 📋 Pull Request Process

### PR Requirements

- [ ] Clear, descriptive title
- [ ] Detailed description of changes
- [ ] Screenshots for visual changes
- [ ] Testing completed
- [ ] Documentation updated if needed

### Review Process

1. **Automated Checks**: CI/CD pipeline runs tests
2. **Peer Review**: At least one team member reviews
3. **QA Testing**: QA team validates changes
4. **Approval**: Maintainer approves and merges

### PR Template

```markdown
## Description
Brief description of changes made.

## Type of Change
- [ ] Bug fix
- [ ] New feature
- [ ] Content update
- [ ] Documentation update
- [ ] Translation

## Testing
- [ ] Local testing completed
- [ ] Cross-browser testing done
- [ ] Mobile testing completed
- [ ] Accessibility verified

## Screenshots
Include screenshots for visual changes.

## Additional Notes
Any additional information for reviewers.
```

## 🐛 Reporting Issues

### Bug Reports

Use the GitHub issue template and include:
- Clear description of the problem
- Steps to reproduce
- Expected vs actual behavior
- Browser and device information
- Screenshots if applicable

### Feature Requests

- Describe the feature and its benefits
- Explain the use case
- Consider implementation complexity
- Discuss potential alternatives

## 📞 Getting Help

- **GitHub Issues**: For bugs and feature requests
- **Discussions**: For questions and general discussion
- **Email**: Contact maintainers for sensitive issues
- **Slack**: Join the AWS Study Group community

## 🏆 Recognition

Contributors will be recognized in:
- README.md contributors section
- Release notes for significant contributions
- Annual contributor appreciation

## 📄 License

By contributing, you agree that your contributions will be licensed under the same license as the project (MIT License).

---

**Thank you for contributing to the AWS Account Creation Workshop!**

For questions about contributing, please open an issue or contact the maintainers.
