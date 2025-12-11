# The 99 - Attio CRM Organization Guide

## Overview
This guide outlines how to organize your Attio CRM to effectively manage leads from your Tally forms, segmented by contact type: Brands, Universities/Coaches, Athletes, and Media/Other.

---

## 1. Custom Attributes Setup

### Person Object - Add These Attributes

| Attribute Name | Type | Options | Purpose |
|----------------|------|---------|---------|
| **Contact Type** | Select | Brand, University/Coach, Athlete Waitlist, Media/Other | Primary segmentation |
| **Lead Source** | Select | Website Form, Waitlist, Referral, Social Media, Event, Cold Outreach | Track acquisition |
| **Lead Status** | Select | New, Contacted, Qualified, Proposal Sent, Closed Won, Closed Lost | Pipeline tracking |
| **Priority** | Select | High, Medium, Low | Prioritization |

### Brand-Specific Attributes

| Attribute Name | Type | Notes |
|----------------|------|-------|
| **Company Name** | Text | Link to Company object if available |
| **Industry** | Select | Apparel, Food & Beverage, Technology, Fitness, Financial, Automotive, Consumer Goods, Other |
| **Campaign Track** | Select | Platform, Managed, Agency, Discovery | Which form track they selected |
| **Campaign Type** | Multi-select | Social Posts, UGC, Ambassador, Event, Other | What they want athletes to do |
| **Payment Model** | Select | Pay Per Post, Pay Per View, Retainer, TBD | How they want to pay athletes |
| **Budget Range** | Select | Under $1K, $1K-$5K, $5K-$15K, $15K-$50K, $50K-$100K, $100K+, TBD | Total or per-athlete budget |
| **Athlete Count** | Select | 1-5, 5-10, 10-20, 20+ | Number of athletes needed |
| **Timeline** | Select | This Week, 2 Weeks, This Month, 1-3 Months, Planning | When they want to launch |

### University/Coach-Specific Attributes

| Attribute Name | Type | Notes |
|----------------|------|-------|
| **School Name** | Text | University/college name |
| **Role** | Select | Athletic Director, Associate AD, Head Coach, Assistant Coach, NIL Director, Compliance, SID, Other Staff |
| **Conference** | Select | SEC, Big Ten, Big 12, ACC, Pac-12, American, Mountain West, C-USA, Sun Belt, MAC, D2, D3, NAIA, Other |
| **Division** | Select | D1 Power 5, D1 Group of 5, D1 FCS, D2, D3, NAIA |
| **Services Needed** | Multi-select | Athlete Workshop, Staff Training, Keynote, Consulting, Collective Guidance |
| **Program Timeline** | Select | Immediate, Within 1 Month, 1-3 Months, Next Semester, Exploring |

### Athlete Waitlist Attributes

| Attribute Name | Type | Notes |
|----------------|------|-------|
| **School** | Text | Current university |
| **Instagram Handle** | Text | @handle format |
| **Waitlist Status** | Select | Waitlisted, Invited, Active, Churned | Track platform access |
| **Waitlist Date** | Date | When they joined the waitlist |
| **Referral Source** | Text | If they were referred by another athlete |

### Media/Other-Specific Attributes

| Attribute Name | Type | Notes |
|----------------|------|-------|
| **Organization** | Text | Company/publication |
| **Inquiry Type** | Select | Press, Speaking, Podcast/Interview, Partnership, General, Other |

---

## 2. Lists Structure

Create these Lists in Attio to organize and filter contacts:

### Primary Lists (by Contact Type)

```
📁 All Leads
├── 🏢 Brand Leads
│   └── Filter: Contact Type = "Brand"
├── 🏫 University Leads
│   └── Filter: Contact Type = "University/Coach"
├── 🏀 Athlete Waitlist
│   └── Filter: Contact Type = "Athlete Waitlist"
└── 📰 Media & Other
    └── Filter: Contact Type = "Media/Other"
```

### Pipeline Lists (by Status)

```
📁 Pipeline
├── 🆕 New Leads (This Week)
│   └── Filter: Lead Status = "New" AND Created < 7 days
├── 🔥 Hot Leads
│   └── Filter: Priority = "High" AND Lead Status != "Closed"
├── 📤 Proposals Out
│   └── Filter: Lead Status = "Proposal Sent"
└── ✅ Closed Won (This Quarter)
    └── Filter: Lead Status = "Closed Won" AND Closed Date = This Quarter
```

### Segment-Specific Lists

**Brand Lists (by Campaign Track):**
```
📁 Brand Segments
├── 🚀 Platform Track (Quick Campaigns)
│   └── Filter: Contact Type = "Brand" AND Campaign Track = "Platform"
├── 📋 Managed Track (Larger Campaigns)
│   └── Filter: Contact Type = "Brand" AND Campaign Track = "Managed"
├── 🎯 Agency Track (Specific Athletes)
│   └── Filter: Contact Type = "Brand" AND Campaign Track = "Agency"
├── 🤔 Discovery Track (Need Guidance)
│   └── Filter: Contact Type = "Brand" AND Campaign Track = "Discovery"
└── 💰 High Budget ($50K+)
    └── Filter: Contact Type = "Brand" AND Budget Range IN ["$50K-$100K", "$100K+"]
```

**University Lists:**
```
📁 University Segments
├── 🏆 Power 5 Programs
│   └── Filter: Contact Type = "University/Coach" AND Division = "D1 Power 5"
├── 🎓 Athletic Directors
│   └── Filter: Contact Type = "University/Coach" AND Role = "Athletic Director"
└── 📅 Booking Soon
    └── Filter: Contact Type = "University/Coach" AND Program Timeline IN ["Immediate", "Within 1 Month"]
```

**Athlete Waitlist Lists:**
```
📁 Athlete Waitlist Segments
├── 📋 Waitlisted
│   └── Filter: Contact Type = "Athlete Waitlist" AND Waitlist Status = "Waitlisted"
├── ✉️ Invited (Ready for Platform)
│   └── Filter: Contact Type = "Athlete Waitlist" AND Waitlist Status = "Invited"
└── ✅ Active Users
    └── Filter: Contact Type = "Athlete Waitlist" AND Waitlist Status = "Active"
```

---

## 3. Tally → Attio Integration

### Option A: Zapier Integration (Recommended)

**Zap 1: New Tally Submission → Create Attio Person**

```yaml
Trigger: New Tally Form Submission
Filter: Any submission from The 99 Contact Form

Action: Create/Update Attio Person
Mapping:
  - Email → email (lookup key)
  - Name → name
  - "I am a..." answer → Contact Type
  - All other fields → Respective custom attributes
  - Set Lead Status → "New"
  - Set Lead Source → "Website Form"
```

**Zap 2: Auto-assign Priority (Optional)**

```yaml
Trigger: New Attio Person Created
Filter: Contact Type = "Brand" AND Budget Range = "$50K+"
        OR Contact Type = "University/Coach" AND Division = "D1 Power 5"

Action: Update Attio Person
  - Priority → "High"
```

### Option B: Make.com Integration

Similar workflow structure, often more cost-effective for high volume.

### Field Mapping Reference

**Main Contact Form - Brand Fields:**
| Tally Field | Attio Attribute |
|-------------|-----------------|
| Email | email (default) |
| Your name | name (default) |
| "I am a..." | Contact Type = "Brand" |
| Company / Brand name | Company Name |
| Industry | Industry |
| What kind of campaign? | Campaign Track |
| What platform? | Campaign Type |
| What do you want athletes to do? | Campaign Type |
| Payment model? | Payment Model |
| Budget per athlete / Total budget | Budget Range |
| How many athletes? | Athlete Count |
| When do you want to launch? / Timeline | Timeline |

**Main Contact Form - University Fields:**
| Tally Field | Attio Attribute |
|-------------|-----------------|
| "I am a..." | Contact Type = "University/Coach" |
| School / University | School Name |
| Your role | Role |
| Conference | Conference |
| What do you need? | Services Needed |
| When are you looking to get started? | Program Timeline |

**Main Contact Form - Media Fields:**
| Tally Field | Attio Attribute |
|-------------|-----------------|
| "I am a..." | Contact Type = "Media/Other" |
| Organization | Organization |
| What is this regarding? | Inquiry Type |

**Athlete Waitlist Form:**
| Tally Field | Attio Attribute |
|-------------|-----------------|
| Email | email (default) |
| Your name | name (default) |
| School | School |
| Instagram handle | Instagram Handle |
| (auto-set) | Contact Type = "Athlete Waitlist" |
| (auto-set) | Lead Source = "Waitlist" |
| (auto-set) | Waitlist Status = "Waitlisted" |
| (auto-set) | Waitlist Date = submission date |

---

## 4. Workflow Recommendations

### Daily Workflow

1. **Morning Review**: Check "New Leads (This Week)" list
2. **Prioritize**: Move high-value leads to "Hot Leads"
3. **Outreach**: Contact leads by priority, starting with "Hot Leads"
4. **Update Status**: Move leads through pipeline stages after contact

### Lead Scoring Suggestion

Create a mental (or documented) scoring system:

**High Priority Indicators (+3 each):**
- Brand: Agency Track (specific athletes needed)
- Brand: Managed Track with $50K+ budget
- Power 5 Athletic Director
- Urgent timeline (this week)

**Medium Priority Indicators (+1 each):**
- Brand: Platform Track (quick campaigns)
- Brand: Discovery Track (need guidance)
- D1 university program
- 1-3 month timeline

**Low Priority (nurture):**
- Brand: Discovery Track with no budget yet
- University: Just exploring
- Media: General inquiry

### Response Time Targets

| Contact Type | Target Response Time |
|--------------|---------------------|
| Brand - Agency Track | < 4 hours |
| Brand - Managed Track ($50K+) | < 4 hours |
| Brand - Platform Track | < 24 hours |
| Brand - Discovery Track | < 24 hours |
| University/AD | < 8 hours |
| Other University | < 24 hours |
| Athlete Waitlist | Auto-response only |
| Media | < 24 hours |

---

## 5. Views & Dashboards

### Recommended Table Views

**All Leads View - Columns:**
```
Name | Email | Contact Type | Lead Status | Priority | Created Date | Last Activity
```

**Brand Pipeline View - Columns:**
```
Name | Company Name | Campaign Track | Payment Model | Budget Range | Timeline | Lead Status
```

**University Pipeline View - Columns:**
```
Name | School Name | Role | Conference | Services Needed | Program Timeline | Lead Status
```

**Athlete Waitlist View - Columns:**
```
Name | Email | School | Instagram Handle | Waitlist Status | Waitlist Date
```

---

## 6. Quick Setup Checklist

### Phase 1: Core Setup (Do First)
- [ ] Create "Contact Type" select attribute (Brand, University/Coach, Athlete Waitlist, Media/Other)
- [ ] Create "Lead Status" select attribute
- [ ] Create "Lead Source" select attribute (include "Waitlist")
- [ ] Create "Priority" select attribute
- [ ] Create 4 primary Lists (Brand, University, Athlete Waitlist, Media)

### Phase 2: Brand Attributes
- [ ] Create "Campaign Track" select (Platform, Managed, Agency, Discovery)
- [ ] Create "Campaign Type" multi-select
- [ ] Create "Payment Model" select
- [ ] Create "Budget Range" select
- [ ] Create "Athlete Count" select
- [ ] Create "Timeline" select

### Phase 3: Athlete Waitlist Attributes
- [ ] Create "School" text field
- [ ] Create "Instagram Handle" text field
- [ ] Create "Waitlist Status" select (Waitlisted, Invited, Active, Churned)
- [ ] Create "Waitlist Date" date field

### Phase 4: Integration (After Tally Forms Created)
- [ ] Set up Zapier/Make account
- [ ] Create Main Form → Attio Zap (with conditional Contact Type)
- [ ] Create Waitlist Form → Attio Zap (auto-set Athlete Waitlist type)
- [ ] Test with sample submissions
- [ ] Verify field mapping

### Phase 5: Optimization (Week 2+)
- [ ] Create Brand segment Lists by Campaign Track
- [ ] Create Athlete Waitlist segment Lists by status
- [ ] Set up auto-priority Zap for Agency/Managed high-budget
- [ ] Build custom views
- [ ] Refine based on actual lead patterns

---

## 7. Pro Tips

1. **Use Company Objects**: For brands, create Company records and link People to them. This lets you track multiple contacts at the same company.

2. **Notes Are Key**: After every call/meeting, add a Note to the Person record. Attio's AI can summarize these.

3. **Activity Tracking**: Connect your email to Attio to automatically log communications.

4. **Mobile App**: Use Attio's mobile app to update lead status on-the-go after meetings.

5. **Bulk Actions**: Use Lists to perform bulk status updates (e.g., mark all stale leads as "Closed Lost").

---

## Next Steps

1. Sign into Attio and create the core attributes (Phase 1)
2. Create your Tally form using the structure in `TALLY-FORM-STRUCTURE.md`
3. Get your Tally form ID and update site embeds
4. Set up Zapier integration
5. Test the full flow: Submit form → Check Attio → Verify data

---

*Document created for The 99 NIL Consulting*
