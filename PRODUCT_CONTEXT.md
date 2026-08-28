# Ganj VPN — Product & Screen Context

This document summarizes the real mobile product structure that the design must preserve while improving the UI/UX.

## Real app architecture

The Android client is implemented with Jetpack Compose and uses a state-driven UI. The main product screens consume a shared `GanjUiState` and render server/service, connection and checkout state rather than hard-coded demo data.

Core state concepts currently represented in the app include:

- `ConnectionUiState`
- `ContentState`
- `ServiceUiModel`
- `PlanUiModel`
- `UiTier`
- checkout states
- enterprise/support states

The design may improve presentation substantially, but it should not invent a conflicting product model.

---

# Primary navigation

The core destinations are:

1. **Home**
2. **Servers**
3. **Connect**
4. **Store**
5. **Account / Profile**

For the redesign, **Connect is the elevated center tab and dominant action**.

---

# Connection model

The real client distinguishes these connection visual states:

- Disconnected
- Connecting
- Connected
- Reconnecting
- Failed
- Unavailable

The UI must provide a distinct but cohesive visual response for every state.

The connection flow is tied to the currently selected active service/server entitlement. If no eligible service exists, the user must be clearly routed to server/service selection rather than seeing a fake connect state.

## Connect screen must expose

- Current connection/protection state
- Current selected server/service
- Main Connect / Disconnect / Retry action
- Ping / quality where data exists
- Download and upload metrics when real values exist
- Smart Connect entry
- Clear path to change server
- Free/Premium status
- Relevant error/retry state

The main Connect control is a real stateful product action, not decorative art.

---

# Servers / Smart Routing

The current app has a server/service discovery surface (`SmartRoutingScreen`). Services can be active/inactive and belong to product tiers, including VIP/Premium-style tiers.

The redesigned Servers experience should improve the current card list into a consumer-grade browser with:

- Search
- All / Free / Premium / Favorites filters
- Smart Location / Smart Connect recommendation
- Country flag
- Country and city
- Tier badge
- Live ping
- Signal/quality representation
- Favorite action
- Clear selected/current server
- Locked Premium behavior only when needed

Do not hide ping behind a details screen.

---

# Home

Home is a product/account overview, not the primary VPN control.

Current Home responsibilities include:

- Showing connection readiness/protection summary
- Showing selected service
- Showing service tier
- Showing device allowance
- Entry to Connect
- Entry to My Services
- Entry to Store
- Verified subscription/security messaging

The redesign should keep these responsibilities but simplify the hierarchy and avoid duplicating the Connect hero screen.

---

# Store

The real Store consumes an actual catalog of plans and an actual checkout state.

Plan data includes concepts such as:

- product/plan identity
- tier
- benefits
- selected plan
- purchase action

Checkout includes meaningful states such as:

- Idle
- Authentication required
- Pending
- Verified
- Active
- Failure/retry paths

The redesign must show these states clearly and must not imply an instant successful purchase when the backend is still verifying it.

## Store UX goals

- High-conversion but trustworthy
- Current plan is obvious
- Recommended plan is obvious
- Benefits are scannable
- Price/duration hierarchy is clean
- Premium uses restrained gold
- Pending verification is reassuring rather than alarming
- Success ends with a clear route back to Connect

---

# Account / Profile

The account area represents real service ownership and device/account state.

Relevant product concepts include:

- owned services/subscriptions
- service state
- plan/tier
- device limit
- support/diagnostics
- bug reporting
- account/session-related status

Design it as a polished consumer profile, not an admin settings page.

---

# Responsive & accessibility requirements already present in engineering

The Android UI already contains responsive and accessibility policies. The redesign must preserve or improve them.

Important constraints:

- compact Android screens are first-class
- larger font scales must not break navigation
- minimum touch targets must remain accessible
- reduced motion must be supported
- reduced transparency/effects must remain usable
- status cannot be communicated only by color
- long labels must not destroy layout

---

# Motion behavior

Engineering already distinguishes motion policy from state. Design motion should therefore be specified as behavior, not baked into a static layout.

Connection motion should remain bounded and calm:

- Connecting / reconnecting can pulse more actively
- Connected uses slower breathing motion
- Reduced-motion users receive state changes without continuous animation
- Failure does not use a distracting red flashing animation

---

# Design agent instruction

Treat `DESIGN.md` as the desired visual target and this file as the behavioral/product contract.

Do **not** blindly copy the current reference UI. It is included to explain real state, architecture and constraints. Produce a substantial premium redesign while preserving real product behavior.
