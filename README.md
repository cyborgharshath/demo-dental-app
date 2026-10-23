# Clearwater Dental: demo website

A demo website for a dental clinic, in white and light blue. It has four public pages and a staff dashboard, and it runs in the browser with no build step.

Everything on the site is sample content: names, prices, reviews, phone number, email and address. Bookings are saved in the visitor's own browser only, and no messages are really sent.

## Pages

| Page | What it has |
| --- | --- |
| Home | Hero, treatments, how booking works, reviews, blog |
| About us | Clinic story, facilities, dentists, FAQs |
| Book appointment | Booking form with validation and spam protection |
| Contact | Map, phone, WhatsApp, email, hours, privacy policy, footer |
| Staff dashboard | Opens from the footer link on the Contact page |

Each page ends with a "See more" button that leads to the next one.

**Demo staff login:** username `admin`, password `smile2026`. This is for the demo only. A live site needs real accounts checked on a server.

## Folder structure

```
clearwater-dental/
  index.html            Page shell, loads the files below
  css/
    styles.css          All styles and animations
  js/
    config.js           Clinic details and small helper functions
    data.js             Sample data and browser storage
    store.js            Appointment slots, lookups and patient message text
    ui.js               Interface state, page titles, header and footer
    views-public.js     Home, About us and Contact pages
    views-booking.js    Book appointment page and form
    views-admin.js      Staff login and dashboard
    requirements.js     Requirements tracker shown in the dashboard
    app.js              Rendering, page changes and events
  assets/
    favicon.png         Browser tab icon
```

The scripts load in the order listed in `index.html`. Keep that order if you add or rename files.

## Run it on your computer

Open `index.html` in a browser. To serve it from a local address instead:

```
python3 -m http.server 8000
```

Then visit http://localhost:8000.

## Put it on GitHub

1. Create a new repository on GitHub, for example `clearwater-dental`.
2. Upload the contents of this folder, keeping the `css`, `js` and `assets` folders. With Git:

```
git init
git add .
git commit -m "Add Clearwater Dental demo site"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/clearwater-dental.git
git push -u origin main
```

3. To publish it, open the repository's Settings, choose Pages, select the `main` branch and the root folder, and save. GitHub shows the site address after a minute or two.

## Before a real launch

The Requirements tab in the dashboard marks each item as working in the demo, simulated, a production step or future. The main gaps are:

- A backend and database to store bookings (for example Supabase or PostgreSQL).
- Real staff accounts with access checks on the server.
- Real WhatsApp, SMS or email sending for confirmations and reminders.
- Real dentist photos, clinic details and patient-approved reviews.
- A Google Maps embed and a Google Business Profile.
- Legal review of the privacy policy, plus a full accessibility and security check.
