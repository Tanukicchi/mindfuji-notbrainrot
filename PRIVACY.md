# Privacy Approach

Privacy is a core design constraint of NotBrainRot.

The product is not intended to provide parents with a history of the content a child watches. Its purpose is to enforce a configured Screen Time intervention while minimizing unnecessary collection of personal data.

## On-device exercise processing

Exercise evaluation is designed to run on the Child device using Apple's Vision framework.

The intended flow is:

1. The child starts an exercise.
2. Camera input is analyzed locally.
3. The app evaluates repetitions and basic movement quality.
4. Only the result and required coordination state are used by the application flow.
5. Exercise video is not intended to be uploaded to the backend for parental viewing.

## Minimal coordination data

The backend is used for product coordination such as:

- device pairing
- parent / child relationships
- configuration
- connection state
- exercise-completion state where required

The architecture is designed to avoid collecting watched-content histories.

## Public repository

This repository contains only high-level product and architecture information.

No production credentials, private keys, signing assets, user data, or proprietary source code are published here.
