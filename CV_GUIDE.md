# Professional CV Template - Usage Guide

This is a professional, ATS-friendly CV template designed for Senior Software Engineers with expertise in AI/ML, Blockchain, and IoT.

## Features

✨ **Clean & Professional Design**
- Modern typography with excellent readability
- Professional color scheme (blues and grays)
- Clear visual hierarchy for easy scanning

📱 **Fully Responsive**
- Desktop: Multi-column layout for optimal space usage
- Tablet: Adaptive grid system
- Mobile: Single column, touch-friendly design

🖨️ **Print-Ready**
- Optimized for PDF generation
- Proper page breaks to avoid splitting sections
- Clean print styles without shadows or effects

🤖 **ATS-Friendly**
- Semantic HTML structure
- Simple, parseable layout
- Text-based content (no critical info in images)
- Proper heading hierarchy (H1-H4)

♿ **Accessible**
- WCAG 2.1 compliant
- Focus indicators for keyboard navigation
- High contrast mode support
- Reduced motion support

## How to Use

### 1. Customize Your Information

Open `cv.html` in a text editor and replace the following sections with your own information:

#### Header (Lines 15-33)
- **Name**: Update `<h1 class="name">` with your full name
- **Title**: Update `<h2 class="title">` with your current role
- **Contact Info**: Update email, LinkedIn, GitHub, Twitter links

#### Professional Summary (Lines 36-46)
- Rewrite the summary to reflect your unique experience and career goals
- Keep it concise (3-5 sentences)
- Focus on your value proposition

#### Technical Skills (Lines 49-140)
- Add or remove skill categories as needed
- List technologies you're proficient in
- Group related skills together
- Keep lists concise and relevant

#### Professional Experience (Lines 143-178)
- Add your work history (most recent first)
- Replace `[Previous Company Name]` and dates
- Use bullet points to highlight achievements
- Quantify results when possible (e.g., "improved performance by 40%")

#### Education (Lines 181-200)
- Update degree, institution, and graduation year
- Add relevant coursework or honors
- Include GPA if it's impressive (>3.5)

#### Key Projects (Lines 203-250)
- Showcase 3-5 significant projects
- Include tech stack used
- Highlight measurable outcomes
- Focus on projects relevant to your target role

#### Certifications (Lines 253-267)
- List relevant certifications
- Include issuing organization
- Add or remove items as needed
- You can remove this section if you don't have certifications

### 2. Customize the Styling (Optional)

If you want to adjust colors, fonts, or spacing, edit `cv-style.css`:

#### Change Color Scheme (Lines 12-19)
```css
:root {
    --primary-color: #2c3e50;      /* Main headings */
    --secondary-color: #34495e;     /* Subheadings */
    --accent-color: #3498db;        /* Bullets, borders */
    --text-primary: #2c3e50;        /* Body text */
    --text-secondary: #555555;      /* Secondary text */
    --text-light: #777777;          /* Dates, metadata */
    --link-color: #3498db;          /* Links */
}
```

#### Change Fonts (Lines 21-22)
```css
:root {
    --font-primary: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    --font-secondary: Georgia, 'Times New Roman', serif;
}
```

#### Adjust Spacing (Lines 24-29)
```css
:root {
    --spacing-xs: 0.25rem;
    --spacing-sm: 0.5rem;
    --spacing-md: 1rem;
    --spacing-lg: 1.5rem;
    --spacing-xl: 2rem;
    --spacing-xxl: 3rem;
}
```

### 3. Preview Your CV

#### Option 1: Open in Browser
- Double-click `cv.html` to open in your default browser
- Or drag and drop `cv.html` into a browser window

#### Option 2: Use a Local Server
```bash
# Python 3
python -m http.server 8080

# Then open http://localhost:8080/cv.html in your browser
```

### 4. Generate PDF

#### Option 1: Browser Print
1. Open `cv.html` in your browser (Chrome recommended)
2. Press `Ctrl+P` (Windows/Linux) or `Cmd+P` (Mac)
3. Select "Save as PDF" as the destination
4. Settings:
   - Layout: Portrait
   - Margins: Default
   - Scale: 100%
   - Background graphics: Enabled (optional)
5. Click "Save"

#### Option 2: Use Chrome Headless (Command Line)
```bash
# Install Chrome/Chromium first, then:
google-chrome --headless --print-to-pdf=cv.pdf cv.html

# Or with custom paper size:
google-chrome --headless --print-to-pdf=cv.pdf --print-to-pdf-no-header cv.html
```

## Customization Tips

### Adding a Photo
While ATS systems may not parse images well, if you want to add a photo:

1. Add this HTML after the `<h2 class="title">` line:
```html
<img src="profile.jpg" alt="Your Name" class="profile-photo">
```

2. Add this CSS to `cv-style.css`:
```css
.profile-photo {
    width: 150px;
    height: 150px;
    border-radius: 50%;
    object-fit: cover;
    margin: 1rem auto;
    display: block;
}
```

### Adding More Sections
To add a new section (e.g., "Publications", "Awards", "Languages"):

1. Copy an existing section structure
2. Update the heading and content
3. Place it logically in the document flow

Example:
```html
<section class="section languages">
    <h3 class="section-title">Languages</h3>
    <div class="section-content">
        <ul class="certification-list">
            <li>
                <span class="cert-name">English</span>
                <span class="cert-issuer">Native/Fluent</span>
            </li>
            <li>
                <span class="cert-name">Spanish</span>
                <span class="cert-issuer">Professional Working Proficiency</span>
            </li>
        </ul>
    </div>
</section>
```

### Removing Sections
To remove a section you don't need:
1. Find the `<section>` tag with the relevant class
2. Delete from `<section>` to its closing `</section>` tag

## Best Practices

### Content Guidelines
- **Be Concise**: Use bullet points, not paragraphs
- **Quantify Results**: Use numbers, percentages, metrics
- **Action Verbs**: Start bullets with strong verbs (Led, Developed, Implemented, Optimized)
- **Relevant Skills**: Only list skills relevant to your target role
- **Proofread**: Check for typos and grammatical errors

### ATS Optimization
- **Keywords**: Include relevant keywords from job descriptions
- **Standard Headings**: Use common section names (Experience, Education, Skills)
- **No Tables**: Avoid complex tables (this template doesn't use them)
- **Simple Formatting**: Avoid text boxes, graphics with text, columns for main content

### File Naming
When saving your PDF, use a professional format:
- `FirstName_LastName_Resume.pdf`
- `FirstName_LastName_SeniorSoftwareEngineer.pdf`
- Avoid special characters or spaces

## Troubleshooting

### Links Not Working in PDF
This is normal - PDF readers handle links differently. The links will work in the HTML version.

### Formatting Issues When Printing
1. Make sure to print from Chrome or Edge (best CSS support)
2. Enable "Background graphics" in print settings
3. Set margins to "Default" or "None"

### Mobile View Looks Wrong on Desktop
The responsive design adapts based on screen width. Resize your browser window to see different layouts.

### Some Sections Don't Fit on One Page
1. Reduce content slightly
2. Adjust spacing in CSS (decrease `--spacing-*` values)
3. Use smaller font size in print CSS

## Support

For questions or issues:
- Check existing GitHub issues
- Create a new issue with details
- Email: wahsandaruwan6@gmail.com

## License

This CV template is free to use and modify for personal use. Attribution is appreciated but not required.

---

**Created by Himal Sandaruwan**  
Senior Software Engineer | AI/ML, Blockchain, IoT Specialist
