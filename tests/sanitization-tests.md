# Moodle Sanitization Behavior Test Plan

## Overview
This document outlines systematic tests to understand how Moodle's sanitization system modifies HTML and CSS code during the save/reload cycle.

## Key Findings So Far
- `font-weight: 700` gets converted to `font-weight: bold`
- HTML structure gets reorganized (comments removed, formatting changed)
- Visual layouts can break due to sanitization changes

## Test Categories

### 1. CSS Property Value Normalization Tests

#### Test 1.1: Font-Weight Values
**Purpose**: Understand how font-weight values are normalized

**Input Code**:
```html
<div style="font-weight: 100;">Weight 100</div>
<div style="font-weight: 300;">Weight 300</div>
<div style="font-weight: 400;">Weight 400</div>
<div style="font-weight: 500;">Weight 500</div>
<div style="font-weight: 600;">Weight 600</div>
<div style="font-weight: 700;">Weight 700</div>
<div style="font-weight: 800;">Weight 800</div>
<div style="font-weight: 900;">Weight 900</div>
<div style="font-weight: bold;">Weight bold</div>
<div style="font-weight: normal;">Weight normal</div>
```

**Expected Behavior**: Document which numeric values get converted to keywords

#### Test 1.2: Color Value Normalization
**Purpose**: Test how different color formats are handled

**Input Code**:
```html
<div style="color: #ff0000;">Hex Red</div>
<div style="color: red;">Keyword Red</div>
<div style="color: rgb(255, 0, 0);">RGB Red</div>
<div style="color: rgba(255, 0, 0, 0.5);">RGBA Red</div>
<div style="color: hsl(0, 100%, 50%);">HSL Red</div>
<div style="background-color: #ffffff;">White Background</div>
<div style="background-color: white;">White Keyword</div>
```

#### Test 1.3: Size and Measurement Units
**Purpose**: Test how different units are normalized

**Input Code**:
```html
<div style="font-size: 16px;">16px font</div>
<div style="font-size: 1em;">1em font</div>
<div style="font-size: 1rem;">1rem font</div>
<div style="font-size: 100%;">100% font</div>
<div style="padding: 10px;">10px padding</div>
<div style="margin: 1em;">1em margin</div>
<div style="width: 50%;">50% width</div>
<div style="height: 100vh;">100vh height</div>
```

### 2. HTML Structure Preservation Tests

#### Test 2.1: Comment Preservation
**Purpose**: Test if HTML comments survive sanitization

**Input Code**:
```html
<!-- This is a test comment -->
<div>Content with comment above</div>
<div>
    <!-- Inline comment -->
    Content with inline comment
</div>
<!-- Final comment -->
```

#### Test 2.2: Whitespace and Formatting
**Purpose**: Test how whitespace and indentation are handled

**Input Code**:
```html
<div class="container">
    <div class="row">
        <div class="col-6">
            <p>Properly indented content</p>
        </div>
        <div class="col-6">
            <p>More content</p>
        </div>
    </div>
</div>
```

#### Test 2.3: Complex Nesting
**Purpose**: Test how deeply nested structures are handled

**Input Code**:
```html
<div style="border: 1px solid black;">
    <div style="padding: 20px;">
        <div style="background: lightgray;">
            <div style="margin: 10px;">
                <p style="color: blue;">Deeply nested content</p>
            </div>
        </div>
    </div>
</div>
```

### 3. Modern CSS Property Tests

#### Test 3.1: Flexbox Properties
**Purpose**: Test if modern CSS properties are preserved

**Input Code**:
```html
<div style="display: flex; justify-content: center; align-items: center; height: 100px; background: lightblue;">
    <div style="flex: 1;">Flex item 1</div>
    <div style="flex: 2;">Flex item 2</div>
</div>
```

#### Test 3.2: CSS Grid Properties
**Purpose**: Test CSS Grid support

**Input Code**:
```html
<div style="display: grid; grid-template-columns: 1fr 1fr; gap: 10px; background: lightgreen;">
    <div style="background: white; padding: 10px;">Grid item 1</div>
    <div style="background: white; padding: 10px;">Grid item 2</div>
</div>
```

#### Test 3.3: Transform and Animation Properties
**Purpose**: Test advanced CSS properties

**Input Code**:
```html
<div style="transform: rotate(5deg); transition: all 0.3s ease; background: yellow; padding: 20px;">
    Transformed content
</div>
<div style="animation: none; transform: scale(1.1);">
    Scaled content
</div>
```

### 4. Vendor Prefix Tests

#### Test 4.1: Webkit Prefixes
**Purpose**: Test if vendor prefixes are preserved

**Input Code**:
```html
<div style="-webkit-border-radius: 10px; border-radius: 10px; background: orange; padding: 15px;">
    Rounded corners with prefixes
</div>
<div style="-webkit-box-shadow: 0 2px 5px rgba(0,0,0,0.2); box-shadow: 0 2px 5px rgba(0,0,0,0.2); background: white; padding: 10px;">
    Shadow with prefixes
</div>
```

### 5. Save/Reload Cycle Tests

#### Test 5.1: Progressive Sanitization
**Purpose**: Test if sanitization continues with each save

**Process**:
1. Save complex HTML code
2. Reload and check changes
3. Save again without modifications
4. Reload and check for further changes
5. Repeat 2-3 times

#### Test 5.2: Consistency Test
**Purpose**: Test if sanitization is consistent

**Process**:
1. Create identical content in two different pages
2. Save both
3. Compare results for consistency

## Test Execution Template

For each test, document:

| Test ID | Input Code | Output Code | Changes Made | Visual Impact | Notes |
|---------|------------|-------------|--------------|---------------|-------|
| 1.1 | [original] | [after save] | [list changes] | [broken/working] | [observations] |

## Expected Outcomes

1. **CSS Value Normalization Rules**: Clear documentation of which values get converted
2. **HTML Structure Rules**: Understanding of formatting and comment handling
3. **Modern CSS Support**: Knowledge of which properties are safe to use
4. **Sanitization Timing**: Understanding when and how often sanitization occurs
5. **Best Practices**: Guidelines for writing sanitization-resistant code

## Success Criteria

- Complete documentation of all sanitization behaviors
- Updated reference guide with "safe" patterns
- Recommendations for robust Moodle HTML/CSS development
- Test results that can be reproduced by other developers 