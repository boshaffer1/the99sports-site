# The 99 - Framer Content Guide

## Design System

### Colors
```
Black:       #0A0A0A
White:       #FFFFFF
Gold:        #D4AF37
Gold Light:  #F4D03F
Gray:        #888888
Gray Dark:   #1A1A1A
Gray Darker: #111111
```

### Font
- Headlines: **Unbounded** (Google Fonts)
- Body: System fonts (SF Pro, Segoe UI, Roboto)

### Buttons
- Primary: Gold background, black text
- Secondary: Transparent, white border, white text

---

## Assets to Upload

### Images (in assets/images/)
- logo-99.png (main logo)
- trace-presenting.jpg
- trace-suit.jpg
- trace-lsu.jpg
- trace-smu.jpg
- trace-portrait.jpg

### Videos (in assets/videos/)
- hero-bg.mp4
- THE 99 WEB - FINAL.mov (VSL)

---

## Page Sections

### 1. NAVBAR
Links: Athletes | Schools | Brands | Contact (gold CTA)

---

### 2. HERO
**Headline:** Build Athletes' Futures
*(Note: "Futures" should be gold)*

**Subhead:** Elite NIL consulting for athletic programs, student-athletes, and brands. Maximizing value through strategic partnerships.

**CTA Button:** Work With Us

**Background:** hero-bg.mp4 (grayscale, overlay)

---

### 3. METRICS BANNER
| 50+ | 500+ | $10M+ | 100+ |
|-----|------|-------|------|
| Programs Served | Athletes Educated | Deals Facilitated | Speaking Events |

---

### 4. THE REALITY (Pie Chart Section)
**Tag:** The Reality
**Headline:** The NIL Market Isn't Built for Everyone

**Subhead:** While headlines celebrate million-dollar deals for star athletes, 99% of college athletes are left without guidance, strategy, or opportunity.

**Problem Points:**
1. **Extreme Inequality** - The top 1% of athletes capture 95% of all NIL money.
2. **No Education** - Less than 10% of NCAA athletes have consistent NIL deals.
3. **Schools That Lead Win** - Programs teaching every athlete NIL will dominate recruiting.

**Pie Chart Stats:**
- 99% of athletes need help
- 5% of NIL money goes to the 99%
- 95% captured by top 1%
- <10% of NCAA athletes have deals
- 4 yrs average eligibility window

---

### 5. WHY THE 99
**Tag:** Why The 99?
**Headline:** We Bridge the Gap
**Subhead:** Strategic NIL solutions for athletic programs, athletes, and brands.

**3 Cards:**

**For Schools**
Comprehensive NIL education programs that prepare your athletes for success while maintaining compliance.

**For Athletes**
Strategic brand building and partnership development that maximizes your earning potential.

**For Brands**
Access to authentic athlete partnerships that drive real engagement and results.

---

### 6. ABOUT TRACE
**Tag:** About
**Headline:** Meet Trace Young

**Bio Paragraph 1:**
A former collegiate athlete turned NIL expert, Trace Young founded The 99 to level the playing field for student-athletes nationwide. His mission: ensure every athlete—not just the top 1%—has the tools to build their brand and secure meaningful partnerships.

**Bio Paragraph 2:**
With hands-on experience at Power 5 programs and a deep understanding of the NIL landscape, Trace delivers high-impact workshops and keynote speeches that transform how programs approach athlete development.

**Highlights:**
- Featured Speaker at NCAA Events
- As Seen on ESPN & Amazon Prime
- Trusted by Power 5 Programs

**Image:** trace-presenting.jpg

---

### 7. FEATURED IN (Logo Marquee)
Logos: ESPN, Amazon Prime, Nike, Adidas, NCAA

---

### 8. SERVICES (Tabbed)

**Tag:** Our Services
**Headline:** How We Help
**Subhead:** From campus visits to year-round consulting, we meet programs and athletes where they are.

**Tabs:** Schools | Athletes | Brands | Workshops | Speaking

#### Schools Tab
**Title:** Athletic Program Solutions
- NIL Education Workshops for student-athletes
- Compliance-focused strategy development
- Brand building curriculum integration
- Collective partnership consultation
- Staff training and best practices

#### Athletes Tab
**Title:** Athlete Development
- Personal brand strategy and positioning
- Social media optimization
- Deal negotiation and structuring
- Long-term partnership development
- Financial literacy education

#### Brands Tab
**Title:** Brand Partnerships
- Athlete partnership matching
- Campaign strategy and execution
- NIL marketplace navigation
- ROI measurement and reporting
- Long-term ambassador programs

#### Workshops Tab
**Title:** NIL Workshops
- Interactive half-day or full-day sessions
- Personal branding masterclasses
- Social media strategy training
- Deal negotiation simulations
- Custom curriculum for your program

#### Speaking Tab
**Title:** Speaking Engagements
- Keynote presentations for conferences
- Athletic department staff meetings
- Student-athlete assemblies
- Industry panels and events
- Virtual and in-person availability

---

### 9. SPEAKING SECTION
**Tag:** Speaking
**Headline:** Book Trace for Your Next Event

**Description:** Whether it's a conference keynote, athletic department workshop, or student-athlete assembly, Trace delivers engaging presentations that inspire action.

**Popular Topics:**
- The New NIL Landscape: What Every Athlete Needs to Know
- Building Your Brand Before You Need It
- From Athlete to Entrepreneur: The Mindset Shift
- NIL Compliance Without Compromise

**CTA:** Inquire About Speaking

---

### 10. TESTIMONIALS
**Tag:** What Leaders Say
**Headline:** Trusted by Industry Leaders

| Name | Title | Quote |
|------|-------|-------|
| Jim Isch | NCAA Executive / Former COO | "Trace bridges the gap between athletes, brands, and universities in a way I haven't seen before. He understands the complexities of the NIL landscape." |
| Matt McMahon | LSU Head Basketball Coach | "Trace has built a powerful brand that serves as a model for student-athletes everywhere. His framework is practical and proven." |
| Ian Hamilton | Former Nike Global Marketing Director | "Trace has proven success building athlete brands. His framework for personal branding and deal-making is invaluable for any program." |
| Ronnie Hamilton | Louisville Assistant Coach | "Trace has the credibility to speak on NIL because he's lived it. His experience closing 70+ deals gives him a perspective that resonates with our athletes." |
| Rob Lanier | Rice Head Basketball Coach | "Trace understands NIL from every angle—athlete, brand, institution. That 360-degree perspective makes his insights uniquely valuable." |
| Chris Capko | SMU Assistant Coach | "The platform Trace has built gives athletes a real blueprint for success. It's not theory—it's actionable and it works." |
| Aaron Katsuma | Minnesota Assistant Coach | "What sets Trace apart is his authenticity. Athletes trust him because he's been in their shoes and built something real." |

---

### 11. CTA SECTION
**Headline:** Ready to Get Started?
**Subhead:** Let's discuss how The 99 can help your program, athletes, or brand succeed in the NIL era.

**Buttons:**
- Schedule a Call (gold)
- Email Us (outline)

**Email:** team@the99sports.com

---

### 12. FOOTER
Links: Athletes | Schools | Brands | Contact | Instagram
Copyright: © 2024 The 99. All rights reserved.

---

## Form Fields (for Framer Forms → Attio)

### Contact Form
1. **Name** (text, required)
2. **Email** (email, required)
3. **I am a...** (dropdown)
   - Athlete
   - University / Athletic Department
   - Brand / Company
   - Media / Press
   - Other
4. **Subject** (text)
5. **Message** (textarea, required)

---

## Zapier Setup (Framer → Attio)

1. Trigger: Framer Form Submission
2. Action: Create Attio Person
3. Field Mapping:
   - Name → Attio Name
   - Email → Attio Email
   - "I am a..." → Attio Type attribute
   - Message → Attio Notes
   - Set Source = "Website Form"

---

## Social Links
- Instagram: https://instagram.com/the99sports
- Twitter: https://twitter.com/the99sports
- LinkedIn: https://linkedin.com/company/the99sports
