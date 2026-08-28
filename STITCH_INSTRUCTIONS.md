# Google Stitch Instructions

Use this repository as the product and design context for Ganj VPN.

## Read first

1. `DESIGN.md`
2. `PRODUCT_CONTEXT.md`
3. `reference/android-ui/GanjTheme.kt`
4. `reference/android-ui/GanjNavigation.kt`
5. `reference/android-ui/GanjConnectControl.kt`
6. `reference/android-ui/GanjVisualComponents.kt`

The Kotlin files are sanitized reference copies from the real Android project. They explain current behavior and state. **Do not merely restyle them.** Create a substantially more premium consumer UI while preserving the product model.

## First generation task — Connect screen only

Create one production-grade mobile **Connect** screen first. Do not generate the remaining application yet.

### Persistent navigation

The bottom navigation must use exactly five destinations:

- Home
- Servers
- **Connect**
- Store
- Profile

**Connect is the middle destination and must be elevated above the other four tabs.** It is the main product action and must visually dominate the navigation.

Do not place Connect as the first tab. Do not replace it with Home. Do not create a different navigation structure.

### Required Connect screen content

The screen must visibly include:

- Official supplied Ganj VPN logo
- Ganj VPN brand identity
- Current account/plan state
- Connection protection status
- Large central premium Connect control
- Disconnected / Connecting / Connected / Reconnecting / Failed visual variants
- Selected server with flag, country and city
- Live ping in milliseconds
- Server quality indicator
- Download and upload metrics when data exists; use dashes when it does not
- Change Server interaction
- Smart Connect action
- Premium upsell only for Free users
- Persistent bottom navigation with elevated center Connect tab

### Visual target

- premium pearl-white base
- modern emerald gemstone depth
- restrained metallic gold accents
- sophisticated Liquid Glass
- realistic readable UI density
- iOS-level refinement with Android practicality
- rounded but not childish
- soft layering and subtle reflections
- high contrast
- no generic dashboard
- no cyberpunk
- no excessive neon
- no fake glass on every surface

### Main Connect control

The hero control should be a signature brand object rather than a generic power button.

Use the official Ganj logo/diamond visual language inside the control, with:

- emerald translucent depth
- subtle gemstone facets
- concentric glass rings
- restrained gold micro-detail
- controlled radial glow
- calm breathing motion when connected
- slightly more active pulse when connecting

The control must remain unmistakably tappable.

### Server information

Show the selected server immediately below or near the hero control. Example realistic content:

**Germany — Frankfurt**  
Premium  
**24 ms**

Ping must be visible without opening another screen.

### Metrics

Use one compact segmented statistics surface:

- Ping — 24 ms
- Download — — before connected, realistic value when connected
- Upload — — before connected, realistic value when connected

Never fabricate an active speed before a connection exists.

### Motion

Specify:

- 180–240ms tab feedback
- soft spring for center Connect tab
- 220–320ms server-selection sheet transition
- reduced-motion variant
- slow connected breathing glow
- no constant distracting animation

## After approval

After the Connect screen is approved, create the Servers screen using the **same component library, navigation, palette, spacing, icon family and glass recipe**. Then continue Store → Home → Profile → Settings/Support.
