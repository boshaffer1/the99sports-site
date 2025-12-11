# The 99 - Figma Setup Guide

## Step 1: Create New File
- New design file → Name: "The 99 Website"
- Frame: Desktop (1440 x 900)

---

## Step 2: Set Up Colors (Styles)
Right panel → Local styles → + Color

| Name | Hex |
|------|-----|
| Black | #0A0A0A |
| White | #FFFFFF |
| Gold | #D4AF37 |
| Gold Light | #F4D03F |
| Gray | #888888 |
| Gray Dark | #1A1A1A |

---

## Step 3: Set Up Text Styles
Right panel → Local styles → + Text

| Name | Font | Weight | Size |
|------|------|--------|------|
| H1 Hero | Unbounded | SemiBold | 72px |
| H2 Section | Unbounded | SemiBold | 48px |
| H3 Card | Unbounded | SemiBold | 24px |
| Body | Inter | Regular | 18px |
| Body Small | Inter | Regular | 16px |
| Tag | Inter | Bold | 12px |
| Button | Unbounded | Medium | 14px |

---

## Step 4: Create Frames (Pages)

### Frame 1: Hero (1440 x 900)
```
Background: #0A0A0A
├── Logo (80px height, centered top)
├── H1: "Build Athletes' Futures" (center)
│   └── "Futures" in Gold
├── Subtext (Gray, 18px, max-width 550px)
└── Button: "Work With Us" (Gold bg, Black text)
```

### Frame 2: Metrics Banner (1440 x 200)
```
Background: Linear gradient #111111 → #0A0A0A
├── 4 columns, centered
│   ├── "50+" / "Programs Served"
│   ├── "500+" / "Athletes Educated"
│   ├── "$10M+" / "Deals Facilitated"
│   └── "100+" / "Speaking Events"
```

### Frame 3: The Reality (1440 x 800)
```
Background: #111111
├── Left column (text)
│   ├── Tag: "THE REALITY"
│   ├── H2: "The NIL Market Isn't Built for Everyone"
│   ├── Body text
│   └── 3 Problem cards (icon + title + text)
└── Right column
    └── Pie chart graphic (99% gold, 1% gray)
```

### Frame 4: Why The 99 (1440 x 600)
```
Background: #0A0A0A
├── Tag: "WHY THE 99?"
├── H2: "We Bridge the Gap"
└── 3 Cards (equal width)
    ├── "For Schools" + icon + text
    ├── "For Athletes" + icon + text
    └── "For Brands" + icon + text
```

### Frame 5: About (1440 x 700)
```
Background: #1A1A1A
├── Left: Image (trace-presenting.jpg)
└── Right:
    ├── Tag: "ABOUT"
    ├── H2: "Meet Trace Young"
    ├── Bio paragraphs
    └── 3 Highlight pills
```

### Frame 6: Services (1440 x 700)
```
Background: #0A0A0A
├── Tag + H2 centered
├── 5 Tab buttons (Schools, Athletes, Brands, Workshops, Speaking)
└── Content area
    ├── Left: Service list (bullet points)
    └── Right: Image
```

### Frame 7: Testimonials (1440 x 600)
```
Background: #1A1A1A
├── Tag: "WHAT LEADERS SAY"
├── H2: "Trusted by Industry Leaders"
└── 3 Cards (grid)
    └── Each: Quote + Avatar circle + Name + Title
```

### Frame 8: CTA (1440 x 400)
```
Background: Gradient #0A0A0A → #1a1510
├── H2: "Ready to Get Started?"
├── Body text
└── 2 Buttons
    ├── "Schedule a Call" (Gold)
    └── "Email Us" (Outline)
```

### Frame 9: Footer (1440 x 150)
```
Background: #0A0A0A
Border-top: 1px #222
├── Logo (left)
├── Links (center): Athletes | Schools | Brands | Contact | Instagram
└── Copyright (right)
```

---

## Step 5: Add Images
1. Drag images from Finder into Figma canvas
2. Place in appropriate frames
3. Set to "Fill" mode for cover effect

Images needed:
- logo-99.png
- trace-presenting.jpg
- trace-suit.jpg
- trace-lsu.jpg
- trace-smu.jpg

---

## Step 6: Export to Framer

1. Select all frames (Cmd+A)
2. Plugins → Framer → Copy to Framer
3. Open Framer → Paste (Cmd+V)
4. Framer will import with:
   - All images
   - Text styles
   - Colors
   - Layout structure

---

## Component Specs

### Button - Primary
```
Padding: 14px 36px
Background: #D4AF37
Text: #0A0A0A
Font: Unbounded Medium 14px
Border-radius: 4px
```

### Button - Outline
```
Padding: 14px 36px
Background: transparent
Border: 1px solid rgba(255,255,255,0.3)
Text: #FFFFFF
Font: Unbounded Medium 14px
Border-radius: 4px
```

### Card
```
Background: rgba(255,255,255,0.02)
Border: 1px solid rgba(255,255,255,0.08)
Border-radius: 16px
Padding: 28px
```

### Tag
```
Font: Inter Bold 12px
Color: #D4AF37
Letter-spacing: 0.12em
Uppercase
```

### Avatar Circle
```
Size: 44x44
Background: Linear gradient #D4AF37 → #F4D03F
Border-radius: 50%
Text: Unbounded Bold 14px, #000
```

---

## Quick Start

1. Open Figma
2. Press F → Create frame 1440x900
3. Fill background #0A0A0A
4. Add text "Unbounded" font (search in font picker)
5. Start building sections top to bottom
6. Drag in images from the assets folder I opened

Need the Unbounded font? It's on Google Fonts - Figma has it built in, just search "Unbounded" in the font picker.
