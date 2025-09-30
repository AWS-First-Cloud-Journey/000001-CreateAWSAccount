# AWS First Cloud Journey - Create AWS Account Workshop

A comprehensive workshop guide for creating and securing your first AWS account, built with Hugo static site generator.

## 🎯 Workshop Overview

This workshop provides step-by-step guidance for:
- Creating a new AWS account
- Setting up Multi-Factor Authentication (MFA)
- Creating administrator users and groups
- Configuring AWS Management Console
- Getting AWS Support assistance

## 📋 Prerequisites

- Valid email address
- Credit/debit card for account verification
- Mobile phone for MFA setup
- Basic understanding of cloud computing concepts

## 🏗️ Project Structure

```
000001-CreateAWSAccount/
├── content/                    # Workshop content (Markdown files)
│   ├── 1-Create-New-AWS-Account/
│   ├── 2-MFA-Setup-For-AWS-User-(root)/
│   ├── 3-Create-Admin-User-and-Group/
│   ├── 4-verify-new-account/
│   ├── 5-Explore-and-configure-the-AWS-Management-Console/
│   └── 6-Support-cases/
├── static/                     # Static assets (images, CSS)
├── themes/hugo-theme-learn/    # Hugo Learn theme
├── layouts/                    # Custom layout overrides
├── public/                     # Generated site output
└── config.toml                # Hugo configuration
```

## 🚀 Quick Start

### Local Development

1. **Install Hugo Extended**
   ```bash
   # Download and extract Hugo (already included in project)
   tar -xzf hugo_extended_0.131.0_linux-amd64.tar.gz
   sudo mv hugo /usr/local/bin/
   ```

2. **Start Development Server**
   ```bash
   hugo server -D
   ```

3. **Access Workshop**
   - Open browser to `http://localhost:1313`
   - Available in English and Vietnamese

### Build for Production

```bash
hugo --minify
```

## 📚 Workshop Modules

### Module 1: Create New AWS Account
- Account registration process
- Payment method setup
- Phone verification
- Support plan selection

### Module 2: MFA Setup for Root User
- Virtual MFA device configuration
- U2F security key setup
- Hardware MFA device options

### Module 3: Create Admin User and Group
- IAM best practices
- Administrator group creation
- User management

### Module 4: Account Verification
- AWS Support case creation
- Account authentication process

### Module 5: AWS Management Console
- Console navigation
- Region configuration
- Dashboard customization

### Module 6: Support Cases
- Support plan overview
- Case management
- Best practices

## 🌐 Multi-Language Support

- **English**: Primary language
- **Vietnamese**: Complete translation available

## 🔧 Configuration

### Hugo Configuration (`config.toml`)
- Theme: `hugo-theme-learn`
- Multi-language setup
- Search functionality enabled
- Workshop theme variant

### Key Features
- Responsive design
- Search functionality
- Multi-language navigation
- Code syntax highlighting
- Image lightbox support

## 📝 Content Management

### Adding New Content
1. Create new Markdown file in appropriate module directory
2. Use proper front matter:
   ```yaml
   ---
   title: "Page Title"
   date: 2024-01-01
   weight: 1
   chapter: false
   pre: " <b> 1. </b> "
   ---
   ```

### Image Management
- Store images in `static/images/` directory
- Use Hugo shortcodes for responsive images
- Include alt text for accessibility

## 🚀 Deployment

### GitHub Pages
Repository is configured for GitHub Pages deployment at:
`https://github.com/AWS-First-Cloud-Journey/000001-CreateAWSAccount`

### Manual Deployment
1. Build site: `hugo --minify`
2. Deploy `public/` directory to web server

## 🤝 Contributing

### Content Updates
- [ ] Review and update AWS console screenshots
- [ ] Verify all links and references
- [ ] Update pricing information
- [ ] Add new MFA device types
- [ ] Enhance troubleshooting sections

### Technical Improvements
- [ ] Optimize image sizes and formats
- [ ] Implement automated testing
- [ ] Add CI/CD pipeline
- [ ] Enhance mobile responsiveness
- [ ] Add interactive elements

### Translation Tasks
- [ ] Review Vietnamese translations
- [ ] Add additional language support
- [ ] Update terminology consistency
- [ ] Verify cultural appropriateness

## 📋 Task Assignments

### Priority 1 (Immediate)
- **Content Team**: Update AWS console screenshots (Q4 2024 interface)
- **Technical Team**: Remove large binary files (go1.22.6.linux-amd64.tar.gz)
- **QA Team**: Test all workshop steps with new AWS accounts

### Priority 2 (Short-term)
- **Design Team**: Improve mobile experience
- **Content Team**: Add troubleshooting FAQ section
- **Technical Team**: Implement automated link checking

### Priority 3 (Long-term)
- **Product Team**: Add interactive AWS simulator
- **Content Team**: Create video supplements
- **Technical Team**: Migrate to Hugo modules

## 🔍 Quality Assurance

### Content Review Checklist
- [ ] All screenshots current (within 6 months)
- [ ] Links functional and secure (HTTPS)
- [ ] Instructions tested with fresh AWS account
- [ ] Multi-language consistency verified
- [ ] Accessibility standards met

### Technical Review Checklist
- [ ] Site builds without errors
- [ ] All pages load correctly
- [ ] Search functionality works
- [ ] Mobile responsiveness verified
- [ ] Performance optimized

## 📊 Analytics & Metrics

### Success Metrics
- Workshop completion rate
- User feedback scores
- Time to complete modules
- Support case reduction

### Tracking Implementation
- Google Analytics integration
- User journey mapping
- Feedback collection forms
- A/B testing framework

## 🛠️ Maintenance

### Regular Tasks (Monthly)
- Update AWS service screenshots
- Verify external links
- Review user feedback
- Update dependencies

### Quarterly Reviews
- Content accuracy audit
- Performance optimization
- Security updates
- User experience improvements

## 📞 Support & Contact

- **Technical Issues**: Create GitHub issue
- **Content Questions**: Contact workshop maintainers
- **AWS Support**: Use official AWS support channels

## 📄 License

This workshop content is provided under the MIT License. See LICENSE file for details.

## 🏷️ Tags

`aws` `cloud-computing` `workshop` `tutorial` `account-setup` `security` `mfa` `iam` `hugo` `documentation`

---

**Last Updated**: September 30, 2024  
**Version**: 1.0.0  
**Maintainers**: AWS Study Group Community
