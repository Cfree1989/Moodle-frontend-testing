# Moodle HTML/CSS Reference Guide for Instructors

**Phase 1 Completion Status**: ✅ **COMPLETED**  
**Completion Date**: May 2025  
**Project Phase**: Phase 1 Final Results  
**Next Phase**: Phase 2 - Production-Ready Pattern Development  

## Executive Summary
**32 comprehensive tests completed. 20 fully supported, 6 stripped, 6 modified.**

**BREAKTHROUGH DISCOVERY**: HTML tables are immune to Moodle's sanitization and enable professional layouts!

**Key Finding**: Use table-based layouts for complex designs - they survive Moodle's HTML sanitization while div-based layouts break.

---

## What Works Perfectly

### Table-Based Layouts (RECOMMENDED - Sanitization Immune)
```html
<table style="width: 100%; border-collapse: separate; border-spacing: 20px;">
  <tr>
    <td style="width: 50%; background: linear-gradient(145deg, #ffffff 0%, #f8fafc 100%); border-radius: 16px; box-shadow: 0px 6px 20px rgba(0,0,0,0.08); padding: 25px;">
      <h3 style="font-size: 21px; font-weight: bold; color: #1f2937; margin: 0 0 15px 0;">Card Title</h3>
      <p style="font-size: 16px; margin: 0 0 15px 0; line-height: 1.6; color: #4b5563;">Card content here</p>
      <a style="display: inline-block; padding: 10px 20px; background: linear-gradient(135deg, #3b82f6, #1d4ed8); color: white; text-decoration: none; border-radius: 8px; font-weight: bold;">Button</a>
    </td>
    <td style="width: 50%; background: #f5f5f7; border-radius: 16px; padding: 25px;">
      <h3 style="font-size: 21px; font-weight: bold; margin: 0 0 15px 0;">Second Column</h3>
      <p style="margin: 0;">More content here</p>
    </td>
  </tr>
</table>
```

**Why Tables Work:**
- ✅ **Immune to sanitization** - structure survives HTML reformatting
- ✅ **Reliable spacing** - uses `border-spacing` for consistent gaps
- ✅ **Professional styling** - complex CSS works perfectly
- ✅ **Nested layouts** - tables can be nested for sophisticated designs

### HTML Elements (All Supported)
- All basic elements: `<div>`, `<section>`, `<article>`, `<nav>`
- Custom data attributes: `data-*`
- Forms: `<input>`, `<select>`, `<textarea>`, `<button>` (display only)
- Links and lists
- **Tables: `<table>`, `<tr>`, `<td>` - BEST for complex layouts**

### CSS Styling (Inline Only)
```html
<div style="color: red; font-size: 20px; padding: 10px; border: 1px solid blue;">
```
- All basic properties: color, font-size, padding, margin, border
- **Advanced CSS3**: gradients, box-shadow, border-radius, transforms
- Complex values: rgba(), multiple properties
- **Use `font-weight: bold`** instead of numeric values (700 gets converted)

### Media Embedding (Full Support)
```html
<!-- YouTube -->
<iframe src="https://www.youtube.com/embed/VIDEO_ID" width="560" height="315"></iframe>

<!-- Vimeo -->
<iframe src="https://player.vimeo.com/video/VIDEO_ID" width="640" height="360"></iframe>

<!-- HTML5 Audio -->
<audio controls>
    <source src="audio.wav" type="audio/wav">
</audio>

<!-- HTML5 Video -->
<video controls width="320" height="240">
    <source src="video.mp4" type="video/mp4">
</video>
```

### Bootstrap Framework Support
```html
<div class="container">
    <div class="row">
        <div class="col-sm-6">Column 1</div>
        <div class="col-sm-6">Column 2</div>
    </div>
</div>
```

### Graphics Elements
```html
<!-- SVG Graphics -->
<svg width="100" height="100">
    <circle cx="50" cy="50" r="40" stroke="black" fill="red" />
</svg>

<!-- Canvas -->
<canvas width="200" height="100" style="border:1px solid #000;"></canvas>
```

---

## What Doesn't Work

### JavaScript (Completely Stripped)
- Event handlers: `onclick`, `onchange`, `onmouseover`
- Script blocks: `<script>` tags removed
- External scripts: `<script src="">` removed
- **Solution**: Use Moodle's built-in interactive tools instead

### CSS Style Blocks (Stripped)
```html
<!-- This gets completely removed -->
<style>
.my-class { background: yellow; }
</style>
```
**Solution**: Use inline styles only

### External Resources (Security Blocked)
- External CSS links: `<link rel="stylesheet">` stripped  
- Meta tags: `<meta>` completely stripped
- **Solution**: Use inline CSS and Moodle's built-in resources

### Complex Div Layouts (Break Due to Sanitization)
```html
<!-- AVOID: This breaks after save/reload -->
<div style="display: flex; justify-content: space-between;">
  <div style="flex: 1; margin-right: 20px;">Content</div>
  <div style="flex: 1;">Content</div>
</div>
```
**Solution**: Use table layouts instead

---

## What Gets Modified by Moodle

### CSS Value Normalization
- `font-weight: 700` → `font-weight: bold`
- `color: rgb(255, 0, 0)` → `color: #ff0000`
- `font-weight: 600` stays unchanged (only 700 converts)

### HTML Structure Changes
- Comments removed
- Whitespace/indentation reorganized
- `<object>` tags → `<iframe>` conversion

### Form Behavior
- Forms display perfectly but don't submit (no backend processing)
- Use for visual organization only

---

## Best Practices & Patterns

### 1. Professional Multi-Column Layout
```html
<table style="width: 100%; border-collapse: separate; border-spacing: 20px;">
  <tr>
    <td style="width: 33%; background: #f8fafc; border-radius: 12px; padding: 20px;">
      <h3 style="font-weight: bold; margin: 0 0 10px 0;">Column 1</h3>
      <p style="margin: 0;">Content here</p>
    </td>
    <td style="width: 33%; background: #f8fafc; border-radius: 12px; padding: 20px;">
      <h3 style="font-weight: bold; margin: 0 0 10px 0;">Column 2</h3>
      <p style="margin: 0;">Content here</p>
    </td>
    <td style="width: 33%; background: #f8fafc; border-radius: 12px; padding: 20px;">
      <h3 style="font-weight: bold; margin: 0 0 10px 0;">Column 3</h3>
      <p style="margin: 0;">Content here</p>
    </td>
  </tr>
</table>
```

### 2. Styled Content Box
```html
<div style="background: linear-gradient(45deg, #ff6b6b, #4ecdc4); padding: 20px; border-radius: 10px; color: white; text-align: center; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">
    Your content here
</div>
```

### 3. Media Section with Description
```html
<div style="text-align: center; margin: 20px 0;">
    <iframe src="https://www.youtube.com/embed/VIDEO_ID" width="560" height="315" style="border-radius: 8px;"></iframe>
    <p style="margin-top: 10px; font-style: italic; color: #666;">Video description</p>
</div>
```

### 4. Resource List with Links
```html
<table style="width: 100%; border-collapse: separate; border-spacing: 0;">
  <tr>
    <td style="background: #f5f5f7; border-radius: 12px; padding: 20px;">
      <h3 style="font-weight: bold; margin: 0 0 15px 0;">Resources</h3>
      <ul style="list-style-type: none; padding: 0; margin: 0;">
        <li style="margin-bottom: 8px;"><a style="color: #0070c9; text-decoration: none;" href="link1.pdf">Resource 1</a></li>
        <li style="margin-bottom: 8px;"><a style="color: #0070c9; text-decoration: none;" href="link2.pdf">Resource 2</a></li>
        <li><a style="color: #0070c9; text-decoration: none;" href="link3.pdf">Resource 3</a></li>
      </ul>
    </td>
  </tr>
</table>
```

### 5. Call-to-Action Button
```html
<div style="text-align: center; margin: 20px 0;">
  <a style="display: inline-block; padding: 15px 30px; background: linear-gradient(135deg, #3b82f6, #1d4ed8); color: white; text-decoration: none; border-radius: 25px; font-weight: bold; box-shadow: 0 4px 12px rgba(59, 130, 246, 0.3);" href="https://forms.office.com/your-form">Submit Assignment</a>
</div>
```

---

## Development Workflow

### 1. Design Phase
- Plan layout using table structure
- Use inline CSS for all styling
- Avoid JavaScript dependencies

### 2. Implementation
- Start with table framework
- Add styling to table cells
- Test multimedia embeds

### 3. Testing
- Save and reload to check sanitization effects
- Verify layout maintains structure
- Test on different screen sizes

### 4. Optimization
- Simplify nested structures where possible
- Use consistent spacing with `border-spacing`
- Optimize for maintainability

---

## Troubleshooting Common Issues

### Layout Breaks After Saving
**Problem**: Div-based layout spacing issues
**Solution**: Convert to table-based layout

### Font Weight Not Working
**Problem**: `font-weight: 700` becomes `bold`
**Solution**: Use `font-weight: bold` directly

### Colors Look Different
**Problem**: `rgb()` values convert to hex
**Solution**: Use hex colors from the start

### JavaScript Not Working
**Problem**: All scripts stripped by Moodle
**Solution**: Use Moodle's built-in interactive features

---

## Project Impact

**Research Completed**: 32 comprehensive tests across all HTML/CSS/JS categories
**Success Rate**: 62.5% full support, with table layouts achieving 100% reliability
**Key Discovery**: Table-based layouts solve the professional design challenge in Moodle

**Instructor Benefits**:
- Create professional, multimedia-rich course content
- Use verified, tested design patterns
- Avoid common pitfalls and sanitization issues
- Build maintainable, reusable layouts

**Next Steps**:
- Use this guide for course design
- Share table layout patterns with other instructors
- Build template library for common use cases

---

**Document Status**: ✅ **FINAL VERSION** - Complete reference guide
**Last Updated**: [Current Date]
**Project**: Moodle Front-End Coding Discovery - LSU Lab 