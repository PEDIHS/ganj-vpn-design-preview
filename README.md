# Ganj VPN — Public Design Preview

This repository is a **sanitized UI/UX design handoff** for Google Stitch / Figma-style design agents.

It intentionally does **not** contain production backend code, credentials, secret locators, deployment configuration, payment internals, VPN provisioning secrets, or private infrastructure.

## Source of truth

The private production repository remains the engineering source of truth. This public repository exposes only the product/UI context needed to redesign the mobile application safely.

## Product

Ganj VPN is a consumer VPN super-app with a hybrid Free + Premium model. The product includes:

- Home / account overview
- Server discovery and Smart Connect
- Central VPN Connect experience
- Free and Premium server tiers
- Live connection state
- Ping / connection-quality presentation
- Subscription Store
- Purchase / verification states
- Account / device management
- Support, diagnostics and settings

## Main navigation — non-negotiable

The app uses five primary destinations in this exact conceptual order:

1. **Home**
2. **Servers**
3. **Connect** — elevated center tab and dominant product action
4. **Store**
5. **Profile / Account**

Do not move Connect into Home. Connect is the center of the product and must remain the visually dominant middle navigation item.

## Design direction

Read [`DESIGN.md`](./DESIGN.md) before generating any UI.

Core identity:

- Pearl / soft white base
- Emerald green functional brand color
- Refined gold Premium accents
- Controlled Liquid Glass
- Premium gemstone-inspired depth
- Modern mobile-first UX
- iOS-quality visual polish while remaining practical on Android
- Strong accessibility and compact-device support

## Engineering reference files

The `reference/android-ui/` directory contains sanitized copies of real Jetpack Compose UI foundations from the private app. They exist so a design agent can understand the current product architecture, states, colors, motion and navigation before proposing a redesign.

These reference files are **context**, not a restriction on visual quality. Preserve product behavior and information architecture, but substantially improve visual composition where `DESIGN.md` requires it.

## First task for the design agent

Start with the **Connect screen only**.

The Connect screen must visibly include:

- Official Ganj VPN logo
- Current protection/connection state
- Large premium Connect control
- Selected server
- Country/city
- Live ping
- Download / upload metrics when available
- Smart Connect
- Free/Premium state
- Persistent 5-item bottom navigation with **Connect elevated in the center**

After the Connect screen is approved, continue to Servers, Store, Home, Profile and supporting flows using the exact same design system.
