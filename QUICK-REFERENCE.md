# 📋 Quick Reference - Connect Card System

## 🔗 Important URLs

### For Clients:
- **Form**: `https://niccyp.github.io/vCardProject/form.html`
- **Instructions**: `https://niccyp.github.io/vCardProject/CLIENT-INSTRUCTIONS.md`

### For You:
- **Main Site**: `https://niccyp.github.io/vCardProject/index.html`
- **Admin Guide**: `ADMIN-GUIDE.md`
- **This Repo**: `https://github.com/niccyp/vCardProject`

## 📧 Email Templates

### Welcome Email
```
Subject: Create Your Connect Card Profile

Hi [Name],

Welcome to Connect Card! To create your digital profile:

1. Go to: https://niccyp.github.io/vCardProject/form.html
2. Fill in your details
3. Upload your photos
4. Generate your vCard
5. Email the file back to hello@connectcard.com.au

Need help? See: https://niccyp.github.io/vCardProject/CLIENT-INSTRUCTIONS.md

Best,
Connect Card Team
```

### Confirmation Email
```
Subject: Your Connect Card is Ready!

Hi [Name],

Your Connect Card profile is live:
https://niccyp.github.io/vCardProject/vCard-template/clients/[name].html

Your card is programmed and will ship [date].

To update your info in the future, just fill out the form again!

Thanks,
Connect Card Team
```

## ⚡ Quick Commands

### Add New Client vCard
```bash
# 1. Save client's HTML to:
vCard-template/clients/firstname-lastname.html

# 2. Commit
git add vCard-template/clients/firstname-lastname.html
git commit -m "Add vCard for Firstname Lastname"
git push

# 3. Live URL:
# https://niccyp.github.io/vCardProject/vCard-template/clients/firstname-lastname.html
```

### Update Existing Client
```bash
# 1. Replace file with new version (same filename)
# 2. Commit
git add vCard-template/clients/firstname-lastname.html
git commit -m "Update vCard for Firstname Lastname"
git push

# URL stays the same - NFC card automatically works!
```

## ✅ Quality Checklist

Before hosting any client vCard:

- [ ] Name spelled correctly
- [ ] Professional photos
- [ ] Email works (click test)
- [ ] Phone works (click test)
- [ ] All URLs have https://
- [ ] Bio is appropriate
- [ ] No typos
- [ ] Tested on mobile
- [ ] File named correctly: `firstname-lastname.html`

## 🎨 Available Theme Colors

Clients can choose from:
- Blue (#007bff)
- Green (#28a745)
- Red (#dc3545)
- Purple (#6f42c1)
- Orange (#fd7e14)
- Teal (#20c997)

## 📸 Photo Requirements

### Profile Photo:
- Square (1:1 ratio)
- Minimum 400x400px
- JPG or PNG
- Under 5MB

### Cover Photo:
- Wide (3:1 ratio)
- Recommended 1200x400px
- JPG or PNG
- Under 5MB
- Optional (gradient used if not provided)

## 🐛 Common Issues & Fixes

| Problem | Solution |
|---------|----------|
| Form won't generate | Use Chrome/Firefox, check required fields |
| Photos not showing | Images too large, resize to <1MB |
| Email bounces back | File too large, use Dropbox/Drive |
| Links not working | Must include `https://` prefix |
| vCard (.vcf) won't download | Works only on live page, not the form |
| Phone formatting | Include country code: `+61 400 000 000` |

## 📁 File Naming Rules

✅ **Correct:**
- `john-smith.html`
- `mary-jane-watson.html`
- `dr-sarah-chen.html`

❌ **Wrong:**
- `John Smith.html` (spaces)
- `john_smith.html` (underscores)
- `JohnSmith.html` (no separator)
- `john.smith.html` (dots in name)

## 🔄 Client Update Process

1. Client fills form again with new info
2. Client generates new vCard
3. Client emails new file
4. You replace old file (same filename)
5. Commit and push
6. Done! NFC card automatically shows new info

## 💼 Workflow Summary

```
CLIENT → Form → Generate → Download → Email to You
                                           ↓
                                    Review & Save
                                           ↓
                                    Commit to Git
                                           ↓
                                    GitHub Pages
                                           ↓
                                  Program NFC Card
                                           ↓
                                    Ship to Client
```

## 📊 Pricing Reference

From your main site:
- **Single Card**: $20
- **Starter Pack (3)**: $50 (save $10)
- **Professional (10)**: $150 (save $50)

## 🎯 Production Timeline

- **In-stock colors**: 3-5 business days
- **Custom colors**: 5-7 business days

## 📦 Card Colors Available

In stock (no wait):
- Jade White
- Red
- Black
- Cocoa Brown
- Sunflower Yellow
- Matte Ash Grey
- Indigo Purple
- Matte Marine Blue
- Green

## 🛠️ Key Files

| File | Purpose |
|------|---------|
| `form.html` | Client form generator |
| `index.html` | Main marketing site |
| `vCard-template/template.html` | Template with placeholders |
| `CLIENT-INSTRUCTIONS.md` | Client guide |
| `ADMIN-GUIDE.md` | Your admin manual |
| `README.md` | Technical documentation |

## 🚨 Emergency Contacts

**Your Email**: hello@connectcard.com.au
**Repository**: https://github.com/niccyp/vCardProject
**Domain**: connectcard.com.au

## 💡 Pro Tips

1. Always test vCard on mobile before programming NFC
2. Keep a spreadsheet of all clients and their URLs
3. Batch process NFC cards for efficiency
4. Save email templates for common responses
5. Check for typos BEFORE hosting
6. Test all links before confirming with client

## 📈 Success Metrics to Track

- Number of cards generated
- Conversion rate (form visits → submissions)
- Most popular theme colors
- Average turnaround time
- Client satisfaction
- Repeat orders

---

**Print this page for quick reference!** 📌

**Last Updated**: December 11, 2025
