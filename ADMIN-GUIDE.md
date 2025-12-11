# Admin Quick Start Guide - Connect Card vCard System

## 🎯 Overview

This guide will help you manage the Connect Card vCard generation system for your clients.

## 🚀 Initial Setup (One-Time)

### 1. Deploy to GitHub Pages
```bash
# Already set up if you're reading this!
# Make sure GitHub Pages is enabled in repo settings
```

Your form will be available at:
- **Development**: Open `form.html` locally
- **Production**: `https://niccyp.github.io/vCardProject/form.html`

### 2. Share with Clients

Send clients to the form URL with these instructions:
```
Hi [Client Name],

Create your Connect Card profile here:
https://niccyp.github.io/vCardProject/form.html

Instructions: https://niccyp.github.io/vCardProject/CLIENT-INSTRUCTIONS.md

Once done, email your HTML file to hello@connectcard.com.au

Thanks!
```

## 📥 Client Workflow

### When a Client Submits Their vCard:

1. **Receive Email**
   - Client sends their generated HTML file (e.g., `john-smith.html`)
   - May include photos if they uploaded them

2. **Review Content**
   - Open the HTML file in a browser
   - Check for:
     - ✅ Professional appearance
     - ✅ Correct contact information
     - ✅ Appropriate photos
     - ✅ No broken links
     - ✅ Proper spelling/grammar

3. **Save to Repository**
   ```bash
   # Save file to clients directory
   # Naming: firstname-lastname.html
   vCard-template/clients/john-smith.html
   ```

4. **Commit and Push**
   ```bash
   git add vCard-template/clients/john-smith.html
   git commit -m "Add vCard for John Smith"
   git push
   ```

5. **Get Live URL**
   ```
   https://niccyp.github.io/vCardProject/vCard-template/clients/john-smith.html
   ```

6. **Program NFC Card**
   - Use your NFC programming tool
   - Write the URL to the NFC chip
   - Test with your phone

7. **Confirm with Client**
   ```
   Hi John,

   Your Connect Card is ready! Your profile is live at:
   https://niccyp.github.io/vCardProject/vCard-template/clients/john-smith.html

   Your card is programmed and will be shipped [shipping details].

   Thanks!
   ```

## 🔄 Client Updates

When a client wants to update their vCard:

1. **Client Actions**
   - They fill out the form again with new info
   - Generate new vCard
   - Email updated file

2. **Your Actions**
   - Replace old file with new one (same filename)
   - Commit and push
   - NFC card automatically works with new content!
   - ✅ No need to reprogram the card

## 📁 File Organization

### Recommended Structure:
```
vCard-template/
├── clients/
│   ├── john-smith.html
│   ├── sarah-johnson.html
│   ├── mike-chen.html
│   └── emily-davis.html
└── images/
    └── client-uploads/  (if storing images separately)
```

### Naming Convention:
- Use lowercase
- Replace spaces with hyphens
- No special characters
- Format: `firstname-lastname.html`

Examples:
- ✅ `john-smith.html`
- ✅ `mary-jane-watson.html`
- ✅ `dr-robert-jones.html`
- ❌ `John Smith.html`
- ❌ `john_smith.html`
- ❌ `JohnSmith.html`

## 🛠️ Troubleshooting

### Common Issues:

#### Issue: "Photos not showing"
**Solution**: The form embeds photos as base64. If the file is very large, some email clients might block it. Ask client to use smaller images (under 1MB each).

#### Issue: "Generated HTML won't download"
**Solution**: Try a different browser. Works best in Chrome, Firefox, Edge.

#### Issue: "vCard (.vcf) download not working"
**Solution**: This is a client-side feature. Ensure they're clicking the "Save Contact" button on their live vCard page, not the form.

#### Issue: "Links not clickable"
**Solution**: Ensure URLs include `https://` prefix (e.g., `https://www.example.com`)

#### Issue: "Email has attachment issues"
**Solution**: Large HTML files with embedded images can be 1-3MB. Use file sharing services like Dropbox/Google Drive if needed.

## 📊 Quality Control Checklist

Before deploying a client's vCard:

- [ ] Name spelled correctly
- [ ] Professional profile photo
- [ ] Contact info tested (click call/email buttons)
- [ ] All links work (website, LinkedIn)
- [ ] Bio is appropriate and typo-free
- [ ] Theme color looks good
- [ ] Mobile responsive (test on phone)
- [ ] "Save Contact" button works
- [ ] File named correctly
- [ ] Committed to git repository

## 🎨 Customization Requests

### Client Wants Different Colors:
The form has 6 preset colors. For custom colors:

1. Have them choose closest preset
2. Manually edit their HTML file:
   ```css
   :root {
       --primary-color: #YOUR_COLOR;
   }
   ```
3. Save and commit

### Client Wants Additional Fields:
Currently supported:
- ✅ Phone, Email, Website, LinkedIn
- ✅ Name, Title, Company, Bio
- ✅ Profile & Cover Photos

For additional fields (Instagram, Twitter, etc.):
- Manually edit their HTML file
- Add button in the buttons-container section

### Client Wants Custom Layout:
Use one of their generated pages as a template and customize it manually. Keep the basic structure for consistency.

## 📈 Scaling Tips

### Managing Many Clients:

1. **Spreadsheet Tracking**
   ```
   Client Name | Email | vCard File | Live URL | NFC Programmed | Shipped
   John Smith | john@... | john-smith.html | https://... | ✅ | ✅
   ```

2. **Organized Folders**
   ```
   clients/
   ├── 2025-01/
   ├── 2025-02/
   └── 2025-03/
   ```

3. **Automated Testing**
   Periodically check all client URLs are still live

4. **Backup Strategy**
   - Git repository is your backup
   - GitHub keeps all history
   - Can restore old versions anytime

## 🔐 Privacy & Security

- Client photos are embedded in HTML (base64)
- No external image hosting needed
- All data is static HTML
- No databases or servers required
- HTTPS via GitHub Pages (secure)

## 💡 Pro Tips

1. **Test First**: Always test the vCard on your phone before programming NFC
2. **Batch Processing**: Program multiple NFC cards at once
3. **Template Emails**: Save response templates for common requests
4. **Mobile Preview**: Always check on mobile - that's where most people will see it
5. **URL Shortener**: Consider using a custom domain for cleaner URLs

## 📞 Client Support Templates

### Update Request Response:
```
Hi [Client],

To update your vCard:
1. Visit: https://niccyp.github.io/vCardProject/form.html
2. Fill in your new information
3. Generate and download
4. Email the new file to me

Your NFC card will automatically show the new info once I update it.

Thanks!
```

### Technical Issue Response:
```
Hi [Client],

I see you're having trouble with the form. Here are some tips:

- Use Chrome or Firefox browser
- Make sure images are under 5MB
- Include https:// in website URLs
- Use +61 format for phone numbers

Need more help? Give me a call!

Thanks!
```

## 🎓 Learning Resources

- **Form Code**: `form.html` (fully commented)
- **Template Code**: `vCard-template/template.html`
- **Example**: `vCard-template/clients/example-sarah-johnson.html`
- **Client Guide**: `CLIENT-INSTRUCTIONS.md`

## 📝 Next Steps

1. ✅ Test the form yourself
2. ✅ Generate a sample vCard
3. ✅ Program a test NFC card
4. ✅ Share form link with first clients
5. ✅ Set up email templates
6. ✅ Create client tracking spreadsheet

---

**Questions?** Check README.md or review the code comments.

**Ready to go!** 🚀 Share the form with your first client and start creating awesome Connect Cards!
