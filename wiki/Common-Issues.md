# Common Issues & Troubleshooting

This page covers the most frequently encountered issues and their solutions.

## 🚨 Quick Fixes

### Images Not Displaying
**Symptoms**: Broken image icons, alt text showing instead of images

**Causes & Solutions**:
1. **Incorrect file path**
   ```html
   <!-- ❌ Wrong -->
   <img src="pictures/avatar.jpg" />
   
   <!-- ✅ Correct -->
   <img src="Pictures/iron man.jpg" />
   ```

2. **Case sensitivity** (especially on Linux/GitHub Pages)
   - File: `iron man.jpg`
   - HTML must match exactly: `Pictures/iron man.jpg`

3. **Missing files**
   - Check all files exist in `Pictures/` folder
   - Verify file extensions (.jpg, .png, .jpeg)

4. **File permissions**
   - Ensure files are readable
   - Check repository privacy settings

### CSS Styles Not Applied
**Symptoms**: Plain HTML with no styling, default browser fonts

**Solutions**:
1. **Check CSS file location**
   ```html
   <!-- CSS file must be in same directory as index.html -->
   <link rel="stylesheet" href="styles.css" />
   ```

2. **Verify CSS file exists**
   - Confirm `styles.css` is present
   - Check for typos in filename

3. **Browser caching**
   - Hard refresh: `Ctrl + F5` (Windows) or `Cmd + Shift + R` (Mac)
   - Clear browser cache

4. **Server issues** (local development)
   - Use proper local server instead of file:// protocol
   - Try VS Code Live Server extension

### Animation Not Working
**Symptoms**: Static background, no rotation

**Solutions**:
1. **Browser compatibility**
   - Update to modern browser version
   - Chrome, Firefox, Safari, Edge supported

2. **Hardware acceleration**
   - Enable in browser settings
   - Check graphics drivers are updated

3. **Reduced motion settings**
   ```css
   /* Respect user's motion preferences */
   @media (prefers-reduced-motion: reduce) {
     .web-lines {
       animation: none;
     }
   }
   ```

### Links Not Working
**Symptoms**: Clicking platform icons does nothing, or 404 errors

**Solutions**:
1. **Check URL format**
   ```html
   <!-- ✅ Include https:// -->
   <a href="https://github.com/username" target="_blank">
   
   <!-- ❌ Missing protocol -->
   <a href="github.com/username" target="_blank">
   ```

2. **Verify social media URLs**
   - Test links manually in browser
   - Check for typos in usernames

3. **Target attribute**
   ```html
   <!-- Opens in new tab -->
   <a href="URL" target="_blank">
   ```

## 📱 Mobile & Responsive Issues

### Card Too Wide on Mobile
**Solution**: Add viewport meta tag
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
```

### Text Too Small
**Solution**: Adjust mobile-specific CSS
```css
@media (max-width: 480px) {
    .name {
        font-size: 18px;
    }
    .username {
        font-size: 12px;
    }
}
```

### Images Pixelated
**Solution**: Use high-resolution images
- 2x size for retina displays
- Example: 240px image displayed at 120px

## 🌐 Deployment Issues

### GitHub Pages Not Updating
**Solutions**:
1. **Check Actions tab** for build errors
2. **Wait 5-10 minutes** for changes to propagate
3. **Clear browser cache** for the GitHub Pages URL
4. **Verify branch settings** in repository settings

### 404 on GitHub Pages
**Solutions**:
1. **Ensure `index.html` is in root directory**
2. **Check repository is public** (for free GitHub Pages)
3. **Verify Pages settings** are configured correctly

### Custom Domain Issues
**Solutions**:
1. **DNS propagation**: Wait 24-48 hours for DNS changes
2. **CNAME file**: Must contain only your domain name
3. **HTTPS certificate**: May take time to provision

## 🎨 Design & Layout Issues

### Badge Positioning Wrong
**Problem**: Badge overlay not aligned with avatar

**Solution**: Adjust CSS positioning
```css
.badge {
    position: relative;
    bottom: 20px;      /* Adjust vertical position */
    right: 36px;       /* Adjust horizontal position */
}
```

### Stats Boxes Uneven
**Problem**: Statistics boxes different heights

**Solution**: Use flexbox alignment
```css
.stats {
    display: flex;
    align-items: stretch;  /* Makes boxes equal height */
}
```

### Text Overflow
**Problem**: Long usernames or names breaking layout

**Solution**: Add text overflow handling
```css
.username {
    max-width: 200px;
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
}
```

## 🔧 Performance Issues

### Slow Loading
**Solutions**:
1. **Optimize images**:
   - Compress images (TinyPNG, ImageOptim)
   - Use WebP format when supported
   - Add `loading="lazy"` to images

2. **Minify CSS**:
   - Remove unnecessary whitespace and comments
   - Combine CSS rules where possible

### Memory Issues
**Problem**: High RAM usage due to animation

**Solution**: Optimize SVG animation
```css
.web-lines {
    /* Use transform instead of changing properties */
    animation: rotateWeb 120s linear infinite;
    /* Add will-change for better performance */
    will-change: transform;
}
```

## 🐛 Browser-Specific Issues

### Internet Explorer
**Problems**: Limited CSS support, no SVG animation
**Solution**: Add IE detection and fallbacks
```css
/* IE fallback */
.no-svg .web-lines {
    display: none;
}
```

### Safari
**Problem**: Some CSS properties not supported
**Solution**: Add vendor prefixes
```css
.card {
    -webkit-border-radius: 20px;
    border-radius: 20px;
}
```

## 📊 Validation Errors

### HTML Validation
**Common errors**:
- Missing alt attributes on images
- Unclosed tags
- Invalid nesting

**Solution**: Use [W3C HTML Validator](https://validator.w3.org/)

### CSS Validation
**Common errors**:
- Unknown property values
- Missing semicolons
- Invalid selectors

**Solution**: Use [W3C CSS Validator](https://jigsaw.w3.org/css-validator/)

## 🔍 Debugging Steps

### 1. Browser Developer Tools
- **Console tab**: Check for JavaScript errors
- **Network tab**: See failed resource loads
- **Elements tab**: Inspect HTML/CSS

### 2. Step-by-Step Isolation
1. Test with fresh browser profile
2. Disable browser extensions
3. Try incognito/private mode
4. Test on different device

### 3. Code Validation
1. Validate HTML structure
2. Check CSS syntax
3. Verify file paths
4. Test in local environment first

## 🆘 Getting Help

### When to Seek Help:
- Tried all troubleshooting steps
- Issue persists across multiple browsers
- Deployment problems continue after 24 hours

### How to Report Issues:
1. **Describe the problem clearly**
2. **Include your environment**:
   - Operating System
   - Browser and version
   - Device type
3. **Provide steps to reproduce**
4. **Share error messages**
5. **Include relevant code snippets**

### Support Channels:
- [GitHub Issues](https://github.com/harshityadav-7/personal-card/issues)
- [Stack Overflow](https://stackoverflow.com/questions/tagged/html+css)
- Web development communities

---

**Related Pages**: 
- [Browser Compatibility](Browser-Compatibility.md)
- [Performance Tips](Performance-Tips.md)
- [GitHub Pages Deployment](GitHub-Pages.md)
