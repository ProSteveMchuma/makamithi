# Image Upload Guide - Makamithi Website

## 📸 Required Images & Locations

### 1. **LOGO (High Priority)** 🔴
**Location:** `/workspaces/makamithi/assets/logos/`

**Files Needed:**
- `makamithi-logo.png` - Main logo (recommended: 400x100px, transparent background)
- `makamithi-logo-white.png` - White version for dark backgrounds
- `makamithi-icon.png` - Icon only (192x192px for PWA)
- `makamithi-icon-512.png` - Larger icon (512x512px for PWA)
- `favicon.ico` - Browser favicon (32x32px)
- `favicon-16x16.png` - Small favicon
- `favicon-32x32.png` - Standard favicon
- `apple-touch-icon.png` - Apple devices (180x180px)

**Where Used:**
- Website header (sidebar & top navigation)
- Browser tab (favicon)
- Mobile app icon (PWA)
- Footer
- Social media sharing (Open Graph)

---

### 2. **HERO SECTION**
**Location:** `/workspaces/makamithi/assets/images/`

**Files Needed:**
- `hero-background.jpg` - Main hero image (1920x1080px recommended)

**Suggestions:**
- Wide shot of Makamithi main store/warehouse
- Team members serving customers
- Well-stocked shelves with products
- Farmers with Makamithi products

**Current:** Using Unsplash placeholder
**Replace in:** Line ~1886 of index.html

---

### 3. **ABOUT SECTION**
**Location:** `/workspaces/makamithi/assets/images/`

**Files Needed:**
- `about-main.jpg` - Main branch photo (1200x800px)
- `about-vision.jpg` - Vision card image (800x800px)
- `about-mission.jpg` - Mission card image (800x800px)
- `warehouse.jpg` - Optional: warehouse/logistics photo
- `team-photo.jpg` - Optional: team group photo

**Suggestions:**
- Actual Makamithi Machakos branch exterior
- Inside store showing product displays
- Warehouse with organized inventory
- Team members (agronomists, sales staff)

**Current:** Using Unsplash placeholders
**Replace in:** Lines ~1923, 1939, 1945 of index.html

---

### 4. **PRODUCTS (5 Images)**
**Location:** `/workspaces/makamithi/assets/products/`

**Files Needed:**
- `animal-feeds.jpg` - Animal feeds display (800x600px)
- `fertilizers.jpg` - Fertilizers/soil amendments (800x600px)
- `seeds.jpg` - Seed packets/varieties (800x600px)
- `crop-protection.jpg` - Pesticides/herbicides (800x600px)
- `veterinary.jpg` - Veterinary products (800x600px)

**Suggestions:**
- Take photos of actual products in your store
- Show branded packaging (Bayer, Syngenta, etc.)
- Well-lit product displays
- Multiple products per category if possible

**Current:** Using Unsplash placeholders
**Replace in:** Lines ~1963, 1976, 1989, 2002, 2015 of index.html

---

### 5. **PARTNER LOGOS (8+ Images)**
**Location:** `/workspaces/makamithi/assets/partners/`

**Files Needed:**
- `bayer.png` - ✅ Already uploaded
- `syngenta.png` - ✅ Already uploaded
- `partner-3.png` - Add real partner logo
- `partner-4.png` - Add real partner logo
- `partner-5.png` - Add real partner logo
- `partner-6.png` - Add real partner logo
- `partner-7.png` - Add real partner logo
- `partner-8.png` - Add real partner logo

**Recommended Size:** 200x100px, transparent PNG

**Possible Partners:**
- East African Seed Company
- Yara (fertilizers)
- Corteva Agriscience
- BASF
- UPL Limited
- Osho Chemical
- Elgon Kenya
- Coopers K-Brands

**Current:** 6 placeholders exist
**Replace in:** Lines ~2028-2043 of index.html

---

### 6. **LOCATION PHOTOS (6 Images)**
**Location:** `/workspaces/makamithi/assets/locations/`

**Files Needed:**
- `main-shop-machakos.jpg` - Main Shop exterior
- `annex-shop-machakos.jpg` - Annex Shop exterior
- `bus-park-machakos.jpg` - Bus Park location
- `emali-shop.jpg` - Emali branch
- `wote-shop.jpg` - Wote branch
- `kitui-shop.jpg` - Kitui branch

**Recommended Size:** 800x600px

**Usage:** Will be added to location cards in Contact section

---

### 7. **TESTIMONIAL PHOTOS (Optional but Recommended)**
**Location:** `/workspaces/makamithi/assets/testimonials/`

**Files Needed:**
- `customer-1.jpg` - Farmer testimonial photo (300x300px)
- `customer-2.jpg` - Farmer testimonial photo
- `customer-3.jpg` - Farmer testimonial photo
- `customer-4.jpg` - Farmer testimonial photo

**Suggestions:**
- Photos of happy customers/farmers
- Get written consent for using photos
- Include names and locations in testimonials

---

## 🔧 How to Upload Images

### Method 1: VS Code Upload (Easiest)
1. Open VS Code file explorer
2. Navigate to the target folder (e.g., `/assets/logos/`)
3. Drag and drop your images into the folder
4. Images will automatically upload

### Method 2: Terminal Command
```bash
# Upload single file
cd /workspaces/makamithi/assets/logos
# Then drag file or use upload command

# Or copy from local machine
scp /path/to/local/image.png user@server:/workspaces/makamithi/assets/logos/
```

### Method 3: Git Upload
```bash
# Add images
git add assets/logos/*.png
git commit -m "Add company logos"
git push origin main
```

---

## 📝 After Uploading Images

### Update HTML References

**1. Logo Updates:**
Replace line ~48 and other logo references:
```html
<!-- OLD -->
<meta property="og:image" content="...logos/makamithi.png">

<!-- NEW -->
<meta property="og:image" content="https://makamithi.inspirehub.co.ke/assets/logos/makamithi-logo.png">
```

**2. Hero Image:**
Replace line ~1886:
```html
<!-- OLD -->
<img src="https://images.unsplash.com/photo-..." alt="...">

<!-- NEW -->
<img src="assets/images/hero-background.jpg" alt="Makamithi Agro Store - Serving farmers with quality agricultural products">
```

**3. About Images:**
Replace lines ~1923, 1939, 1945:
```html
<!-- OLD -->
<img src="https://images.unsplash.com/..." alt="...">

<!-- NEW -->
<img src="assets/images/about-main.jpg" alt="Our main branch in Machakos, Kenya">
```

**4. Product Images:**
Replace lines ~1963-2015:
```html
<!-- OLD -->
<img src="https://images.unsplash.com/..." alt="Animal Feeds">

<!-- NEW -->
<img src="assets/products/animal-feeds.jpg" alt="Premium Animal Feeds - Makamithi">
```

**5. Partner Logos:**
Replace lines ~2028-2043:
```html
<!-- OLD -->
<div class="partner-logo">Partner 1</div>

<!-- NEW -->
<div class="partner-logo">
    <img src="assets/partners/partner-name.png" alt="Partner Name">
</div>
```

---

## 🎨 Image Optimization Tips

### Before Uploading:
1. **Resize images** to recommended dimensions
2. **Compress images** using:
   - TinyPNG (https://tinypng.com/)
   - Squoosh (https://squoosh.app/)
   - ImageOptim (Mac)
   
3. **Convert to WebP** for better performance (optional):
   ```bash
   # Using cwebp command
   cwebp hero-background.jpg -q 80 -o hero-background.webp
   ```

4. **File naming conventions:**
   - Use lowercase
   - Use hyphens (not spaces or underscores)
   - Be descriptive: `main-shop-exterior.jpg` not `IMG_1234.jpg`

### Target File Sizes:
- **Logo:** < 50KB
- **Hero image:** < 200KB
- **Product images:** < 150KB each
- **About images:** < 150KB each
- **Partner logos:** < 30KB each

---

## ✅ Quick Checklist

### Phase 1: Essential (Do First)
- [ ] Company logo (PNG with transparent background)
- [ ] Favicon set (16x16, 32x32)
- [ ] PWA icons (192x192, 512x512)
- [ ] Hero background image
- [ ] Main branch photo (for About section)

### Phase 2: Important (Do Soon)
- [ ] 5 product category images
- [ ] All 8 partner logos
- [ ] 2-3 additional About section images

### Phase 3: Nice to Have
- [ ] 6 location photos (one per branch)
- [ ] 3-4 customer testimonial photos
- [ ] Team member photos
- [ ] Warehouse/logistics photos

---

## 🚀 I'll Help You Update

Once you upload the images, let me know and I'll:
1. ✅ Update all HTML references
2. ✅ Add proper alt text for SEO
3. ✅ Implement lazy loading
4. ✅ Add image optimization code
5. ✅ Update PWA manifest with new icons
6. ✅ Test all image paths

---

## 📞 Need Help?

**Common Issues:**
- **Images not showing:** Check file paths and names match exactly
- **Images too large:** Use TinyPNG to compress before uploading
- **Wrong size:** Use online resizers or Photoshop/GIMP

**What to provide:**
Just upload the images to the correct folders, and I'll handle all the HTML updates automatically!

---

## 🎯 Priority Order

1. **URGENT:** Logo + Favicon (impacts brand identity immediately)
2. **HIGH:** Product images (improves product section credibility)
3. **MEDIUM:** About section images (builds trust)
4. **LOW:** Location photos (nice to have, can add later)

Ready to upload? Drop your images in the folders and let me know! 🚀
