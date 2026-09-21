# Technical Overview

NotBrainRot is primarily an iOS product, but the project spans several engineering domains.

## iOS application layer

The Parent and Child apps are developed in Swift / SwiftUI.

The project uses native Apple capabilities for:

- Screen Time authorization and app selection
- managed app shielding
- device activity handling
- on-device pose estimation
- cross-target shared state where needed
- notifications and device-health flows

## Exercise evaluation

Exercise evaluators use Apple's Vision pose observations as input.

The implementation focuses on practical mobile evaluation rather than generic pose visualization. Evaluators combine movement state, joint relationships, repetition transitions, and exercise-specific constraints.

Examples of implemented or actively developed evaluators include:

- squats
- high knees
- chain punches
- push-ups and further exercises

The evaluators are developed iteratively against real test behavior, including incomplete repetitions and common false-positive cases.

## Backend

Supabase provides PostgreSQL-backed coordination for the two-app system.

Backend responsibilities include:

- parent and child device records
- pairing flows
- child configuration
- connection-state handling
- selected server-side functions

The architecture separates backend coordination from camera-based evaluation.

## Apple platform integration

A major part of the engineering work is operating within Apple's protected Screen Time ecosystem.

This includes work with:

- FamilyControls
- ManagedSettings
- DeviceActivity
- entitlements
- provisioning and code signing
- App Groups
- TestFlight and App Store release preparation

## Product engineering

Because this is an independently developed product, the work also includes areas beyond implementation:

- product-flow design
- privacy decisions
- architecture trade-offs
- release planning
- backend data modeling
- debugging across multiple devices
- documentation of technical decisions

The private source repository remains the system of record for implementation details.
