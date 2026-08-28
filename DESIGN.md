# DESIGN.md — Ganj VPN

## 0. Product identity

**Product:** Ganj VPN  
**Category:** Consumer VPN / subscription app  
**Primary platform:** Mobile-first, Android production app with iOS-level visual polish  
**Design objective:** Build a distinctive, premium, trustworthy VPN experience that feels modern, elegant and fast rather than technical, cyberpunk or generic.

This design system is the single visual source of truth. Every new screen must inherit the same tokens, navigation, spacing, component language and motion behavior.

---

# 1. Non-negotiable product rules

1. **Connect is the central product action.**
2. The **Connect tab must always be the visually dominant center item** in the bottom navigation.
3. Do not move Connect into Home.
4. The persistent bottom navigation must keep the same 5-item structure throughout the main app:
   - Home
   - Servers
   - **Connect** — center, elevated, primary
   - Store
   - Profile
5. Use the supplied **official Ganj VPN logo**. Do not invent, redraw, simplify or replace the logo.
6. Do not change the logo proportions or reinterpret the diamond/shield/G monogram.
7. The user must be able to identify current VPN state, selected server, ping, server quality, plan status and the next primary action within one glance.
8. Free and Premium states must be visually distinct, but never aggressive or spammy.
9. Do not use a generic dashboard aesthetic.
10. Do not use hacker/cyberpunk visuals.
11. Do not overload the interface with gradients, glass or glow.
12. Every main screen must be usable with one hand on a phone.

---

# 2. Brand character

The product should feel premium, confident, secure, refined, calm, fast, exclusive, modern, technically capable and approachable.

Visual metaphor: **premium emerald gemstone + precision technology + polished metal + translucent modern glass**.

The app should visually sit between luxury fintech, premium travel apps, top-tier VPN products and polished modern iOS products.

Do not make it look like a gaming app, crypto dashboard, hacker terminal, cheap VPN clone, enterprise admin panel or generic AI-generated mobile UI.

---

# 3. Core visual language

## 3.1 Main palette

### Light mode
- Background Primary: `#F7F8F5`
- Background Secondary: `#FFFFFF`
- Surface Soft: `#F1F5F0`
- Surface Glass: white with 60–78% opacity
- Emerald 900: `#063E2F`
- Emerald 800: `#07533C`
- Emerald 700: `#087A52`
- Emerald 600: `#0A9A65`
- Emerald 500: `#18B879`
- Emerald 300: `#70D8AC`
- Gold 700: `#A86F12`
- Gold 600: `#C68B22`
- Gold 500: `#D8A43A`
- Gold 300: `#F0CE78`
- Text Primary: `#12211B`
- Text Secondary: `#5F6E67`
- Text Tertiary: `#8C9993`
- Border Soft: `rgba(15, 64, 47, 0.10)`
- Success: `#139A64`
- Warning: `#D79B2E`
- Error: `#D94A4A`

### Dark mode
- Background Primary: `#07110D`
- Background Secondary: `#0B1812`
- Elevated Surface: `#10231A`
- Glass Surface: dark emerald-black with 58–72% opacity
- Text Primary: `#F5F8F6`
- Text Secondary: `#A9BBB2`
- Border Soft: `rgba(135, 222, 181, 0.14)`
- Emerald remains saturated
- Gold remains restrained and premium

## 3.2 Color behavior

Emerald is the **functional brand color** for connect, active states, healthy ping, selected server, active tab, success and Smart Connect.

Gold is the **premium/status color** for Premium badges, VIP/featured plans, subscription emphasis, paid-plan selection, upgrade accents and rare metallic details.

Never use gold for ordinary navigation or common controls.

---

# 4. Liquid Glass rules

Use **controlled Liquid Glass**, not glassmorphism everywhere.

Approved uses:
- bottom navigation container
- central Connect tab
- selected server card
- modal and bottom sheet
- premium plan card
- compact statistic cards
- top floating status card
- quick actions

Glass specification:
- high background blur
- subtle inner highlight
- fine 1px translucent border
- very soft shadow
- minimal tint
- readable content

Avoid glass on every card, bright rainbow reflections, excessive blur, low-contrast text and stacking more than two translucent layers.

---

# 5. Typography

Use a premium modern sans-serif.

For English mockups use SF Pro, Inter or an equivalent clean system sans. For Persian production use a modern high-legibility Persian sans with matching weights.

Hierarchy:
- Display: 32–36 / semibold
- Page title: 26–30 / semibold
- Section title: 20–22 / semibold
- Card title: 16–18 / semibold
- Body: 15–16 / regular
- Secondary: 13–14 / regular
- Caption: 11–12 / medium
- Numeric metric: 24–32 / semibold
- Ping metric: 15–18 / semibold

Do not overuse bold. Prefer clear hierarchy through spacing and size.

---

# 6. Grid, spacing and geometry

Use an 8pt spacing system with 4pt micro-adjustments.

Core spacing: 4, 8, 12, 16, 20, 24, 32, 40.

Phone page horizontal padding:
- 18–20pt compact phones
- 22–24pt large phones

Main card radius: 22–28pt. Small card radius: 16–20pt. Pills: capsule or 14–18pt radius.

Bottom navigation:
- floating glass container
- safe-area aware
- approximately 72–84pt visible height
- central Connect item elevated 12–18pt above nav baseline

Touch target: minimum 44×44pt.

---

# 7. Elevation and lighting

Use depth subtly. Card shadows should have low spread and very soft neutral/emerald tint.

Central Connect control may use emerald radial glow, a low-opacity golden ring accent in Premium state, glass reflection and layered concentric rings.

Never use large black shadows.

---

# 8. Iconography

Use refined outline icons with consistent stroke, slightly rounded geometry and compact legibility. Filled states are reserved for active navigation or strong state feedback.

Do not mix unrelated icon families. Flags should be clean and circular or softly rounded, not oversized.

---

# 9. Persistent navigation

The bottom navigation is a defining brand element.

Always use:
1. Home
2. Servers
3. **Connect**
4. Store
5. Profile

The Connect tab must be centered, larger than other tabs, elevated, use the official Ganj VPN logo where appropriate, visually communicate connection state and remain accessible from every major main-tab screen.

### Connect tab states

**Disconnected:** emerald-dark glass center button, subtle emerald rim, official logo visible, label Connect.

**Connecting:** animated outer ring, logo remains visible, subtle rotating/ripple indicator.

**Connected:** brighter emerald, calm glow, small success indicator.

**Error:** restrained error ring while preserving brand identity; never use alarming full-screen red.

---

# 10. Screen: Connect — PRIMARY HERO SCREEN

This is the most important screen in the entire app. It must look unique, premium and memorable.

## 10.1 Header
- left: official Ganj VPN logo + brand
- right: compact plan status / Premium badge
- optional notification icon
- airy composition

## 10.2 Connection status
Use a compact glass status surface near the hero control.

States:
- Not connected
- Connecting…
- Connected
- Reconnecting…
- Connection failed

Secondary message:
- Your connection is protected
- Your connection is unprotected

Avoid technical jargon.

## 10.3 Hero Connect control
Use a large circular or rounded-orb control approximately 180–220pt.

Visual:
- layered translucent emerald glass
- subtle gemstone facets inspired by official logo
- official Ganj mark inside
- concentric rings
- premium metallic gold micro-accent
- controlled reflection
- elegant depth

Disconnected: “Connect”. Connecting: “Connecting” with animated ring. Connected: “Connected” with connection duration below.

## 10.4 Ping and speed metrics
Directly below hero control, use one segmented glass statistics card:
- Ping
- Download
- Upload

Example: Ping 24 ms, Download 256 Mbps, Upload 98 Mbps.

Ping color:
- excellent: emerald
- moderate: warm amber
- poor: muted red

Do not show fake speed values before connection. Use “—” when unavailable.

## 10.5 Selected server
Use a large selected-server card.

Left: flag, country, city. Center: server class, Free/Premium badge, quality indicator. Right: live ping and Change/chevron.

Example: Germany / Frankfurt / Premium / 24 ms.

Tapping opens server selection.

## 10.6 Smart Connect
Provide a compact Smart Connect card with lightning icon, “Smart Connect”, “Choose the fastest available server” and one-tap action. Do not make it stronger than the main Connect control.

## 10.7 Premium upsell
For Free users use an elegant premium card with white/emerald glass, restrained gold detail, benefit-focused copy and an Upgrade CTA. No aggressive countdown or intrusive initial pop-up.

For Premium users replace it with plan summary or a useful account benefit card.

## 10.8 Recommended servers
If screen height permits, show only 2–3 compact recommended servers. Preserve Connect hero dominance.

---

# 11. Screen: Servers

The Servers screen must look like the same app as Connect.

Header: Servers + optional compact plan badge.

Search: large rounded “Search country or server” field with filter action.

Filters: All / Free / Premium / Favorites. Selected state uses emerald fill and white text.

Smart Location: lightning icon, “Smart Location”, “Fastest available server”, tap to connect/select.

Each server row includes:
- favorite star
- country flag
- country
- city
- Free/Premium badge
- live ping
- signal quality bars
- optional server load

Example: Netherlands / Amsterdam · Premium / 28 ms.

Ping must be visible without opening details:
- 0–60ms: emerald
- 61–120ms: neutral/amber
- 121ms+: amber/red depending on severity

Paid servers should remain visually attractive with a small gold crown/Premium pill; lock behavior occurs on selection rather than by greying the entire row.

---

# 12. Server selection interaction

Tapping the selected server from Connect opens a modern bottom sheet or full server browser. Preserve context, show current server, allow one-tap replacement, display ping and Free/Premium state.

Transition should feel shared-element-like, 220–320ms, with smooth spring behavior.

---

# 13. Screen: Home

Home is not Connect.

Focus on account snapshot, plan status, useful shortcuts, recent/recommended information, notifications, optional referral/campaign and a quick server/recent connection summary.

Do not duplicate the full Connect hero.

Possible sections: greeting + plan, current subscription, quick actions, recent connection, recommended server, account/device state and useful promotion.

---

# 14. Screen: Store

Store must look premium and conversion-focused.

Header: Store + current plan chip.

Hero: elegant white/emerald card with gold Premium accents showing current plan, expiration and upgrade opportunity.

Plan cards include:
- plan name
- duration
- final price
- old price only if there is a real discount
- feature summary
- device limit
- Premium server access
- CTA

Recommended plan is slightly larger with a subtle gold edge and “Recommended” label, never cartoonish.

Feature comparison can include Premium locations, speed priority, device limit, support and advanced features.

Purchase flow:
1. Select plan
2. Plan detail
3. Order summary
4. Payment method
5. Pending state
6. Success / failure

Success screen uses elegant emerald success, optional restrained gold sparkle, active plan summary and “Start Connecting” CTA.

---

# 15. Screen: Profile

Sections: user identity, plan, devices, notifications, support, settings, privacy and logout.

Profile header should be a premium glass card with avatar/identity, plan badge and subscription expiration. Do not make Profile look like a settings dump.

---

# 16. Settings

Use grouped native-feeling list sections for Auto Connect, connection preferences, protocol/advanced connection where appropriate, theme, notifications, language, privacy, diagnostics and About. Use switches sparingly.

---

# 17. Subscription states

Support all visual states:
- Free
- Trial
- Premium active
- Premium expiring soon
- Expired
- Payment pending

Gold is strongest only for active Premium, featured upgrade and purchase success.

---

# 18. Core UX states

Every critical screen needs loading, skeleton, empty, offline, error, retry, success, disabled and permission-denied states.

VPN-specific states:
- no internet
- server unavailable
- timeout
- VPN permission required
- reconnecting
- switching servers
- connection interrupted

Messages must be human-readable.

---

# 19. Motion system

Motion must feel premium, calm and responsive.

## Connect animation
Disconnected → Connecting: outer ring expands slightly, emerald glow increases, logo gets a subtle depth/reflection shift, thin ring begins controlled rotation and any particles/shimmer remain extremely subtle.

Connecting → Connected: ring closes smoothly, soft emerald pulse, one restrained gold highlight sweep and state label changes without layout jump.

Connected idle: no noisy constant animation; only slow breathing glow.

Disconnect: reverse animation and fade to calm inactive state.

## Tab animation
180–240ms, active icon lifts 2–4pt, text fades/slides minimally, central Connect button uses a soft spring.

## Cards
Slight 0.98 scale on press, no dramatic bounce.

## Bottom sheets
Spring-based with smooth dim layer and glass surface.

---

# 20. Responsive behavior

Design first for 360–430px Android widths.

Ensure no clipped labels, adaptive server rows, clean card stacking, slightly smaller Connect control on compact devices, stable bottom navigation and safe-area compliance.

---

# 21. Accessibility

Minimum requirements:
- strong text contrast
- 44pt touch targets
- no color-only status communication
- dynamic-text resilience
- clear active/inactive states
- readable ping and plan labels
- reduced-motion compatible states

---

# 22. Design consistency rules

Across every screen preserve the same bottom navigation, icon family, radius hierarchy, glass recipe, emerald/gold semantics, typography hierarchy, spacing rhythm, card depth and header style.

Do not redesign navigation differently per screen. Do not introduce a new accent color without a functional reason. Do not create unrelated one-off card styles.

---

# 23. AI generation instructions

1. Start with the design system.
2. Create **Connect** first.
3. Next create **Servers**.
4. Then Store.
5. Then Home.
6. Then Profile.
7. Then Settings and support flows.
8. Maintain one shared component library.
9. Never change the bottom navigation structure.
10. Never replace the official logo.
11. Preserve white + emerald + refined gold.
12. Use Liquid Glass selectively.
13. Every screen must look production-ready, not conceptual.
14. Use realistic content and realistic UI density.
15. Do not generate device frames unless specifically requested.
16. Prefer flat screen exports suitable for implementation/reference.
17. Show real interaction states as separate variants when needed.

---

# 24. First screen generation brief

Generate the **Connect screen** first.

Required visible elements:
- official Ganj VPN logo in header
- plan state
- notification entry if useful
- clear VPN protection state
- large premium central Connect control
- selected server
- live ping
- download/upload placeholders or values based on state
- Smart Connect
- optional premium card
- 5-item bottom navigation: Home / Servers / Connect / Store / Profile
- Connect must be the elevated center tab

Design language:
- premium light mode
- pearl white background
- emerald gemstone depth
- refined gold metallic micro-accents
- controlled Liquid Glass
- high-end mobile spacing
- clean readable type
- no excessive visual noise

After the Connect screen is approved, generate Servers using the exact same design system.
