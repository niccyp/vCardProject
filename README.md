# vCardProject - Connect Card Digital Profiles

NFC-enabled 3D printed business cards that link to personalized client profile pages hosted in this repository.

## 🎯 Project Overview

This repository manages digital vCard profile pages for Connect Card clients. Clients use an online form to generate their personalized profile pages, which are then linked to their NFC business cards.

## 📁 Repository Structure

```
vCardProject/
├── index.html                  # Main marketing website
├── form.html                   # Client form generator (NEW!)
├── CLIENT-INSTRUCTIONS.md      # Step-by-step guide for clients
├── vCard-template/
│   ├── template.html          # Enhanced template with placeholders
│   ├── nic.pol.html          # Example client profile
│   └── clients/              # Directory for client profile pages
│       └── nic.pol.html
└── images/                    # Shared images and assets
```

## 🚀 How It Works

### For Clients:

1. **Visit the Form**: Clients access `form.html` in their browser
2. **Fill in Details**: Enter name, job title, company, bio, contact info
3. **Upload Photos**: Add profile picture and optional cover photo
4. **Choose Theme**: Select a color scheme
5. **Generate**: Click "Generate vCard" to create their page
6. **Download**: Download the HTML file
7. **Submit**: Email the file to you for hosting

### For You (Admin):

1. **Receive vCard**: Client emails their generated HTML file
2. **Review**: Check the content and photos
3. **Host**: Upload to `vCard-template/clients/[client-name].html`
4. **Program NFC**: Link the NFC chip to the hosted URL
5. **Deliver**: Send the physical card to the client

## 🎨 Features

### Client Form (`form.html`)
- ✅ User-friendly form interface
- ✅ Profile photo upload with preview
- ✅ Optional cover photo upload
- ✅ Theme color selection (6 colors)
- ✅ Real-time photo preview
- ✅ Client-side vCard generation
- ✅ Download as HTML file
- ✅ Preview in new tab option
- ✅ Form validation

### Generated vCard Pages
- ✅ Modern, responsive design
- ✅ Profile photo (circular)
- ✅ Cover photo or gradient background
- ✅ Name, title, company display
- ✅ Brief bio section
- ✅ Contact buttons (Call, Email)
- ✅ Optional Website link
- ✅ Optional LinkedIn link
- ✅ "Save Contact" button (downloads .vcf file)
- ✅ Customizable theme colors
- ✅ Mobile-optimized layout

## 🔧 Technical Details

### Form Generator
- Pure HTML/CSS/JavaScript (no backend required)
- Client-side image processing using FileReader API
- Base64 encoding for embedded images
- Generates standalone HTML files
- Includes embedded vCard data for contact downloads

### Template System
The `template.html` uses placeholders for easy customization:
- `{{NAME}}` - Client's full name
- `{{JOB_TITLE}}` - Job title
- `{{COMPANY}}` - Company name
- `{{BIO}}` - Brief bio
- `{{EMAIL}}` - Email address
- `{{PHONE}}` - Phone number
- `{{WEBSITE}}` - Website URL
- `{{LINKEDIN}}` - LinkedIn URL
- `{{COLOR}}` - Theme color
- `{{PHOTO_PATH}}` - Profile photo
- `{{COVER_PHOTO}}` - Cover photo HTML
- `{{VCARD_DATA}}` - vCard contact data

## 📋 Client Workflow

### Step 1: Access Form
Send clients this link: `https://[your-domain]/form.html`

### Step 2: Form Submission
Clients fill out the form and click "Generate vCard"

### Step 3: Download
They download their personalized HTML file (e.g., `john-smith.html`)

### Step 4: Email Submission
Clients email the file to you at: `hello@connectcard.com.au`

### Step 5: Hosting
You upload their file to the repository and program their NFC card

## 📧 Client Communication

### Welcome Email Template
```
Subject: Welcome to Connect Card!

Hi [Client Name],

Thank you for choosing Connect Card! To create your personalized digital profile:

1. Visit: [your-domain]/form.html
2. Fill in your details
3. Upload your photos
4. Generate and download your vCard
5. Email the file back to us

Need help? Check out our guide: CLIENT-INSTRUCTIONS.md

Best regards,
Connect Card Team
```

## 🎯 Best Practices

### Photo Guidelines
- **Profile Photo**: Square, minimum 400x400px, professional headshot
- **Cover Photo**: 1200x400px or 3:1 aspect ratio, company logo or background
- **Format**: JPG or PNG
- **Quality**: High resolution for best results

### Content Guidelines
- **Bio**: 1-2 sentences, professional tone
- **Phone**: Include country code (e.g., +61 for Australia)
- **Links**: Always use complete URLs (https://...)
- **Name**: Use professional/legal name

### File Naming
Generated files use this format: `firstname-lastname.html`
- All lowercase
- Hyphens instead of spaces
- No special characters

## 🔄 Updates and Changes

Clients can update their vCard anytime:
1. Fill out the form again with new information
2. Generate a new vCard file
3. Email the updated file
4. You replace the old file with the new one
5. NFC card automatically points to updated content (no reprogramming needed!)

## 🌐 Deployment

### GitHub Pages (Recommended)
1. Enable GitHub Pages in repository settings
2. Set source to main branch
3. Your form will be at: `https://[username].github.io/vCardProject/form.html`

### Custom Domain
1. Add `CNAME` file with your domain
2. Configure DNS settings
3. Access at: `https://connectcard.com.au/form.html`

## 📊 Example Clients

- **Nicholas Pollack**: See `vCard-template/nic.pol.html` for reference
- More examples in `vCard-template/clients/`

## 🛠️ Customization

### Changing Colors
Edit the color options in `form.html` around line 280:
```html
<div class="color-option">
    <input type="radio" name="themeColor" value="#007bff">
    <label class="color-swatch" style="background: #007bff;">Blue</label>
</div>
```

### Adding Fields
1. Add form field in `form.html`
2. Update `generateVCard()` function to capture data
3. Modify `createVCardHTML()` to include new field
4. Update `template.html` with new placeholder

## 📞 Support

For questions or issues:
- **Email**: hello@connectcard.com.au
- **Documentation**: See `CLIENT-INSTRUCTIONS.md`

## 📝 License

© 2025 Connect Card. All rights reserved.

---

**Brisbane, Australia** | Smart NFC Business Cards for the Digital Age
