# BloodLink – Blood & Emergency Donor Network

A clean, responsive college mini project that connects people who urgently need blood with
nearby voluntary blood donors. Built with React, Vite, Tailwind CSS, and Lucide icons — no
backend, no external services. Demo data is stored in the browser using localStorage.

## Getting started

Requires Node.js 18 or newer.

```bash
npm install
npm run dev
```

Then open the printed URL (usually http://localhost:5173).

To create a production build:

```bash
npm run build
npm run preview
```

## Features

- **Home** – hero section, demo statistics with count-up animation, and clickable blood group
  cards that pre-filter the donor directory.
- **Find Donors** – filter donors by blood group, city, and availability; view details and
  reveal demo contact info.
- **Emergency Requests** – live board of active requests, sorted by urgency, with critical
  cases highlighted in red and an "I Can Donate" action.
- **Create Blood Request** – validated form; on submit the request is saved, appears on the
  board, and matching available donors (same group + same city) are shown instantly.
- **Become a Donor** – validated registration form with an eligibility confirmation checkbox;
  new donors appear in search immediately.
- **Dashboard** – live counts, recent requests table (with "mark completed"), donors-by-group
  bars, and a Reset Demo Data button.
- **Toasts** – small notifications for registrations, submissions, matches, and completions.
- **Persistence** – donors and requests survive page refreshes via localStorage.

## Project structure

```
src/
├── components/     # Navbar, Hero, cards, forms, filters, toasts, footer
├── pages/          # Home, FindDonors, EmergencyRequests, RequestBlood,
│                   # BecomeDonor, Dashboard, About, Privacy
├── context/        # AppContext – donors, requests, toasts + localStorage
├── data/           # Fictional sample donors and requests (first-run seed)
├── utils/          # Constants, time helpers, donor matching
├── App.jsx         # Routes and layout
├── main.jsx        # Entry point
└── index.css       # Tailwind layers + shared component classes
```

## Demo data

On first run the app seeds 13 fictional donors and 7 fictional emergency requests across
multiple cities and all 8 blood groups. Use **Dashboard → Reset Demo Data** to restore the
original sample data at any time. All names, phone numbers, emails, and hospitals are
invented — never enter real personal data while testing.

## Disclaimer

BloodLink is a demonstration project. Blood donation eligibility, compatibility, collection,
storage, and transfusion decisions must be handled by qualified healthcare professionals and
authorized blood banks. The matching feature uses simple exact blood-group matching for demo
purposes and is not a medical compatibility system.
