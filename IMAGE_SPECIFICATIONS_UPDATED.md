# Updated Image Specifications for Nurse.ICU Website

## Layout Changes - Images Now Left-Aligned

The website layout has been updated to use a **horizontal card layout** where images appear on the left side of content instead of above it.

## Image Categories & Specifications

### 1. Hero Images (No Change)
**Location:** Homepage main banner
**Dimensions:** 1536x1024px (your current image dimensions)
**Format:** PNG
**Current file:** `hero-banner.png`
**CSS Class:** `.hero-image-full`

---

### 2. Resource Card Images (UPDATED SIZE)
**Location:** Left side of resource cards
**Dimensions:** 150x100px (3:2 aspect ratio) - Perfect for 1536x1024 source images
**Format:** PNG (changed from JPG)
**Layout:** Images now appear on the LEFT of content

#### Required PNG Files (150x100px each):

1. **nclex-prep.png**
   - Content: Stressed student with coffee and highlighters
   - Theme: Reality of studying

2. **clinical-refs.png**
   - Content: Quick reference cards/cheat sheets
   - Theme: Practical tools

3. **nursing-skills.png**
   - Content: Nurse mid-procedure, focused
   - Theme: Real clinical work

4. **nursing-education.png**
   - Content: Online learning setup, coffee required
   - Theme: Remote learning reality

5. **nursing-ceus.png**
   - Content: Certificate completion screen
   - Theme: The grind continues

6. **career-advancement.png**
   - Content: Professional meeting or interview
   - Theme: Playing the game

7. **specialty-certifications.png**
   - Content: Certificate wall or badge collection
   - Theme: Achievement unlocked

8. **nursing-products.png**
   - Content: Quality nursing gear laid out
   - Theme: Tools of the trade

9. **nursing-legal.png**
   - Content: Legal documents, serious tone
   - Theme: Protect yourself

**CSS Class:** `.resource-image`

---

## New Layout Structure

Each resource item now uses this structure:
```
┌─────────────────────────────────────────┐
│ [150x100  ] │ Title                     │
│ [Image    ] │ Description text...       │
│ [         ] │ [Tag] [Tag] [Tag]         │
└─────────────────────────────────────────┘
```

### Responsive Behavior:
- **Desktop/Tablet:** Image left (150x100px), content right
- **Mobile:** Stacks vertically with centered 120x80px images

---

## Implementation Notes

### File Format Change:
- **Changed from JPG to PNG** for better quality and transparency support
- All resource images are now **150x100px instead of 400x120px**
- **Perfect 3:2 aspect ratio** matches your 1536x1024 source images

### HTML Structure Change:
Each resource item now includes a `.resource-item-content` wrapper:
```html
<a href="page.html" class="resource-item">
  <div class="img-placeholder resource-image"><!-- Image here --></div>
  <div class="resource-item-content">
    <h3>Title</h3>
    <p>Description</p>
    <div class="specialty-tags"><!-- Tags here --></div>
  </div>
</a>
```

### CSS Changes:
- `.resource-item` now uses `display: flex`
- Images are `flex-shrink: 0` to maintain size
- Content area uses `flex: 1` to fill remaining space

---

## Migration Steps

1. **Create smaller PNG versions** of your resource images (80x80px)
2. **Focus on icon-style imagery** rather than wide landscapes
3. **Ensure images work well at small sizes** - simple, clear designs
4. **Save all as PNG format** in `assets/images/` directory
5. **Test on mobile** to ensure 60x60px versions are still readable

---

## Benefits of New Layout

- **More content visible** without scrolling
- **Better use of horizontal space** on desktop
- **Professional appearance** similar to modern app layouts
- **Improved readability** with content prominently displayed
- **Mobile-friendly** stacking behavior
