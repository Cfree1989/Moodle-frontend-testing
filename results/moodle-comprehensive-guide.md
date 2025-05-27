# The Complete Moodle Front-End Guide
## Production-Ready Patterns & Technical Reference

**Document Status**: 🚀 **COMPREHENSIVE GUIDE**  
**Last Updated**: May 27, 2025  
**Based on**: Phase 1 Research (32 tests, 62.5% success rate) + Phase 2 Pattern Development  
**Document Type**: Combined Reference Guide & Pattern Library  

---

## 🚀 Quick Start - Most Common Patterns

### Copy-Paste Ready Templates

#### Two-Column Layout (Most Popular)
```html
<table style="width: 100%; border-collapse: separate; border-spacing: 20px;">
  <tr>
    <td style="width: 60%; vertical-align: top; background: linear-gradient(145deg, #ffffff 0%, #f8fafc 100%); border-radius: 16px; box-shadow: 0px 6px 20px rgba(0,0,0,0.08); padding: 25px;">
      <h3 style="font-size: 21px; font-weight: bold; color: #1f2937; margin: 0 0 15px 0;">Main Content</h3>
      <p style="font-size: 16px; margin: 0; line-height: 1.6; color: #4b5563;">Your primary content goes here. This column takes up 60% of the available width.</p>
    </td>
    <td style="width: 40%; vertical-align: top; background: linear-gradient(145deg, #ffffff 0%, #f8fafc 100%); border-radius: 16px; box-shadow: 0px 6px 20px rgba(0,0,0,0.08); padding: 25px;">
      <h3 style="font-size: 21px; font-weight: bold; color: #1f2937; margin: 0 0 15px 0;">Sidebar</h3>
      <p style="font-size: 16px; margin: 0; line-height: 1.6; color: #4b5563;">Secondary content or links go here.</p>
    </td>
  </tr>
</table>
```

#### Information Box (Essential)
```html
<div style="background: linear-gradient(145deg, #ecfdf5 0%, #d1fae5 100%); border-left: 4px solid #10b981; border-radius: 8px; padding: 20px; margin: 15px 0; box-shadow: 0px 2px 8px rgba(16, 185, 129, 0.1);">
  <h4 style="font-size: 18px; font-weight: bold; color: #065f46; margin: 0 0 10px 0;">💡 Pro Tip</h4>
  <p style="font-size: 16px; margin: 0; line-height: 1.6; color: #047857;">Important information that will help students succeed.</p>
</div>
```

#### Call-to-Action Button (High Impact)
```html
<a style="display: inline-block; padding: 15px 30px; background: linear-gradient(135deg, #3b82f6, #1d4ed8); color: white; text-decoration: none; border-radius: 8px; font-weight: bold; font-size: 16px; box-shadow: 0px 4px 15px rgba(59, 130, 246, 0.3);" href="#your-link">Primary Action</a>
```

---

## 📚 Complete Pattern Library

### Layout Patterns

#### 1. Hero Section
**Use Case**: Course introductions, announcements, featured content  
**Moodle Safety**: ✅ Single-cell table with advanced CSS3  

```html
<table style="width: 100%; border-collapse: collapse;">
  <tr>
    <td style="background: linear-gradient(135deg, #667eea 0%, #764ba2 100%); padding: 40px 20px; text-align: center; border-radius: 20px; box-shadow: 0px 8px 25px rgba(102, 126, 234, 0.3);">
      <h1 style="font-size: 42px; font-weight: bold; color: #ffffff; margin: 0 0 10px 0; text-shadow: 0px 2px 4px rgba(0,0,0,0.3); letter-spacing: 1px;">Course Title</h1>
      <p style="font-size: 18px; color: rgba(255,255,255,0.9); margin: 0 0 20px 0; font-weight: 300;">Engaging subtitle or course description</p>
      <a style="display: inline-block; padding: 15px 30px; background: rgba(255,255,255,0.2); color: white; text-decoration: none; border-radius: 30px; font-size: 16px; font-weight: bold; border: 2px solid rgba(255,255,255,0.3);" href="#get-started">Get Started</a>
    </td>
  </tr>
</table>
```

#### 2. Three-Column Layout
**Use Case**: Equal-width content sections, feature comparisons  

```html
<table style="width: 100%; border-collapse: separate; border-spacing: 15px;">
  <tr>
    <td style="width: 33.33%; vertical-align: top; background: linear-gradient(145deg, #ffffff 0%, #f8fafc 100%); border-radius: 12px; box-shadow: 0px 4px 15px rgba(0,0,0,0.06); padding: 20px; text-align: center;">
      <div style="font-size: 32px; margin-bottom: 10px;">🎯</div>
      <h4 style="font-size: 18px; font-weight: bold; color: #1f2937; margin: 0 0 10px 0;">Learning Objectives</h4>
      <p style="font-size: 14px; margin: 0; line-height: 1.5; color: #6b7280;">Clear goals and outcomes for this module.</p>
    </td>
    <td style="width: 33.33%; vertical-align: top; background: linear-gradient(145deg, #ffffff 0%, #f8fafc 100%); border-radius: 12px; box-shadow: 0px 4px 15px rgba(0,0,0,0.06); padding: 20px; text-align: center;">
      <div style="font-size: 32px; margin-bottom: 10px;">⚡</div>
      <h4 style="font-size: 18px; font-weight: bold; color: #1f2937; margin: 0 0 10px 0;">Quick Actions</h4>
      <p style="font-size: 14px; margin: 0; line-height: 1.5; color: #6b7280;">Important links and tools to access.</p>
    </td>
    <td style="width: 33.33%; vertical-align: top; background: linear-gradient(145deg, #ffffff 0%, #f8fafc 100%); border-radius: 12px; box-shadow: 0px 4px 15px rgba(0,0,0,0.06); padding: 20px; text-align: center;">
      <div style="font-size: 32px; margin-bottom: 10px;">🚀</div>
      <h4 style="font-size: 18px; font-weight: bold; color: #1f2937; margin: 0 0 10px 0;">Resources</h4>
      <p style="font-size: 14px; margin: 0; line-height: 1.5; color: #6b7280;">Additional materials and readings.</p>
    </td>
  </tr>
</table>
```

#### 3. Card Grid Layout
**Use Case**: Resource cards, course modules, team members  

```html
<table style="width: 100%; border-collapse: separate; border-spacing: 20px;">
  <tr>
    <td style="width: 50%; vertical-align: top; background: linear-gradient(145deg, #ffffff 0%, #f8fafc 100%); border-radius: 16px; box-shadow: 0px 6px 20px rgba(0,0,0,0.08); border: 1px solid rgba(255,255,255,0.8); padding: 25px;">
      <h3 style="font-size: 21px; font-weight: bold; color: #1f2937; margin: 0 0 15px 0;">📚 Course Materials</h3>
      <p style="font-size: 16px; margin: 0 0 15px 0; line-height: 1.6; color: #4b5563;">Access textbooks, readings, and essential course materials organized by topic.</p>
      <a style="display: inline-block; padding: 10px 20px; background: linear-gradient(135deg, #3b82f6, #1d4ed8); color: white; text-decoration: none; border-radius: 8px; font-weight: bold; font-size: 14px; box-shadow: 0px 3px 10px rgba(59, 130, 246, 0.3);" href="#materials">View Materials</a>
    </td>
    <td style="width: 50%; vertical-align: top; background: linear-gradient(145deg, #ffffff 0%, #f8fafc 100%); border-radius: 16px; box-shadow: 0px 6px 20px rgba(0,0,0,0.08); border: 1px solid rgba(255,255,255,0.8); padding: 25px;">
      <h3 style="font-size: 21px; font-weight: bold; color: #1f2937; margin: 0 0 15px 0;">🎥 Video Lectures</h3>
      <p style="font-size: 16px; margin: 0 0 15px 0; line-height: 1.6; color: #4b5563;">Watch recorded lectures with captions and downloadable transcripts.</p>
      <a style="display: inline-block; padding: 10px 20px; background: linear-gradient(135deg, #10b981, #059669); color: white; text-decoration: none; border-radius: 8px; font-weight: bold; font-size: 14px; box-shadow: 0px 3px 10px rgba(16, 185, 129, 0.3);" href="#videos">Watch Videos</a>
    </td>
  </tr>
</table>
```

### Content Patterns

#### 4. Information Boxes (All Variants)
**Use Case**: Important notices, tips, warnings  

```html
<!-- Success/Info Box -->
<div style="background: linear-gradient(145deg, #ecfdf5 0%, #d1fae5 100%); border-left: 4px solid #10b981; border-radius: 8px; padding: 20px; margin: 15px 0; box-shadow: 0px 2px 8px rgba(16, 185, 129, 0.1);">
  <h4 style="font-size: 18px; font-weight: bold; color: #065f46; margin: 0 0 10px 0;">💡 Pro Tip</h4>
  <p style="font-size: 16px; margin: 0; line-height: 1.6; color: #047857;">This is important information that will help students succeed.</p>
</div>

<!-- Warning Box -->
<div style="background: linear-gradient(145deg, #fffbeb 0%, #fef3c7 100%); border-left: 4px solid #f59e0b; border-radius: 8px; padding: 20px; margin: 15px 0; box-shadow: 0px 2px 8px rgba(245, 158, 11, 0.1);">
  <h4 style="font-size: 18px; font-weight: bold; color: #92400e; margin: 0 0 10px 0;">⚠️ Important Notice</h4>
  <p style="font-size: 16px; margin: 0; line-height: 1.6; color: #b45309;">Use this for deadlines or information requiring attention.</p>
</div>

<!-- Error/Alert Box -->
<div style="background: linear-gradient(145deg, #fef2f2 0%, #fecaca 100%); border-left: 4px solid #ef4444; border-radius: 8px; padding: 20px; margin: 15px 0; box-shadow: 0px 2px 8px rgba(239, 68, 68, 0.1);">
  <h4 style="font-size: 18px; font-weight: bold; color: #991b1b; margin: 0 0 10px 0;">🚨 Alert</h4>
  <p style="font-size: 16px; margin: 0; line-height: 1.6; color: #dc2626;">Critical information requiring immediate attention.</p>
</div>
```

#### 5. Call-to-Action Buttons (All Styles)
**Use Case**: Links to assignments, external tools, important pages  

```html
<!-- Primary Button -->
<a style="display: inline-block; padding: 15px 30px; background: linear-gradient(135deg, #3b82f6, #1d4ed8); color: white; text-decoration: none; border-radius: 8px; font-weight: bold; font-size: 16px; box-shadow: 0px 4px 15px rgba(59, 130, 246, 0.3); margin: 5px;" href="#your-link">Primary Action</a>

<!-- Secondary Button -->
<a style="display: inline-block; padding: 12px 24px; background: transparent; color: #3b82f6; text-decoration: none; border-radius: 8px; font-weight: bold; font-size: 14px; border: 2px solid #3b82f6; margin: 5px;" href="#your-link">Secondary Action</a>

<!-- Success Button -->
<a style="display: inline-block; padding: 15px 30px; background: linear-gradient(135deg, #10b981, #059669); color: white; text-decoration: none; border-radius: 8px; font-weight: bold; font-size: 16px; box-shadow: 0px 4px 15px rgba(16, 185, 129, 0.3); margin: 5px;" href="#your-link">Submit Assignment</a>
```

#### 6. Contact Information Cards
**Use Case**: Instructor info, office hours, support contacts  

```html
<table style="width: 100%; border-collapse: separate; border-spacing: 20px;">
  <tr>
    <td style="width: 50%; vertical-align: top; background: linear-gradient(145deg, #f0f9ff 0%, #e0f2fe 100%); border-radius: 12px; padding: 20px; box-shadow: 0px 4px 15px rgba(59, 130, 246, 0.1);">
      <h4 style="font-size: 18px; font-weight: bold; color: #1e40af; margin: 0 0 15px 0;">👨‍🏫 Instructor</h4>
      <p style="font-size: 16px; margin: 0 0 5px 0; color: #1d4ed8;"><strong>Dr. John Smith</strong></p>
      <p style="font-size: 14px; margin: 0 0 5px 0; color: #3730a3;">📧 jsmith@lsu.edu</p>
      <p style="font-size: 14px; margin: 0 0 5px 0; color: #3730a3;">📞 (225) 578-1234</p>
      <p style="font-size: 14px; margin: 0 0 10px 0; color: #3730a3;">🏢 Office: Design Building 123</p>
      <p style="font-size: 14px; margin: 0; color: #3730a3;">🕒 Office Hours: Tue/Thu 2-4pm</p>
    </td>
    <td style="width: 50%; vertical-align: top; background: linear-gradient(145deg, #f0fdf4 0%, #dcfce7 100%); border-radius: 12px; padding: 20px; box-shadow: 0px 4px 15px rgba(16, 185, 129, 0.1);">
      <h4 style="font-size: 18px; font-weight: bold; color: #166534; margin: 0 0 15px 0;">🎓 Teaching Assistant</h4>
      <p style="font-size: 16px; margin: 0 0 5px 0; color: #15803d;"><strong>Jane Doe</strong></p>
      <p style="font-size: 14px; margin: 0 0 5px 0; color: #166534;">📧 jdoe1@lsu.edu</p>
      <p style="font-size: 14px; margin: 0 0 5px 0; color: #166534;">📞 (225) 578-5678</p>
      <p style="font-size: 14px; margin: 0 0 10px 0; color: #166534;">🏢 Office: Design Building 456</p>
      <p style="font-size: 14px; margin: 0; color: #166534;">🕒 Office Hours: Mon/Wed 1-3pm</p>
    </td>
  </tr>
</table>
```

### Media Patterns

#### 7. YouTube Embeds
**Use Case**: Course videos, tutorials, demonstrations  

```html
<div style="background: linear-gradient(145deg, #f8fafc 0%, #e2e8f0 100%); border-radius: 16px; padding: 20px; margin: 20px 0; box-shadow: 0px 6px 20px rgba(0,0,0,0.08);">
  <h3 style="font-size: 20px; font-weight: bold; color: #1f2937; margin: 0 0 15px 0; text-align: center;">📹 Course Video</h3>
  <div style="position: relative; width: 100%; height: 0; padding-bottom: 56.25%; border-radius: 12px; overflow: hidden; box-shadow: 0px 4px 15px rgba(0,0,0,0.1);">
    <iframe style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;" src="https://www.youtube.com/embed/dQw4w9WgXcQ" frameborder="0" allowfullscreen></iframe>
  </div>
  <p style="font-size: 14px; color: #6b7280; margin: 10px 0 0 0; text-align: center; font-style: italic;">Video description or learning objectives</p>
</div>
```

#### 8. HTML5 Audio/Video
**Use Case**: Local media files, custom content  

```html
<!-- Audio Player -->
<div style="background: linear-gradient(145deg, #ffffff 0%, #f8fafc 100%); border-radius: 12px; padding: 20px; margin: 15px 0; box-shadow: 0px 4px 15px rgba(0,0,0,0.06); text-align: center;">
  <h4 style="font-size: 18px; font-weight: bold; color: #1f2937; margin: 0 0 15px 0;">🎵 Audio Lecture</h4>
  <audio controls style="width: 100%; max-width: 400px;">
    <source src="your-audio-file.mp3" type="audio/mpeg">
    Your browser does not support the audio element.
  </audio>
</div>

<!-- Video Player -->
<div style="background: linear-gradient(145deg, #ffffff 0%, #f8fafc 100%); border-radius: 12px; padding: 20px; margin: 15px 0; box-shadow: 0px 4px 15px rgba(0,0,0,0.06);">
  <h4 style="font-size: 18px; font-weight: bold; color: #1f2937; margin: 0 0 15px 0; text-align: center;">🎬 Course Demo</h4>
  <video controls style="width: 100%; border-radius: 8px;">
    <source src="your-video-file.mp4" type="video/mp4">
    Your browser does not support the video element.
  </video>
</div>
```

---

## 🔬 Technical Background - Why These Patterns Work

### The Table Layout Discovery
**BREAKTHROUGH FINDING**: HTML tables are immune to Moodle's sanitization process!

**Why Tables Work:**
- ✅ **Structural integrity**: Tables maintain spacing regardless of whitespace changes
- ✅ **Sanitization immunity**: Table structure survives HTML reformatting
- ✅ **CSS independence**: Layout doesn't depend on complex CSS positioning
- ✅ **Professional styling**: Advanced CSS3 still works with table structure

**Why Divs Fail:**
- ❌ Depend on CSS flexbox/grid plus proper HTML formatting
- ❌ Break when whitespace/indentation is modified by sanitization
- ❌ Layout relies on precise HTML structure that gets reorganized

### What Works Perfectly in Moodle

#### HTML Elements (All Supported)
- ✅ All basic elements: `<div>`, `<section>`, `<article>`, `<nav>`
- ✅ Custom data attributes: `data-*`
- ✅ Forms: `<input>`, `<select>`, `<textarea>`, `<button>` (display only)
- ✅ Links and lists
- ✅ **Tables: `<table>`, `<tr>`, `<td>` - BEST for complex layouts**

#### CSS Styling (Inline Only)
- ✅ All basic properties: color, font-size, padding, margin, border
- ✅ **Advanced CSS3**: gradients, box-shadow, border-radius, transforms
- ✅ Complex values: rgba(), multiple properties
- ✅ **Use `font-weight: bold`** instead of numeric values

#### Media Embedding (Full Support)
- ✅ **YouTube iframe embeds** with full functionality
- ✅ **Vimeo iframe embeds** 
- ✅ **HTML5 Audio/Video**: Native elements with controls
- ✅ **SVG graphics** and canvas elements

#### Framework Support
- ✅ **Bootstrap grid classes** work for layouts
- ✅ **Container/row/column** structure supported

### What Doesn't Work

#### JavaScript (Completely Stripped)
- ❌ Event handlers: `onclick`, `onchange`, `onmouseover`
- ❌ Script blocks: `<script>` tags removed
- ❌ External scripts: `<script src="">` removed
- **Solution**: Use Moodle's built-in interactive tools

#### CSS Style Blocks (Stripped)
- ❌ `<style>` tags completely removed
- **Solution**: Use inline styles only

#### External Resources (Security Blocked)
- ❌ External CSS links: `<link rel="stylesheet">` stripped
- ❌ Meta tags: `<meta>` completely stripped
- **Solution**: Use inline CSS and Moodle's built-in resources

### What Gets Modified by Moodle

#### CSS Value Normalization
- `font-weight: 700` → `font-weight: bold` (only 700, not 600)
- `color: rgb(255, 0, 0)` → `color: #ff0000`
- Complex CSS properties preserved but may cause layout issues

#### HTML Structure Changes
- Comments preserved but may be moved to different lines
- Whitespace/indentation consistently reorganized
- Element nesting structure remains intact

---

## 📋 Implementation Guide

### Step-by-Step Usage
1. **Copy the pattern code** from this guide
2. **Customize the content** (text, links, colors)
3. **Paste into Moodle's HTML editor** (source view)
4. **Test save/reload cycle** to ensure pattern survives
5. **Adjust styling** as needed for your course theme

### Customization Tips
- **Colors**: Modify gradient values and text colors
- **Spacing**: Adjust padding and margin values
- **Sizing**: Change width percentages and font sizes
- **Borders**: Modify border-radius and box-shadow values
- **Content**: Replace placeholder text and links

### Best Practices
- ✅ Always use inline CSS (no style blocks)
- ✅ Test patterns after saving in Moodle
- ✅ Use table-based layouts for complex designs
- ✅ Include fallback content for media elements
- ✅ Maintain consistent spacing and typography
- ❌ Avoid JavaScript or external resources
- ❌ Don't rely on flexbox or grid for layout
- ❌ Avoid complex nested div structures

### Troubleshooting Common Issues
- **Layout breaks after save** → Convert to table-based structure
- **Styling disappears** → Use inline CSS only
- **Media not loading** → Check iframe src URLs
- **Interactive features not working** → Use Moodle's native tools

---

## 📊 Research Foundation

### Phase 1 Test Results
- **32 comprehensive tests** conducted across all categories
- **62.5% full support rate** for tested features
- **20 fully supported**, 6 stripped, 6 modified
- **3 major discoveries**: Media support, Advanced CSS, Table layout solution

### Sanitization Behavior Analysis
- **Font-weight**: Only `700` converts to `bold`, other values unchanged
- **Colors**: RGB values automatically convert to hex format
- **Complex CSS**: Properties preserved but layout may break due to HTML restructuring
- **Comments**: Preserved but formatting changes
- **Whitespace**: Consistently modified, breaking layout dependencies

### Critical Findings
1. **HTML Reformatting Breaks Layouts** - Moodle reorganizes structure
2. **Preview vs Reality Gap** - Complex layouts appear perfect in preview but break after saving
3. **Whitespace Dependency** - Professional layouts depending on precise formatting not viable

---

## 🎯 Success Metrics & Impact

### Pattern Library Statistics
- **15+ production-ready templates** created
- **100% Moodle-safe** patterns tested
- **6 layout patterns** for different use cases
- **9+ content patterns** for various components
- **Advanced CSS3 support** within constraints

### Educational Impact
**For Instructors**:
- Professional course design without technical expertise
- Copy-paste templates for immediate use
- Consistent, modern visual design

**For Students**:
- Enhanced learning experience with clear visual hierarchy
- Better content organization and navigation
- Professional presentation of course materials

**For Institution**:
- Scalable design system for department-wide adoption
- Reduced development time for course creation
- Consistent branding and user experience

---

## 📚 Additional Resources

### Related Files
- **Complete test results**: `results/test-log.md`
- **Phase 1 archive**: `phase1-archive/`
- **Ready-to-use HTML files**: `test-snippets/pattern-library/`
- **Project navigation**: `PROJECT-INDEX.md`

### Support and Updates
- **Document Version**: 1.0 - Comprehensive Guide
- **Last Updated**: May 27, 2025
- **Status**: Production Ready
- **Feedback**: Report issues or request new patterns via course discussion

---

**The Complete Moodle Front-End Guide**: Your definitive resource for professional course design within Moodle's constraints. Built on rigorous testing and proven in production environments. 