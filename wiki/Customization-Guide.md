# Customization Guide

Learn how to customize your Personal Profile Card to match your personal brand and information.

## 🎨 Quick Customization Checklist

- [ ] Replace profile images
- [ ] Update personal information
- [ ] Modify social media links
- [ ] Customize color scheme
- [ ] Update statistics
- [ ] Add/remove skill tags
- [ ] Adjust platform icons

## 👤 Personal Information

### 1. Name and Username
**File**: `index.html`
```html
<!-- Change your name -->
<h2 class="name">Your Name <span class="verified">✔</span></h2>

<!-- Change your username -->
<p class="username">@your_username</p>
```

### 2. Profile Images

#### Main Avatar
**File**: `index.html`
```html
<img src="Pictures/your-avatar.jpg" class="avatar" />
```
- **Recommended size**: 120px × 120px minimum
- **Format**: JPG, PNG, or WebP
- **Aspect ratio**: Square (1:1)

#### Badge/Logo
**File**: `index.html`
```html
<img src="Pictures/your-badge.png" class="badge" />
```
- **Recommended size**: 30px × 30px minimum
- **Format**: PNG (for transparency)
- **Purpose**: Company logo, certification, or personal brand

## 📊 Statistics Section

### Updating Your Stats
**File**: `index.html`
```html
<div class="stats">
    <div class="stat-box">
        <p class="label orange">Your Metric</p>
        <p class="value">Your Number</p>
    </div>
    <div class="stat-box">
        <p class="label green">Another Metric</p>
        <p class="value">Another Number</p>
    </div>
</div>
```

### Popular Coding Statistics:
- Questions Solved
- Active Days
- Contest Rating
- Repositories
- Contributions
- Followers
- Projects Completed
- Years of Experience

## 🔗 Social Media Links

### LinkedIn Section
**File**: `index.html`
```html
<p>You can find me on 
    <a class="linkedin" href="YOUR_LINKEDIN_URL" target="_blank">
        <img src="Pictures/LinkedInImage.png" alt="LinkedIn"/>
    </a>
</p>
```

### Platform Icons
**File**: `index.html`
```html
<div class="icons">
    <a href="YOUR_PLATFORM_URL" target="_blank">
        <img src="Pictures/your-icon.png" alt="Platform Name"/>
    </a>
    <!-- Repeat for each platform -->
</div>
```

### Supported Platforms (with existing icons):
- GeeksforGeeks
- HackerRank  
- Coding Ninjas
- AtCoder
- Codeforces
- CodeChef
- LeetCode

## 🏷️ Skill Tags

### Modifying Tags
**File**: `index.html`
```html
<div class="tags stat-box">
    <span>#YOUR_SKILL</span>
    <span>#ANOTHER_SKILL</span>
    <!-- Add more tags -->
</div>
```

### Popular Tag Categories:

#### Programming Languages:
- `#JAVA`, `#PYTHON`, `#C++`, `#JAVASCRIPT`
- `#TYPESCRIPT`, `#GO`, `#RUST`, `#C#`

#### Frameworks & Libraries:
- `#REACT`, `#ANGULAR`, `#VUE`, `#NODEJS`
- `#SPRING`, `#DJANGO`, `#FLASK`, `#EXPRESS`

#### Technologies:
- `#DSA`, `#ALGORITHMS`, `#DATABASE`, `#CLOUD`
- `#AWS`, `#DOCKER`, `#KUBERNETES`, `#GIT`

#### Achievements:
- `#5STARS`, `#EXPERT`, `#SPECIALIST`, `#PUPIL`
- `#KNIGHT`, `#GUARDIAN`, `#WARRIOR`, `#MASTER`

## 🎨 Color Scheme Customization

### Main Colors
**File**: `styles.css`
```css
:root {
    --bg-color: #000;           /* Page background */
    --card-bg: #141416;         /* Card background */
    --text-primary: #fff;       /* Main text */
    --text-secondary: #aaa;     /* Secondary text */
    --accent-orange: #f59e55;   /* Orange accent */
    --accent-green: #2ecc71;    /* Green accent */
    --border-color: #2e2e32;    /* Border color */
}
```

### Pre-made Color Schemes:

#### Blue Theme:
```css
--accent-orange: #3498db;   /* Blue primary */
--accent-green: #1abc9c;    /* Teal secondary */
```

#### Purple Theme:
```css
--accent-orange: #9b59b6;   /* Purple primary */
--accent-green: #e74c3c;    /* Red secondary */
```

#### Minimal Theme:
```css
--accent-orange: #ffffff;   /* White primary */
--accent-green: #888888;    /* Gray secondary */
```

## 🖼️ Image Optimization

### Image Guidelines:
- **Profile Avatar**: 240px × 240px (displayed at 120px for retina)
- **Badge**: 60px × 60px (displayed at 30px for retina)
- **Platform Icons**: 48px × 48px (displayed at 28px for retina)

### File Size Optimization:
- **JPG**: For photos (profile avatar)
- **PNG**: For graphics with transparency (badges, icons)
- **WebP**: Modern format for better compression
- **Target size**: < 50KB per image

### Tools for Optimization:
- **TinyPNG**: Online PNG/JPG compression
- **GIMP**: Free image editor
- **Canva**: Design tool for creating badges
- **Unsplash**: Free high-quality photos

## 📱 Responsive Considerations

### Mobile-First Approach:
The card is designed to work on all devices, but consider:

```css
/* Custom mobile adjustments */
@media (max-width: 480px) {
    .card {
        max-width: 300px;
        padding: 15px;
    }
    
    .avatar {
        width: 100px;
        height: 100px;
    }
}
```

## 🔧 Advanced Customization

### Adding New Sections:
```html
<div class="custom-section stat-box">
    <h3>Your Section Title</h3>
    <p>Your content here</p>
</div>
```

### Custom Animations:
```css
.custom-element {
    animation: customAnimation 2s ease-in-out infinite;
}

@keyframes customAnimation {
    0% { transform: scale(1); }
    50% { transform: scale(1.05); }
    100% { transform: scale(1); }
}
```

## ✅ Testing Your Changes

After customization:
1. **Validate HTML**: Use W3C HTML Validator
2. **Test responsiveness**: Check on different screen sizes
3. **Verify links**: Ensure all social links work
4. **Image loading**: Confirm all images display properly
5. **Browser compatibility**: Test in multiple browsers

---

**Related Pages**: 
- [Color Schemes](Color-Schemes.md)
- [Profile Images Guide](Profile-Images.md)
- [Adding Platforms](Adding-Platforms.md)
