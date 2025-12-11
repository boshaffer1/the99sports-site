# The 99 - Tally Form Structure

## Overview
This document outlines the form structures for The 99's lead capture system. There are **3 separate Tally forms**:
1. **Main Contact Form** - For brands, universities, and media inquiries
2. **Athlete Waitlist** - Simple 4-field waitlist for platform access
3. (Optional) **University Form** - Can be embedded separately on universities page

---

# FORM 1: Main Contact Form

## PAGE 1: Segmentation (Entry Point)
**Title:** "Let's Get Started"
**Subtitle:** "Tell us who you are so we can best help you."

**Question 1:** "I am a..." (Required)
- Type: `Multiple Choice` (single select, card style)
- Options:
  - **Brand** - "I represent a company looking to work with athletes"
  - **University / Coach** - "I work with an athletic program"
  - **Media / Other** - "Press, speaking inquiries, or other"

**Logic Rules:**
- If "Brand" → Go to BRAND PAGE 1
- If "University / Coach" → Go to UNIVERSITY PAGE 1
- If "Media / Other" → Go to MEDIA PAGE 1

---

# BRAND FLOW

## BRAND PAGE 1: Basic Info
**Title:** "Brand Partnership"

**Q2: Your name** (Required)
- Type: `Short text`
- Placeholder: "Full name"

**Q3: Work email** (Required)
- Type: `Email`
- Placeholder: "you@company.com"

**Q4: Company / Brand name** (Required)
- Type: `Short text`
- Placeholder: "Your company"

**Q5: Industry** (Required)
- Type: `Dropdown`
- Options:
  - Apparel & Fashion
  - Food & Beverage
  - Technology
  - Fitness & Wellness
  - Financial Services
  - Automotive
  - Consumer Goods
  - Other

---

## BRAND PAGE 2: Campaign Type (ROUTING)
**Title:** "Tell us about your campaign"

**Q6: What kind of campaign are you planning?** (Required)
- Type: `Multiple Choice` (card style)
- Options:
  - **Quick social posts** - "A few athletes, simple deliverable"
  - **Larger or ongoing campaign** - "Multiple athletes, complex, or recurring"
  - **Specific athlete(s) in mind** - "I know who I want to work with"
  - **Not sure - need guidance** - "Help me figure out the best approach"

**Logic Rules:**
- If "Quick social posts" → PLATFORM TRACK
- If "Larger or ongoing campaign" → MANAGED TRACK
- If "Specific athlete(s) in mind" → AGENCY TRACK
- If "Not sure" → DISCOVERY TRACK

---

## PLATFORM TRACK (Quick Social Posts)

**Q7: What platform?** (Required, Multi-select)
- Type: `Checkboxes`
- Options:
  - Instagram
  - TikTok

**Q8: How many athletes?** (Required)
- Type: `Multiple Choice`
- Options:
  - 1-5
  - 5-10
  - 10-20
  - 20+

**Q9: Budget per athlete?** (Required)
- Type: `Dropdown`
- Options:
  - $25 - $50
  - $50 - $100
  - $100 - $250
  - $250 - $500
  - $500+
  - Not sure yet

**Q10: Payment model?** (Required)
- Type: `Multiple Choice`
- Options:
  - Pay per post (flat fee when completed)
  - Pay per view (based on performance)
  - Let's discuss

**Q11: When do you want to launch?** (Required)
- Type: `Multiple Choice`
- Options:
  - This week
  - Within 2 weeks
  - This month
  - Next month

**Q12: Brief description** (Required)
- Type: `Long text`
- Placeholder: "What should athletes post? Product, messaging, hashtags, any requirements..."

→ Go to THANK YOU PAGE (Platform)

---

## MANAGED TRACK (Larger Campaigns)

**Q7: What do you want athletes to do?** (Required, Multi-select)
- Type: `Checkboxes`
- Options:
  - Social posts (Instagram/TikTok)
  - Create UGC for your brand
  - Brand ambassador (ongoing)
  - Event appearance
  - Other

**Q8: Payment model?** (Required)
- Type: `Multiple Choice`
- Options:
  - Pay per post
  - Pay per view
  - Monthly retainer
  - Let's discuss

**Q9: Total campaign budget?** (Required)
- Type: `Dropdown`
- Options:
  - $5,000 - $15,000
  - $15,000 - $50,000
  - $50,000 - $100,000
  - $100,000+
  - Let's discuss

**Q10: Any athlete requirements?** (Optional, Multi-select)
- Type: `Checkboxes`
- Options:
  - Minimum follower count
  - Specific sport(s)
  - Specific school(s) or region
  - No requirements - open to recommendations

**Q11: Timeline** (Required)
- Type: `Multiple Choice`
- Options:
  - Ready to start
  - Within 1 month
  - 1-3 months
  - Just planning

**Q12: Tell us about your campaign** (Required)
- Type: `Long text`
- Placeholder: "Goals, creative direction, specific needs..."

→ Go to THANK YOU PAGE (Managed)

---

## AGENCY TRACK (Specific Athletes)

**Q7: Do you know which athletes you want?** (Required)
- Type: `Multiple Choice`
- Options:
  - Yes, I have specific names
  - No, but I have criteria (help me find them)

**Q8: What do you need help with?** (Required, Multi-select)
- Type: `Checkboxes`
- Options:
  - Finding the right athletes
  - Outreach and negotiation
  - Contract and compliance
  - Campaign management
  - All of the above

**Q9: Budget for this initiative** (Required)
- Type: `Dropdown`
- Options:
  - Under $10,000
  - $10,000 - $25,000
  - $25,000 - $50,000
  - $50,000+
  - Let's discuss

**Q10: Timeline** (Required)
- Type: `Multiple Choice`
- Options:
  - Urgent (this week)
  - Within 2 weeks
  - Within 1 month
  - Flexible

**Q11: Tell us more** (Required)
- Type: `Long text`
- Placeholder: "Who are you looking for? What's the goal?"

→ Go to THANK YOU PAGE (Agency)

---

## DISCOVERY TRACK (Not Sure)

**Q7: What are you trying to achieve?** (Required, Multi-select)
- Type: `Checkboxes`
- Options:
  - Brand awareness
  - Drive sales / conversions
  - Content creation
  - Build athlete relationships
  - Something else

**Q8: Budget range** (Required)
- Type: `Dropdown`
- Options:
  - Under $5,000
  - $5,000 - $25,000
  - $25,000 - $100,000
  - $100,000+
  - No budget yet

**Q9: Anything else we should know?** (Optional)
- Type: `Long text`
- Placeholder: "Tell us about your brand and goals..."

→ Go to THANK YOU PAGE (Discovery)

---

# UNIVERSITY FLOW

## UNIVERSITY PAGE 1: Basic Info
**Title:** "Athletic Program Inquiry"

**Q2: Your name** (Required)
- Type: `Short text`
- Placeholder: "Full name"

**Q3: Your role** (Required)
- Type: `Dropdown`
- Options:
  - Athletic Director
  - Associate / Assistant AD
  - Head Coach
  - Assistant Coach
  - NIL Director / Coordinator
  - Compliance Officer
  - Sports Information Director
  - Other Staff

**Q4: School / University** (Required)
- Type: `Short text`
- Placeholder: "University name"

**Q5: Conference** (Optional)
- Type: `Dropdown`
- Options:
  - SEC
  - Big Ten
  - Big 12
  - ACC
  - Pac-12
  - American
  - Mountain West
  - Conference USA
  - Sun Belt
  - MAC
  - Division II
  - Division III
  - NAIA
  - Other

**Q6: Work email** (Required)
- Type: `Email`
- Placeholder: "you@university.edu"

---

## UNIVERSITY PAGE 2: Needs

**Q7: What do you need?** (Required, Multi-select)
- Type: `Checkboxes`
- Options:
  - NIL education workshop for athletes
  - Staff training / best practices
  - Keynote / speaking engagement
  - Ongoing consulting partnership
  - Collective partnership guidance
  - Not sure yet - want to learn more

**Q8: When are you looking to get started?** (Required)
- Type: `Dropdown`
- Options:
  - Immediately
  - Within 1 month
  - 1-3 months
  - Next semester
  - Just exploring

**Q9: Anything else we should know?** (Optional)
- Type: `Long text`
- Placeholder: "Specific challenges, number of athletes, upcoming events..."

→ Go to THANK YOU PAGE (University)

---

# MEDIA / OTHER FLOW

## MEDIA PAGE 1
**Title:** "Media & Other Inquiries"

**Q2: Your name** (Required)
- Type: `Short text`
- Placeholder: "Full name"

**Q3: Email** (Required)
- Type: `Email`
- Placeholder: "your@email.com"

**Q4: Organization** (Optional)
- Type: `Short text`
- Placeholder: "Company, publication, or organization"

**Q5: What is this regarding?** (Required)
- Type: `Multiple Choice`
- Options:
  - Press / Media inquiry
  - Speaking engagement request
  - Podcast / Interview request
  - Partnership opportunity
  - General question
  - Other

**Q6: Tell us more** (Required)
- Type: `Long text`
- Placeholder: "Please provide details about your inquiry..."

→ Go to THANK YOU PAGE (Media)

---

# FORM 2: Athlete Waitlist

**SEPARATE FORM** - Simple, high-conversion waitlist for athletes

## Waitlist Page 1
**Title:** "Get Paid to Post"
**Subtitle:** "Join the waitlist for early access to The 99's athlete campaign platform"

**Q1: Your name** (Required)
- Type: `Short text`
- Placeholder: "Full name"

**Q2: Email** (Required)
- Type: `Email`
- Placeholder: "your@email.com"

**Q3: School** (Required)
- Type: `Short text`
- Placeholder: "University name"

**Q4: Instagram handle** (Required)
- Type: `Short text`
- Placeholder: "@yourhandle"

→ Go to WAITLIST THANK YOU PAGE

---

# THANK YOU PAGES

## Thank You - Platform (Brands)
**Title:** "Thanks! We'll create your campaign."
**Message:** "We've received your campaign details. Our team will set everything up and reach out within 24-48 hours to get you started."
**CTA:** "Follow us on Instagram" → @the99sports

## Thank You - Managed (Brands)
**Title:** "Thanks! Let's talk."
**Message:** "We're excited about your campaign. Someone from our team will reach out within 24 hours to schedule a call and scope out your project."
**CTA:** "Follow us on Instagram" → @the99sports

## Thank You - Agency (Brands)
**Title:** "Thanks! We'll be in touch."
**Message:** "Custom athlete partnerships are our specialty. We'll reach out within 24 hours to discuss your needs."
**CTA:** "Follow us on Instagram" → @the99sports

## Thank You - Discovery (Brands)
**Title:** "Thanks! Let's figure this out together."
**Message:** "We'll reach out within 24-48 hours to learn more about your brand and help you find the right approach."
**CTA:** "Follow us on Instagram" → @the99sports

## Thank You - University
**Title:** "Thanks for reaching out!"
**Message:** "We're excited to learn more about your program. Someone from our team will reach out within 24-48 hours to discuss how we can support your athletes."
**CTA:** "Learn more about our workshops" → /universities

## Thank You - Media
**Title:** "Message received!"
**Message:** "Thanks for getting in touch. We'll review your inquiry and respond within 24-48 hours."
**CTA:** "Back to homepage" → /

## Thank You - Athlete Waitlist
**Title:** "You're on the list!"
**Message:** "We'll reach out when it's your turn for early access. In the meantime, follow us for updates."
**CTA:** "Follow @the99sports on Instagram"

---

# TALLY SETTINGS

## Design
- Theme: Dark mode
- Primary color: #D4AF37 (gold)
- Font: System default
- Hide Tally branding: Yes (Pro feature)

## Notifications
- Email notifications: ON → team@the99sports.com
- Include all form responses in email

## Integrations
1. **Google Sheets** - Send all responses to a master sheet
2. **Zapier/Make** - Trigger to Attio CRM

## Hidden Fields (for tracking)
- `source` - Where they came from (homepage, brands page, etc.)
- `utm_source` - For campaign tracking
- `utm_medium`
- `utm_campaign`

---

# EMBED CODES

## Main Contact Form
```html
<iframe
  data-tally-src="https://tally.so/embed/MAIN_FORM_ID?alignLeft=1&hideTitle=1&transparentBackground=1&dynamicHeight=1"
  loading="lazy"
  width="100%"
  height="500"
  frameborder="0"
  title="The 99 Contact Form">
</iframe>

<script>
  var d=document,w="https://tally.so/widgets/embed.js",v=function(){"undefined"!=typeof Tally?Tally.loadEmbeds():d.querySelectorAll("iframe[data-tally-src]:not([src])").forEach((function(e){e.src=e.dataset.tallySrc}))};if("undefined"!=typeof Tally)v();else if(d.querySelector('script[src="'+w+'"]')==null){var s=d.createElement("script");s.src=w,s.onload=v,s.onerror=v,d.body.appendChild(s)}
</script>
```

## Athlete Waitlist Form
```html
<iframe
  data-tally-src="https://tally.so/embed/WAITLIST_FORM_ID?alignLeft=1&hideTitle=1&transparentBackground=1&dynamicHeight=1"
  loading="lazy"
  width="100%"
  height="400"
  frameborder="0"
  title="Athlete Waitlist">
</iframe>

<script>
  var d=document,w="https://tally.so/widgets/embed.js",v=function(){"undefined"!=typeof Tally?Tally.loadEmbeds():d.querySelectorAll("iframe[data-tally-src]:not([src])").forEach((function(e){e.src=e.dataset.tallySrc}))};if("undefined"!=typeof Tally)v();else if(d.querySelector('script[src="'+w+'"]')==null){var s=d.createElement("script");s.src=w,s.onload=v,s.onerror=v,d.body.appendChild(s)}
</script>
```

---

# INTERNAL ROUTING GUIDE

| Form Track | What They Selected | Your Action |
|------------|-------------------|-------------|
| **Platform** | Quick social posts | Create campaign on platform for them (concierge) |
| **Managed** | Larger/ongoing campaign | Sales call → scope project → send proposal |
| **Agency** | Specific athletes | High-touch sales → custom quote |
| **Discovery** | Not sure | Discovery call → educate → route appropriately |
| **Waitlist** | Athlete signup | Add to waitlist → notify when platform ready |

---

*Replace `MAIN_FORM_ID` and `WAITLIST_FORM_ID` with your actual Tally form IDs after creation.*
