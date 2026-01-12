# Piritha N - Portfolio Website

A modern, colorful, and responsive portfolio website with dark/light theme toggle and contact form functionality.

## Features

✨ **Modern Design**
- Beautiful gradient color schemes
- Smooth animations and transitions
- Responsive design for all devices

🌓 **Theme Toggle**
- Dark and light mode support
- Theme preference saved in localStorage
- Smooth theme transitions

📧 **Contact Form**
- Direct email functionality using EmailJS (optional)
- Fallback to mailto link if EmailJS not configured
- Form validation and user feedback

📱 **Fully Responsive**
- Mobile-first design
- Hamburger menu for mobile devices
- Optimized for tablets and desktops

## Setup Instructions

### 1. Basic Setup

Simply open `index.html` in your web browser or host it on any web server.

### 2. EmailJS Setup (Optional - for direct email functionality)

The contact form is currently configured to use a mailto fallback. To enable direct email sending:

1. **Create an EmailJS Account**
   - Go to [https://www.emailjs.com/](https://www.emailjs.com/)
   - Sign up for a free account (allows 200 emails/month)

2. **Create an Email Service**
   - Go to "Email Services" in your dashboard
   - Add a new service (Gmail recommended)
   - Follow the setup instructions
   - Note your **Service ID**

3. **Create an Email Template**
   - Go to "Email Templates"
   - Create a new template
   - Use these variables in your template:
     - `{{to_email}}` - Recipient email (piri.nags15@gmail.com)
     - `{{from_name}}` - Sender's name
     - `{{from_email}}` - Sender's email
     - `{{subject}}` - Email subject
     - `{{message}}` - Email message
   - Note your **Template ID**

4. **Get Your Public Key**
   - Go to "Account" → "General"
   - Copy your **Public Key**

5. **Update script.js**
   - Open `script.js`
   - Find the `EMAILJS_CONFIG` object (around line 94)
   - Replace the placeholder values:
     ```javascript
     const EMAILJS_CONFIG = {
         PUBLIC_KEY: 'your_public_key_here',
         SERVICE_ID: 'your_service_id_here',
         TEMPLATE_ID: 'your_template_id_here'
     };
     ```

6. **Test the Form**
   - Submit a test message
   - Check your email (piri.nags15@gmail.com)
   - Verify the message was received

### 3. Alternative: Use FormSpree (Another Option)

If you prefer FormSpree instead of EmailJS:

1. Sign up at [https://formspree.io/](https://formspree.io/)
2. Create a new form and get your form endpoint
3. Update the form action in `index.html`:
   ```html
   <form id="contactForm" class="contact-form" action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
   ```

## Customization

### Changing Colors

Edit the CSS variables in `styles.css` (lines 1-31):

```css
:root {
    --accent-1: #6366f1;  /* Primary accent color */
    --accent-2: #8b5cf6;  /* Secondary accent color */
    --accent-3: #ec4899;  /* Tertiary accent color */
    /* ... more colors ... */
}
```

### Updating Content

- Edit `index.html` to update your information
- Modify section content, projects, skills, etc.
- Update social media links and contact information

### Adding New Sections

1. Add HTML section in `index.html`
2. Add corresponding CSS styles in `styles.css`
3. Update navigation menu if needed

## File Structure

```
portfolio/
├── index.html      # Main HTML file
├── styles.css      # All CSS styles
├── script.js       # JavaScript functionality
└── README.md       # This file
```

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## License

This portfolio is open source and available for personal use.

## Contact

**Piritha N**
- Email: piri.nags15@gmail.com
- Phone: 9176463644
- Location: Chennai, Tamil Nadu
- LinkedIn: [linkedin.com/in/piritha-n-693483218](https://linkedin.com/in/piritha-n-693483218)
- GitHub: [github.com/Piritha-15](https://github.com/Piritha-15)

---

Built with ❤️ using HTML, CSS, and JavaScript

