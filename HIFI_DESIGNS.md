# Hoora Car Wash — Hi-Fi Mobile Design Spec

This document defines high-fidelity (hi-fi) mobile UI designs for the requested booking and upsell journeys.

## Visual Language

- **Style:** clean, premium, conversion-focused.
- **Density:** low-to-medium; avoid clutter and over-explanation.
- **Primary rule:** one strong action per screen.
- **Tap optimization target:** 2 to 3 taps wherever possible.

## Design Tokens

### Colors

- `Brand/Primary`: `#FFD400`
- `Brand/PrimaryPressed`: `#E6BE00`
- `Text/Primary`: `#101114`
- `Text/Secondary`: `#667085`
- `Surface/Default`: `#FFFFFF`
- `Surface/Muted`: `#F7F8FA`
- `Border/Subtle`: `#E6E8EC`
- `Success`: `#16A34A`

### Typography

- **H1:** 28/34, Semibold
- **H2:** 22/28, Semibold
- **Title:** 18/24, Semibold
- **Body:** 16/22, Regular
- **Caption:** 13/18, Regular
- **Button:** 16/20, Semibold

### Spacing and Layout

- 4pt grid: 4, 8, 12, 16, 20, 24
- Horizontal padding: 16
- Card radius: 16
- Button radius: 12
- Sticky footer top radius: 16

## Flow 1 — New User Normal Booking

### Screen 1: Home — Choose Your Wash

- Top: `Your Car: Hyundai Venue`
- Title: `Choose Your Wash`
- Card 1 (recommended):
  - `Complete Wash`
  - `Exterior + Interior`
  - `₹399` and `75 mins`
  - Primary CTA: `Book Now`
- Card 2:
  - `Quick Wash`
  - `₹199` and `45 mins`
  - Secondary CTA: `Select`
- Card 3:
  - `Deep Clean`
  - `₹1299` and `3 hours`
  - Secondary CTA: `Select`
- No sticky cart bar.

### Screen 2: Select Slot

- Header: `Complete Wash`
- Horizontal date strip + available time slots
- Sticky CTA: `Confirm & Pay ₹399` (disabled until slot is selected)

### Screen 3: Review

- Service: `Complete Wash`
- Slot: `7 to 8 AM`
- Address: `Home`
- Primary CTA: `Pay ₹399`

### Screen 4: Success

- Title: `Booking Confirmed`
- Summary of service + slot
- Primary CTA: `Done`

**Expected taps:** 3 to 4

## Flow 2 — Wash Pack Discovery and Purchase

### Trigger

- User has no booking by T+7.

### Screen 1: Home Banner

- Banner title: `Starter Wash Pack`
- `3 Washes`
- `₹499`
- `Valid 30 Days`
- `Save ₹98`
- Primary CTA: `Buy Pack`

### Screen 2: Pack Details

- Title: `Wash Pack`
- `3 Quick Washes`
- `Valid 30 days`
- `Use anytime`
- Primary CTA: `Buy for ₹499`

### Screen 3: Payment + Success

- Payment CTA: `Pay ₹499`
- Success content: `You have 3 washes`
- Prompt: `Book your first wash now?`
- Actions:
  - Primary: `Book Now`
  - Secondary: `Later`

## Flow 3 — Wash Pack First Booking

### Screen 1: Select Slot

- Header: `Quick Wash`
- Slot selector only (no price)
- Primary CTA: `Confirm`

### Screen 2: Success

- Title: `Wash booked`
- Subtext: `2 washes remaining`
- Primary CTA: `Done`

**Expected taps after activation:** 2

## Flow 4 — Active Pack Returning User

### Screen 1: Home Shortcut

- Top card text: `You have 2 washes left`
- Supporting line: `Book next wash`
- Primary CTA: `Book Now`

### Screen 2: Slot Selection

- Slot selector
- Primary CTA: `Confirm`

### Screen 3: Success

- `Wash booked`
- Remaining balance shown
- CTA: `Done`

## Flow 5 — Add-on Flow (Simplified)

### Placement

- Appears **after slot confirmation** and before final completion.
- Must remain optional and skippable.

### Screen: Enhance Your Wash

- Title: `Enhance Your Wash`
- Toggle options:
  - `Dashboard Polish ₹39`
  - `Air Freshener ₹89`
  - `Underbody ₹89`
- Primary CTA: `Add & Continue`
- Secondary CTA: `Skip`

## Flow 6 — Post 3rd Wash Upsell

### Trigger

- After completion of the final included pack wash.

### Entry

- Push: `You completed your Wash Pack`

### Screen: Upgrade

- Prompt: `Enjoyed Hoora?`
- Offer: `Upgrade to Monthly Plan`
- Detail: `4 Washes / Month`
- Price: `₹999`
- Actions:
  - Primary: `Start Plan`
  - Secondary: `Book Single Wash`

## Flow 7 — Returning Non-Pack User Quick Book

### Screen 1: Quick Book

- Title: `Quick Book`
- Last service: `Complete Wash`
- Last slot: `Morning`
- Actions:
  - Primary: `Repeat & Select Slot`
  - Secondary: `Explore Other Washes`

### Screen 2: Slot + Pay

- Slot selector
- Primary CTA: `Confirm & Pay`

### Screen 3: Success

- `Booking Confirmed`
- CTA: `Done`

## What Is Explicitly Removed

- No expandable clutter in primary booking path
- No recommend checkbox
- No long itemized breakdown in core journey
- No cart page
- No confusing stacked pricing

## Tap Count Summary

- Normal booking: 3 to 4 taps
- Wash pack first booking: 2 taps
- Repeat booking: 2 taps

## Component Behavior Rules

- One primary CTA per screen
- Sticky CTA for slot/payment screens
- Add-ons never block booking completion
- Keep success screens concise with one final action
