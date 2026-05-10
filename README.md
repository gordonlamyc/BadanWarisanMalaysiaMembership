# Badan Warisan Malaysia - Membership & Community App

A web application built for **Badan Warisan Malaysia (BWM)** to manage memberships, donations, and event registrations — all in one place.

---

## About the App

Badan Warisan Malaysia is a non-profit heritage conservation organisation. This app serves as a digital platform for members and supporters to:

- Register and renew their BWM membership
- Make donations to heritage conservation campaigns
- Browse and register for heritage events and programmes
- Track their engagement through a Heritage Passport and Community Leaderboard

---

## Features

### Membership Management
- New member registration with full personal details and address
- Digital membership card with QR code for identity verification
- Admin QR code scanner to validate member cards at events
- Membership renewal with integrated payment flow

### Donations
- Donate to active heritage conservation campaigns
- View full donation history with receipts
- Multiple payment methods supported (FPX, GrabPay, Card)
- Leaderboard showcasing top donors to encourage community giving

### Event Registration
- Browse upcoming BWM heritage events and programmes
- View event details including date, time, location, and organiser
- Register and pay for events directly in the app
- My Tickets section to view all registered events

### Community & Engagement
- **Heritage Passport** — Collect stamps by visiting heritage sites. Complete all 6 sites to earn 10% off membership renewal.
- **My Journal** — Document and share event experiences with photos and reflections.
- **Community Wall** — View messages and testimonials from fellow supporters.
- **Leaderboard** — Rankings for top donors and top volunteers.
- **AI Heritage Assistant** — A chatbot to answer questions about BWM, events, membership, and heritage conservation.

### User Account
- Sign up and login with email authentication (via Supabase Auth)
- Edit profile (name, phone number)
- Notification and language settings
- Manage payment methods

---

## Tech Stack

| Layer       | Technology                          |
|-------------|--------------------------------------|
| Frontend    | React 18 + TypeScript                |
| Build Tool  | Vite                                 |
| Styling     | Tailwind CSS + Radix UI              |
| Icons       | Lucide React                         |
| Backend/DB  | Supabase (Auth + PostgreSQL)         |
| QR Code     | html5-qrcode, qrcode.react           |
| Forms       | React Hook Form                      |
| Charts      | Recharts                             |
| SMS         | Twilio                               |

---

## Getting Started

### Prerequisites

- Node.js (v18 or later)
- A Supabase project (free tier works)



## App Navigation

```
Home (Dashboard)
├── Membership Registration / Renewal
├── Leaderboard
├── AI Heritage Assistant
├── Community Wall
├── Heritage Passport (Quick Access)
└── My Journal (Quick Access)

Events
└── Event Details → Register & Pay

Donate
└── Campaign Donation → Payment

Profile
├── My Membership Card (with QR code)
├── Heritage Passport
├── Donation History
├── My Journal
├── Edit Profile
└── Settings
```

---

## Design System

The app uses a heritage-inspired visual identity:

| Token           | Value     | Usage                        |
|-----------------|-----------|------------------------------|
| Heritage Green  | #0A402F   | Headers, primary buttons     |
| Parchment Cream | #FFFBEA   | Page backgrounds             |
| Heritage Gold   | #B48F5E   | Accent icons, highlights     |
| Charcoal        | #333333   | Body text                    |
| White           | #FFFFFF   | Cards and surfaces           |

**Fonts:** Lora (headings, serif) and Inter (body text, sans-serif)

---

## Database Setup

Profile and membership data are stored in Supabase. The app uses:

- `auth.users` — Authentication and basic profile data (name, phone)
- Custom tables for memberships, donations, and event registrations (see migration SQL file)
- Row Level Security (RLS) enabled on all tables

See `DATABASE_SETUP.md` for a full breakdown of the data structure and optional profiles table setup.

---

## Project Structure

```
src/
├── components/       # All screen and UI components
├── contexts/         # Auth context and global state
├── lib/              # Supabase client and utilities
├── services/         # API service functions
├── styles/           # Global CSS
├── types/            # TypeScript type definitions
├── assets/           # Images and static files
└── App.tsx           # Main app with screen routing
```

---

## Contributing

This project is developed for Badan Warisan Malaysia. For contributions or issues, please open a pull request or contact the development team.

---

## Licence

This project is private and intended for use by Badan Warisan Malaysia only.

---

*Preserving Malaysia's built heritage — one membership at a time.*
