# Nurture Sync Website

A modern, professional healthcare website for Nurture Sync - a revolutionary healthcare app that provides digital health profiles, AI-powered features, and a community platform for doctors and patients.

## 🚀 Quick Start

### Running Locally

Simply open `index.html` in your web browser, or use a local server:

```bash
# Using Python
python -m http.server 8000

# Using Node.js (npx)
npx serve .

# Using PHP
php -S localhost:8000
```

Then open `http://localhost:8000` in your browser.

## 📁 Project Structure

```
Webapp/
├── index.html              # Home page
├── services.html           # Services page with tabs
├── team.html               # Team page
├── testimonials.html       # Testimonials with videos
├── contact.html            # Contact form with EmailJS
├── css/
│   └── style.css           # Main stylesheet
├── js/
│   └── main.js             # JavaScript functionality
├── Images/                 # Partner/testimonial images
├── videos/                 # Testimonial videos
├── team/                   # Team member photos
├── Nurture sync logo.png   # Logo
└── README.md               # This file
```

## 📧 Setting Up Email (Contact Form)

The contact form uses EmailJS to send emails directly to knandini7816@gmail.com.

### Steps to Configure:

1. **Go to [EmailJS.com](https://www.emailjs.com/)** and sign in with `knandini7816@gmail.com`

2. **Create an Email Service:**
   - Click "Email Services" → "Add New Service"
   - Choose "Gmail" and connect your account
   - Note the **Service ID** (e.g., `service_abc123`)

3. **Create an Email Template:**
   - Click "Email Templates" → "Create New Template"
   - Use this template:
   ```
   Subject: {{subject}} - New Contact from Nurture Sync Website
   
   Name: {{from_name}}
   Email: {{from_email}}
   Phone: {{phone}}
   
   Message:
   {{message}}
   ```
   - Note the **Template ID** (e.g., `template_xyz789`)

4. **Get Your Public Key:**
   - Go to "Account" → "API Keys"
   - Copy your **Public Key**

5. **Update contact.html:**
   - Open `contact.html`
   - Find and replace these placeholders:
   ```javascript
   emailjs.init('YOUR_PUBLIC_KEY');        // Line ~182
   emailjs.send('YOUR_SERVICE_ID', 'YOUR_TEMPLATE_ID', templateParams)  // Line ~199
   ```

## 🚀 Deployment Options

### Option 1: Netlify (Recommended - Free)

**Via Netlify CLI:**
```bash
# Install Netlify CLI
npm install -g netlify-cli

# Login to Netlify
netlify login

# Deploy
cd /path/to/Webapp
netlify deploy --prod --dir .
```

**Via Drag & Drop:**
1. Go to [app.netlify.com](https://app.netlify.com)
2. Drag the entire `Webapp` folder to the deployment area
3. Your site will be live instantly!

### Option 2: GitHub Pages (Free)

1. Create a GitHub repository
2. Push all files:
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git remote add origin https://github.com/YOUR_USERNAME/nurture-sync.git
   git push -u origin main
   ```
3. Go to Repository Settings → Pages
4. Select "Deploy from a branch" → "main" → "/ (root)"
5. Access at `https://YOUR_USERNAME.github.io/nurture-sync`

### Option 3: Vercel (Free)

```bash
# Install Vercel CLI
npm install -g vercel

# Deploy
cd /path/to/Webapp
vercel --prod
```

### Option 4: Traditional Web Hosting

Simply upload all files via FTP to your web host's `public_html` folder.

## 🖼️ Adding Team Photos

To add real team photos:

1. Create individual photos for each team member
2. Save them in the `team/` folder as:
   - `team/nandini.png`
   - `team/vishal.png`
   - `team/sarvesh.png`
   - `team/pranesh.png`
3. Photos will automatically appear on the Team page

*Currently, fallback avatars are displayed if photos are not found.*

## 🎨 Customization

### Colors
Edit `css/style.css` and modify the CSS custom properties at the top:
```css
:root {
  --primary-500: #009688;  /* Main teal color */
  --primary-600: #00897b;
  --accent-cyan: #00bcd4;
  /* ... more colors */
}
```

### Content
- Edit HTML files directly to change text content
- Images are in the `Images/` folder
- Videos are in the `videos/` folder

## 📱 Features

- ✅ Fully responsive design (mobile, tablet, desktop)
- ✅ Modern animations and transitions
- ✅ Glassmorphism UI effects
- ✅ Interactive service tabs
- ✅ Video testimonials with play controls
- ✅ Image gallery with hover effects
- ✅ Contact form with EmailJS integration
- ✅ Scroll animations
- ✅ Mobile hamburger menu
- ✅ Scroll-to-top button
- ✅ SEO optimized

## 🤝 Support

For questions or support, contact:
- **Email:** knandini7816@gmail.com

---

© 2026 Nurture Sync. All rights reserved.
