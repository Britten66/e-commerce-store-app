# Steem - Digital Gaming Storefront

## Overview
A frontend e-commerce web application inspired by the Steam platform, built entirely in React. This project simulates a complete digital storefront experience, featuring game discovery, dynamic routing, cart management, conditional user authentication flows, and a simulated checkout process.

## Tech Stack
* **React 18**
* **React Router DOM**
* **Vite**
* **Context API**

## Setup

```bash
cd steem-app
npm install
npm run dev
```

## Git Workflow
This repository follows a strict feature-branch workflow to ensure stable integration:

* `main` - Final production builds only.
* `dev` - Active integration branch for testing.
* `feature/*` - Isolated branches for active development.

**Development Lifecycle:**
1. Create a new feature branch originating from `dev`.
2. Work, test, and commit changes locally.
3. Merge completed feature branch back into `dev`.
4. Merge `dev` → `main` only for the final finalized submission.

## User Flow

```text
                          START
                            ↓
                    ┌───────────────┐
                    │ Landing Page  │
                    └───────────────┘
                            ↓
                    [Browse Games]
                            ↓
                 ┌──────────────────────┐
                 │ Store/Search Page    │
                 │ (Filter & Search)    │
                 └──────────────────────┘
                            ↓
                    [Add to Cart]
                            ↓
                    ┌──────────────┐
                    │  Cart Page   │
                    └──────────────┘
                            ↓
                [Proceed to Checkout]
                            ↓
                    ┌──────────────┐
                    │ Login Check? │
                    └──────────────┘
                      ↓            ↓
                Not Logged In   Logged In
                      ↓            ↓
              ┌──────────────┐     │
              │  Login Page  │     │
              └──────────────┘     │
                      ↓            │
                      └───────────┘
                            ↓
                   ┌──────────────┐
                   │Checkout Page │
                   └──────────────┘
                            ↓
                [Complete Purchase]
                            ↓
                 Order Confirmation
                            ↓
                          END
```

### Standard Interaction Paths
* **Guest User Checkout:** `Landing` → `Store` → `Cart` → `Login` → `Checkout` → `Confirmation`
* **Authenticated User Checkout:** `Landing` → `Store` → `Cart` → `Checkout` → `Confirmation`
* **Direct Navigation:** Users maintain the ability to navigate laterally to any primary view via the persistent global Navbar at any stage in the flow.

## Team
* Christopher Britten
* Justin Seaward
