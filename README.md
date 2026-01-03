# PonoBuilder Shopify Theme

**Version:** 1.0.0
**Author:** PonoBuilder Team
**Description:** Professional e-commerce theme for modular pontoon systems

## 📦 What's Included

A complete, production-ready Shopify theme for PonoBuilder's pontoon product showcase website with:

- ✅ **5 Page Templates**: Homepage, Products, About, How It Works, Quote
- ✅ **Product Catalog**: 6 pontoon products with SKUs, pricing, and specifications
- ✅ **Quote Request Form**: Shopify contact form integration
- ✅ **Responsive Design**: Mobile, tablet, and desktop optimized
- ✅ **Modern Styling**: Compiled Tailwind CSS with clean, professional blue theme
- ✅ **Trust Elements**: Testimonials, stats, warranty badges
- ✅ **Professional Navigation**: Header with mobile menu, comprehensive footer

## 🚀 Installation Instructions

### Step 1: Prepare Your Theme

1. Download or clone this repository
2. **IMPORTANT**: Create a ZIP file of the **shopify-theme folder contents**, not the folder itself

**Correct structure inside the ZIP:**
```
ponobuilder-theme.zip
├── assets/
├── config/
├── layout/
├── locales/
├── sections/
├── templates/
└── README.md
```

**Incorrect structure (don't do this):**
```
ponobuilder-theme.zip
└── shopify-theme/
    ├── assets/
    ├── config/
    └── ...
```

### Step 2: Upload to Shopify

1. Log in to your **Shopify Admin** panel
2. Navigate to: **Online Store** → **Themes**
3. Scroll to the **"Theme library"** section
4. Click **"Add theme"** button
5. Select **"Upload ZIP file"**
6. Choose your `ponobuilder-theme.zip` file
7. Click **"Upload"**
8. Wait for Shopify to process (10-30 seconds)

### Step 3: Preview and Publish

1. Once uploaded, find the theme in your Theme library
2. Click **"Customize"** to preview
3. Check all pages work correctly:
   - Homepage (/)
   - Products (/pages/products)
   - About (/pages/about)
   - How It Works (/pages/how-it-works)
   - Quote (/pages/quote)
4. If everything looks good, click **"Publish"** to make it live

## 📄 Required Shopify Pages

After publishing the theme, you need to create the following pages in Shopify:

### Creating Pages:

1. Go to: **Online Store** → **Pages**
2. Click **"Add page"**
3. Create each of the following:

| Page Title | Template | URL Handle |
|-----------|----------|------------|
| Products | `page.products` | `/pages/products` |
| About | `page.about` | `/pages/about` |
| How It Works | `page.how-it-works` | `/pages/how-it-works` |
| Request Quote | `page.quote` | `/pages/quote` |

**Important:** When creating each page, select the corresponding template from the **"Template"** dropdown on the right side.

## 🎨 Theme Features

### Homepage (index.liquid)
- Hero section with trust badges
- Feature highlights (Marine-Grade Quality, Easy Installation, 10-Year Warranty)
- Benefits section with product advantages
- Customer testimonials
- Call-to-action sections

### Products Page (page.products.liquid)
- 6 Product cards with:
  - Product images (placeholder)
  - SKU numbers
  - Pricing (including sale prices)
  - Feature lists
  - Star ratings and review counts
  - Stock status
  - "Request Quote" buttons
- Benefits section
- Custom configuration CTA

### About Page (page.about.liquid)
- Company story
- Statistics section (2,400+ customers, 14 years, etc.)
- Core values
- Team member profiles

### How It Works Page (page.how-it-works.liquid)
- 6-step process walkthrough:
  1. Initial Consultation
  2. Custom Design
  3. Quote Approval
  4. Manufacturing
  5. Delivery
  6. Installation & Support

### Quote Page (page.quote.liquid)
- Shopify contact form with fields:
  - Name, Email, Phone
  - Company
  - Project Type
  - Budget Range
  - Timeline
  - Project Description
- "What to Expect" information
- Contact details
- Trust badges

## 🔧 Customization

### Colors
The theme uses a blue color scheme. To customize colors, edit `/assets/styles.css`:

```css
/* Primary Blue */
.bg-blue-600 { background-color: rgb(37, 99, 235); }
.bg-blue-700 { background-color: rgb(29, 78, 216); }

/* Update these to your brand colors */
```

### Logo
To add your logo:
1. Go to: **Online Store** → **Themes** → **Customize**
2. Click on **Header** section
3. Upload logo image
4. Adjust logo size as needed

### Contact Information
Update contact details in `/sections/footer.liquid`:
- Email: `info@ponobuilder.com`
- Phone: `(555) 123-4567`
- Hours: `Mon-Fri 8AM-6PM`

### Products
To add real products:
1. Go to: **Products** in Shopify Admin
2. Click **"Add product"**
3. Add product details, images, and pricing
4. Assign SKUs matching those in the theme (e.g., `PON-STD-001`)

## 📱 Responsive Design

The theme is fully responsive across:
- **Mobile** (< 768px): Hamburger menu, stacked layouts
- **Tablet** (768px - 1024px): 2-column grids, optimized spacing
- **Desktop** (> 1024px): 3-column grids, full layouts

## 🎯 Navigation Structure

The theme expects this menu structure:
- Home (/)
- Products (/pages/products)
- About (/pages/about)
- How It Works (/pages/how-it-works)
- Get Quote (/pages/quote)

To set this up:
1. Go to: **Online Store** → **Navigation**
2. Click **"Main menu"**
3. Add the menu items above

## 📧 Contact Form Configuration

The quote form uses Shopify's native contact form. Submissions will:
- Be sent to your Shopify admin email
- Appear in: **Settings** → **Notifications** → **Customer notifications**

To customize email notifications:
1. Go to: **Settings** → **Notifications**
2. Find **"Customer contact"**
3. Customize the email template

## 🐛 Troubleshooting

### Theme shows no styles (white background)
**Solution:** The CSS file is included. If styles don't load:
1. Check that `styles.css` exists in `/assets/` folder
2. Verify the ZIP file structure (see Step 1 above)
3. Try uploading the theme again

### Pages return 404 errors
**Solution:** Pages need to be created in Shopify:
1. Go to: **Online Store** → **Pages**
2. Create pages with the exact URL handles listed above
3. Assign the correct template to each page

### Contact form doesn't work
**Solution:** Make sure:
1. Page template is set to `page.quote`
2. Shopify contact form is enabled
3. Check spam folder for form submissions

### Mobile menu not working
**Solution:** The mobile menu JavaScript is included in `theme.liquid`. Clear browser cache and reload.

## 📊 Theme File Structure

```
shopify-theme/
├── assets/
│   └── styles.css           # Compiled Tailwind CSS (all styles)
├── config/
│   ├── settings_schema.json # Theme settings
│   └── settings_data.json   # Default settings
├── layout/
│   └── theme.liquid         # Main layout wrapper
├── locales/
│   └── en.default.json      # English translations
├── sections/
│   ├── header.liquid        # Site header + navigation
│   └── footer.liquid        # Site footer
├── templates/
│   ├── index.liquid         # Homepage template
│   ├── page.about.liquid    # About page
│   ├── page.how-it-works.liquid  # How It Works page
│   ├── page.products.liquid      # Products page
│   └── page.quote.liquid         # Quote request page
└── README.md                # This file
```

## 📈 Next Steps After Installation

1. **Add Product Images**: Replace placeholder images with real product photos
2. **Update Content**: Customize text, testimonials, and company information
3. **Configure SEO**: Add meta descriptions and titles in page settings
4. **Set Up Analytics**: Add Google Analytics or Shopify Analytics
5. **Test Contact Form**: Submit a test quote to verify email delivery
6. **Mobile Testing**: Test all pages on mobile devices
7. **SSL Certificate**: Ensure HTTPS is enabled in Shopify

## 🔒 Security Notes

- Never commit API keys or credentials to the theme
- Keep Shopify admin password secure
- Enable two-factor authentication on Shopify account
- Regularly backup your Shopify store

## 📞 Support

For theme support:
- **Email:** support@ponobuilder.com
- **Phone:** (555) 123-4567
- **Documentation:** https://ponobuilder.com/docs

## 📝 Version History

**v1.0.0** (Current)
- Initial release
- Complete homepage, products, about, how-it-works, and quote pages
- Responsive design with mobile navigation
- Shopify contact form integration
- Compiled Tailwind CSS styling

## ⚖️ License

Copyright © 2024 PonoBuilder. All rights reserved.

---

**Built with care for PonoBuilder** 🚤
