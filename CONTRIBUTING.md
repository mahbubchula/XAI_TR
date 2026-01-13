# Contributing to XAI_TR

Thank you for your interest in contributing to the XAI_TR course! This document provides guidelines to help you contribute effectively.

## 🌟 Welcome Contributors!

We believe that the best educational content is created collaboratively. Whether you're a student, researcher, or educator, your contributions are valuable and welcome!

## 🎯 Ways to Contribute

### 1. Content Contributions
- Add new examples from your research field
- Create tutorials and walkthroughs
- Develop Jupyter notebooks with detailed explanations
- Write case studies showing real-world applications
- Improve existing module content with clearer explanations

### 2. Visual Content
- Create diagrams and flowcharts
- Design infographics
- Develop animations for complex concepts
- Add illustrations to clarify difficult topics

### 3. Resources
- Share useful references (papers, tutorials, videos)
- Add templates for common tasks
- Recommend tools and software
- Create checklists and worksheets

### 4. Bug Fixes and Improvements
- Fix typos and grammatical errors
- Improve code examples
- Update outdated information
- Enhance documentation clarity

## 📝 Content Style Guide

### Writing Principles

**Keep It Simple**
- Use plain, conversational language
- Avoid jargon when possible
- Define technical terms when first introduced
- Write as if explaining to a friend

**Be Beginner-Friendly**
- Assume no prior programming knowledge
- Explain concepts step-by-step
- Use analogies and real-world examples
- Include "Key Takeaway" boxes for main points

**Structure Your Content**
- Use clear, descriptive headings
- Keep paragraphs short (3-5 sentences)
- Use bullet points and numbered lists
- Include visual breaks between sections

### Content Format Guidelines

#### Module Content Structure
Each module should follow this template:
```markdown
# Module Title

## Overview
Brief description (2-3 sentences)

## Prerequisites
- Required knowledge
- Suggested prior modules

## Learning Objectives
- What you'll learn (3-5 bullet points)

## Content Sections
### Section 1: Topic
Explanation with examples

### Section 2: Topic
More content...

## Hands-on Exercise
Practical activity

## Key Takeaways
- Main point 1
- Main point 2

## Further Reading
- Resource 1
- Resource 2

## Next Steps
Link to next module
```

#### Code Examples
```python
# Use extensive comments
# Explain what each section does

# Example: Load data
import pandas as pd
data = pd.read_csv('example.csv')  # Read CSV file into DataFrame
```

**Code Style:**
- Include comments for every important step
- Use descriptive variable names
- Keep examples simple and focused
- Test all code before submitting

#### Visual Content Standards

**Color Scheme**
- Primary: #2E86AB (Blue - for main concepts)
- Secondary: #A23B72 (Purple - for advanced topics)
- Accent: #F18F01 (Orange - for highlights/warnings)
- Success: #06A77D (Green - for positive outcomes)
- Background: #F4F4F4 (Light gray)

**Diagram Style**
- Use clear, readable fonts (minimum 12pt)
- Include legends where necessary
- Keep designs simple and uncluttered
- Ensure accessibility (color-blind friendly)
- Use consistent styling across all visuals

**File Formats**
- Diagrams: SVG (preferred) or high-res PNG
- Photos/Screenshots: PNG or JPEG
- Animations: GIF (max 5MB) or MP4

**Tools Recommended**
- Diagrams: Draw.io, Lucidchart, or Excalidraw
- Infographics: Canva or Adobe Illustrator
- Animations: Manim, PowerPoint, or After Effects
- Screenshots: Built-in OS tools

## 🔄 Contribution Process

### For Small Changes (typos, minor fixes)

1. **Fork the repository**
   ```bash
   # Click "Fork" on GitHub
   ```

2. **Create a branch**
   ```bash
   git checkout -b fix-typo-module01
   ```

3. **Make your changes**
   - Edit the relevant files
   - Commit with clear message

4. **Submit a Pull Request**
   - Describe what you changed and why
   - Reference any related issues

### For Larger Contributions (new modules, major content)

1. **Open an Issue First**
   - Describe what you want to add
   - Discuss approach with maintainers
   - Get feedback before investing time

2. **Follow the process above**
   - Create your content following our templates
   - Ensure consistency with existing material

3. **Request Review**
   - Tag relevant reviewers
   - Be open to feedback and suggestions

## ✅ Pull Request Checklist

Before submitting your PR, ensure:

- [ ] Content follows the style guide
- [ ] All code examples are tested and working
- [ ] Markdown is properly formatted
- [ ] Links are working and correct
- [ ] Spelling and grammar are checked
- [ ] Visual content meets standards (if applicable)
- [ ] Files are in the correct directories
- [ ] Commit messages are clear and descriptive

## 📋 Adding New Modules

To add a new module:

1. Use the template in `modules/MODULE_TEMPLATE.md`
2. Create a new directory: `modules/XX-module-name/`
3. Add a comprehensive `README.md` in that directory
4. Include at least one hands-on example
5. Update the main README.md to link to your module
6. Update `docs/COURSE_ROADMAP.md` with module details

## 🎨 Creating Visual Content

1. Follow the color scheme and style guidelines
2. Save files in appropriate `/visuals` subdirectories
3. Include source files when possible (.drawio, .ai, etc.)
4. Add alt text descriptions for accessibility
5. Reference visuals in module content

## 🧪 Adding Code Examples

1. Place in appropriate `/examples` subdirectory
2. Include extensive comments
3. Test thoroughly before submitting
4. Add a README explaining what the example demonstrates
5. Keep dependencies minimal and well-documented

## 🤝 Code of Conduct

### Our Standards

**Be Respectful**
- Use welcoming and inclusive language
- Respect different viewpoints and experiences
- Accept constructive criticism gracefully

**Be Collaborative**
- Help others learn and improve
- Share knowledge generously
- Give credit where it's due

**Be Professional**
- Focus on what's best for the community
- Show empathy toward other contributors
- Maintain a positive learning environment

### Unacceptable Behavior

- Harassment or discriminatory language
- Trolling or insulting comments
- Sharing others' private information
- Any conduct inappropriate for a learning environment

## 📞 Getting Help

**Questions about contributing?**
- Open a [Discussion](https://github.com/mahbubchula/XAI_TR/discussions)
- Ask in an [Issue](https://github.com/mahbubchula/XAI_TR/issues)
- Reach out to maintainers

## 🙏 Recognition

All contributors will be:
- Listed in the repository's Contributors page
- Acknowledged in relevant module sections
- Celebrated in our community updates

Thank you for helping make AI research accessible to everyone! 🚀

---

**Questions?** Don't hesitate to ask. We're here to help you contribute successfully!
