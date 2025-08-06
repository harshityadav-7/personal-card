# HTML Structure Documentation

This page provides a detailed breakdown of the HTML structure used in the Personal Profile Card.

## 🏗️ Overall Structure

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <!-- Meta and styling -->
</head>
<body>
    <div class="card">
        <!-- All content -->
    </div>
</body>
</html>
```

## 📋 Detailed Breakdown

### 1. Document Head
```html
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Personal Card</title>
    <link rel="stylesheet" href="styles.css" />
</head>
```
- **UTF-8 charset**: Supports international characters
- **Viewport meta**: Ensures proper mobile rendering
- **Title**: Browser tab title
- **Stylesheet link**: Connects to CSS file

### 2. Main Card Container
```html
<div class="card">
    <!-- All card content -->
</div>
```
- **Purpose**: Main wrapper for the entire profile card
- **Styling**: Dark theme, rounded corners, shadows, animations

### 3. SVG Background Animation
```html
<svg class="web-lines" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1000 1000" preserveAspectRatio="xMidYMid slice">
    <!-- Circles -->
    <circle cx="500" cy="500" r="100" stroke="#eeeeee22" stroke-width="1" fill="none"/>
    <circle cx="500" cy="500" r="200" stroke="#eeeeee22" stroke-width="1" fill="none"/>
    <!-- ... more circles -->
    
    <!-- Radial Lines -->
    <line x1="500" y1="0" x2="500" y2="1000" stroke="#eeeeee22" stroke-width="1"/>
    <!-- ... more lines -->
</svg>
```

#### SVG Components:
- **5 Concentric circles**: Create web-like pattern (100px to 500px radius)
- **8 Radial lines**: Vertical, horizontal, and diagonal lines
- **Low opacity stroke**: `#eeeeee22` for subtle visibility
- **CSS Animation**: 360° rotation over 120 seconds

### 4. Header Section
```html
<div class="header">
    <h1><span class="brand">Perso</span><span class="highlight">nal</span></h1>
    <h1>CARD</h1>
</div>
```
- **Brand styling**: "Perso" in white, "nal" in orange
- **Typography**: Bold, prominent title

### 5. Profile Section
```html
<div class="profile">
    <img src="Pictures/iron man.jpg" class="avatar" />
    <img src="Pictures/CololioLogoImage.png" class="badge" />
</div>
```
- **Avatar**: Main profile picture (120px circular)
- **Badge**: Small overlay icon (30px circular)
- **Positioning**: Badge positioned relative to avatar

### 6. User Information
```html
<h2 class="name">Harshit Yadav <span class="verified">✔</span></h2>
<p class="username">@harshityadav_7</p>
```
- **Name**: Primary heading with verification checkmark
- **Username**: Styled as a badge with background color

### 7. Statistics Section
```html
<div class="stats">
    <div class="stat-box">
        <p class="label orange">Questions Solved</p>
        <p class="value">2065</p>
    </div>
    <div class="stat-box">
        <p class="label green">Active Days</p>
        <p class="value">317</p>
    </div>
</div>
```
- **Flexbox layout**: Two equal-width stat boxes
- **Color coding**: Orange for questions, green for days
- **Typography**: Small labels, large values

### 8. Social Media Section
```html
<div class="social stat-box">
    <p>You can find me on 
        <a class="linkedin" href="https://www.linkedin.com/in/harshit-yadav-7/" target="_blank">
            <img src="Pictures/LinkedInImage.png" alt="LinkedIn"/>
        </a>
    </p>
    <div class="icons">
        <!-- 7 coding platform links with icons -->
    </div>
</div>
```

#### Platform Links Structure:
```html
<a href="PLATFORM_URL" target="_blank">
    <img src="Pictures/ICON_FILE" alt="PLATFORM_NAME"/>
</a>
```

### 9. Skills Tags Section
```html
<div class="tags stat-box">
    <span>#JAVA</span>
    <span>#C++</span>
    <span>#2STARS</span>
    <span>#DSA</span>
    <span>#NEWBIE</span>
    <span>#KNIGHT</span>
</div>
```
- **Flexbox wrap**: Tags flow naturally
- **Hashtag format**: Technology and achievement tags

## 🔧 Semantic HTML Features

### Accessibility:
- **Alt text**: All images have descriptive alt attributes
- **Semantic elements**: Proper use of h1, h2, p elements
- **Link targets**: External links open in new tabs

### SEO Optimization:
- **Proper heading hierarchy**: h1 for title, h2 for name
- **Descriptive alt text**: Improves image SEO
- **Clean structure**: Search engine friendly

## 🎨 CSS Classes Reference

| Class | Purpose | Element |
|-------|---------|---------|
| `.card` | Main container | `<div>` |
| `.web-lines` | Background animation | `<svg>` |
| `.header` | Title section | `<div>` |
| `.brand` | "Perso" styling | `<span>` |
| `.highlight` | "nal" orange styling | `<span>` |
| `.profile` | Avatar container | `<div>` |
| `.avatar` | Profile image | `<img>` |
| `.badge` | Badge overlay | `<img>` |
| `.name` | User name | `<h2>` |
| `.verified` | Checkmark | `<span>` |
| `.username` | Handle styling | `<p>` |
| `.stats` | Statistics container | `<div>` |
| `.stat-box` | Individual stat/section | `<div>` |
| `.label` | Stat labels | `<p>` |
| `.value` | Stat values | `<p>` |
| `.orange` | Orange color | `<p>` |
| `.green` | Green color | `<p>` |
| `.social` | Social media section | `<div>` |
| `.linkedin` | LinkedIn link | `<a>` |
| `.icons` | Platform icons container | `<div>` |
| `.tags` | Skills tags container | `<div>` |

---

**Related Pages**: 
- [CSS Styling Documentation](CSS-Styling.md)
- [SVG Animation Details](SVG-Animation.md)
- [Customization Guide](Customization-Guide.md)
