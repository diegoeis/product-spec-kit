# Push Notifications System

**Version:** Complete
**Created on:** 10/30/2025
**Last updated:** 10/30/2025
**Status:** Approved

---

## TL:DR;

- **What** to solve: 
  - Users don't receive important event updates in the app in real-time
  - Low retention rate due to lack of proactive engagement
  - Users miss deadlines and opportunities by not being notified
  
- **Why** solve it: 
  - 68% of active users don't open the app daily (analytics data)
  - Competitors with push notifications have 3x better D7 retention (AppAnnie 2024 study)
  - Support receives 200+ tickets/month about "didn't know there was an update"
  
- **How** to solve: 
  - Native iOS/Android push notification system
  - Granular notification preferences by category
  - Smart delivery based on user behavior

---

## Problem or Opportunity Context

Our mobile app currently operates in "pull" mode - users need to open the app to see updates. This results in low engagement (only 32% of users are active weekly) and loss of critical opportunities. Churn analysis shows that 45% of users who cancel cite "didn't know there were new things" as a reason. Competitors with push notifications report 3-4x higher retention at 7 days. This is a fundamental capability expected in modern mobile apps and its absence puts us at a competitive disadvantage.

---

## Solution and Objective

We will implement a push notification system allowing users to receive important updates even with the app closed. We'll start with critical notifications (high-priority events) and allow granular preference control. Our differentiation will be "smart delivery" - an algorithm that learns the best time to notify each user based on their usage pattern, reducing notification fatigue. Objective: increase D7 retention from 32% to 50% in 3 months.

### First Version/Release

**Basic flow:**
1. User installs/updates app → Notification permission prompt
2. User accepts → Automatic preference setup (everything active by default)
3. System sends notification when relevant event occurs
4. User taps notification → App opens directly on event screen
5. User can go to Settings → Notifications to adjust preferences by category

**MVP must include:**
- Delivery infrastructure (iOS APNS + Android FCM)
- Notifications for 3 critical categories: Deadlines, Mentions, Important Updates
- Simple preferences screen (on/off per category)
- Deep linking to open correct screen
- Badge count on app icon

#### General Operating Requirements

- System MUST request notification permission during onboarding (iOS) or first send (Android)
- System MUST respect user settings (silent, DND, etc)
- Notifications MUST have clear title, informative body, and primary action
- System MUST deep link to relevant screen when tapping notification
- System MUST update app icon badge count with number of unread notifications
- System MUST allow disabling categories individually
- User MUST be able to disable all notifications at once
- System MUST send maximum 3 notifications per day per category (anti-spam)
- System MUST sync read/unread state across devices
- Notifications MUST work in foreground and background

#### Feature Descriptions

**Feature 1: Delivery System**
Infrastructure that sends notifications via APNS (iOS) and FCM (Android). Important because it's the technical foundation for all other features and ensures reliable delivery.

**Feature 2: Notification Categories**
Groups notifications into types (Deadlines, Mentions, Updates). Important because it allows granular control - user may want only deadlines, not mentions.

**Feature 3: Preferences Screen**
Interface that allows enabling/disabling categories. Important because it gives control to the user and reduces notification fatigue.

**Feature 4: Deep Linking**
Opens specific event screen when tapping notification. Important because it reduces friction - user goes directly where they need to be.

**Feature 5: Badge Count**
Number on app icon showing unread notifications. Important because it creates sense of urgency and increases app opening.

---

## Technical Fundamentals Considerations

**Stack:**
- Front-end: Swift (iOS) + Kotlin (Android)
- Back-end: Node.js + Express for notification service
- Database: PostgreSQL for preferences + Redis for token cache
- Queue: RabbitMQ to process batch sends

**External services:**
- Apple Push Notification Service (APNS) - iOS
- Firebase Cloud Messaging (FCM) - Android

**Internal services used:**
- Events API (already exists) - notification source
- Users API (already exists) - preferences and permissions
- New: Notification Service (to be created)

**Back-end flowchart:**

```
[Events API] 
    ↓ (publishes event)
[RabbitMQ] 
    ↓ (consumes)
[Notification Service]
    ↓ (fetches preferences)
[PostgreSQL]
    ↓ (filters users)
[Notification Service]
    ↓ (sends notification)
[APNS/FCM]
    ↓ (delivers)
[User device]
```

---

## Risk Mitigation

**Market Risk:**
- **Risk:** Users deny notification permission → **Mitigation:** Educate value before asking permission; allow reactivation later
- **Risk:** Notification fatigue causing uninstalls → **Mitigation:** Limit of 3/day per category; granular preferences

**Technical Risk:**
- **Risk:** APNS/FCM downtime → **Mitigation:** Automatic retry + in-app notification as fallback
- **Risk:** Service performance with millions of sends → **Mitigation:** Queue architecture + batch sending; load testing before launch

**Compliance Risk:**
- **Risk:** LGPD requires explicit consent → **Mitigation:** Permission prompt is opt-in; consent logs stored
- **Risk:** GDPR "right to be forgotten" → **Mitigation:** Endpoint to delete tokens when deleting account

---

## Potential in Numbers

### Financial Impact

**Impacted customers:** 100% of active base (estimated 50,000 users)

**Financial projection:**
- **Assumption 1:** 60% of users accept notifications (industry benchmark: 50-70% - Source: OneSignal State of Push 2024)
- **Assumption 2:** Notifications increase D7 retention from 32% to 50% (benchmark: +50% retention - Source: Localytics 2024)
- **Assumption 3:** Each 1% retention point = $2,000 additional MRR (calculation: average LTV $120 * conversion)

**Calculation:**
- Base with notifications: 50,000 * 60% = 30,000 users
- Retention increase: 18 percentage points (32% → 50%)
- Financial impact: 18 * $2,000 = **$36,000 additional MRR**
- Payback: ~2 months (dev cost $70,000 / $36,000)

**Data sources:**
- OneSignal "State of Mobile Push Notifications 2024"
- Localytics "Mobile App Engagement Report 2024"
- Internal analytics data (current retention, LTV)

### Indicators and Metrics to Monitor

**Product Metrics:**
- Notification opt-in rate - Goal: ≥60% of active users
- Successfully delivered notifications - Goal: ≥95% (excluding users without permission)
- Notification open rate - Goal: ≥40% (benchmark: 30-50%)
- Conversion rate (tap → action in app) - Goal: ≥70%
- Average time between notification and opening - Goal: <5 minutes (indicates relevance)

**Business Metrics:**
- D7 Retention - Goal: increase from 32% to 50%
- D30 Retention - Goal: increase from 18% to 28%
- DAU/MAU ratio - Goal: increase from 0.32 to 0.45
- Churn rate - Goal: reduce from 8% to 5% per month
- NPS related to "knowing about updates" - Goal: increase from 6 to 8

**Business indicators moved:**
- D7 Retention ↑ → Freemium→paid conversion ↑ → MRR ↑
- DAU ↑ → Engagement ↑ → Premium feature conversion ↑

---

## Users and Market

**Segment:** All mobile app users (iOS and Android)

**Main personas:**
1. **Laura, Project Manager** (35 years): Needs to know urgent deadlines even outside the app; high priority on deadline notifications
2. **Carlos, Freelance Designer** (28 years): Wants mention notifications in feedback; opens app 2-3x/day; risk of missing important comments
3. **Ana, Student** (22 years): Uses app sporadically; needs reminder of important events; without notifications, forgets the app

**How they solve today:**
- Open app manually several times a day (inefficient)
- Set up calendar reminders (laborious)
- Use email as fallback (slow, low open rate)
- Some use competitor apps that have push notifications

---

## Studies and Discoveries

**Study 1: Interviews with churned users (May 2024)**
- 15 qualitative interviews
- 67% mentioned "didn't know there was an update" as churn factor
- 80% said notifications would make them return

**Study 2: Competitor analysis**
- Asana, Trello, Notion have robust push notifications
- All allow granular control by category
- Smart timing (intelligent scheduling) is competitive differentiator

**Study 3: Prototype A/B test (June 2024)**
- 500 beta users
- Group with notifications had 2.8x more engagement
- Opt-in rate was 64% (above benchmark)

### Competitors and Other Solutions

**Asana:**
- Notifications by project, task, mention
- Smart timing (sends at best time)
- Digest mode (groups notifications)
- **Our differentiator:** Simpler, fewer categories (reduces fatigue)

**Trello:**
- Card, mention, deadline notifications
- Notification snooze
- Badge count
- **Our differentiator:** Smart delivery from MVP (Trello doesn't have)

**Slack:**
- Highly customizable notifications
- "Do not disturb" hours
- Custom keywords
- **Our differentiator:** More product-focused (not communication), fewer options = simpler

---

## Artifacts and Documentation

- [Figma: Notification and preferences designs](#) (fictional link)
- [Miro: User journey with notifications](#) (fictional link)
- [Document: Churned user interviews](#) (fictional link)
- [Spreadsheet: Competitor analysis](#) (fictional link)
- [Technical PRD: Notification service architecture](#) (to be created by engineering)

---

## Possible Future Evolution

**Release 2: Smart Notifications (Q1 2026)**
- Smart timing: algorithm learns best time to notify each user
- Digest mode: groups less urgent notifications in daily summary
- Rich notifications: images, action buttons, content preview

**Release 3: Advanced Personalization (Q2 2026)**
- Custom rule creation ("notify if X and Y")
- Notification snooze
- Custom keywords for alerts

**Release 4: Analytics and Insights (Q3 2026)**
- Notification dashboard for admins
- Message A/B testing
- Audience segmentation

**Long-term vision:**
Notifications become primary retention and engagement channel. System learns individual preferences and automatically optimizes timing/content. Reduces support costs by proactively alerting users to problems.

---

## Change History

| Date | Version | Change | Author |
|------|---------|--------|--------|
| 10/30/2025 | 1.0 | Initial creation | Diego Eis |

---

## Approvals

| Role | Name | Date | Status |
|------|------|------|--------|
| Product Manager | Diego Eis | 10/30/2025 | ✅ Approved |
| Tech Lead | [To be defined] | - | ⏳ Pending |
| Head of Product | [To be defined] | - | ⏳ Pending |