# RoomSync — Room Reservation and Facility Scheduling

A responsive, dependency-free **HTML + CSS + vanilla JavaScript** room scheduling demonstration. No build tools or server required.

## Launch

Open `index.html` in a modern browser, or publish the repository using **GitHub → Settings → Pages → Deploy from a branch → main / (root)**. The URL will be `https://YOUR-USERNAME.github.io/REPOSITORY/`.

## Demo logins

- Administrator: `admin@roomsync.demo` / `admin123`
- Member: `user@roomsync.demo` / `user123`

You can also register a member account.

## Included

- Dashboard and facility cards
- Searchable facilities and administrator facility management
- Reservation requests, status tracking and cancellation
- Overlap detection for approved reservations (`startA < endB && startB < endA`)
- Approval/rejection with **re-check for conflicts at approval time**
- Monthly scheduling calendar
- Usage reports, room utilization counts, CSV export
- Responsive navy/blue interface with architectural background imagery

## IMPORTANT: limitations of GitHub Pages and localStorage

This is a **single-browser demo**, not a secure multi-user production service. All data, including demo passwords, is stored in `localStorage` in plain text. Login is a convenience UI, not secure authentication. Different browsers/devices **do not share** reservations, and users can inspect/change their local data. Do not enter real personal information or sensitive data. The included admin account is public demo-only. The calendar shows approved bookings and the current user's pending bookings; admins also see other pending bookings. Remote Unsplash images and Google Fonts require an internet connection; the app still operates without them.

For real shared bookings and security, add server-side authentication, a shared database, and server-enforced role permissions and conflict checks. GitHub Pages alone cannot provide these.

## Files

- `index.html` — single-page entry point
- `css/style.css` — design, components and responsive layout
- `js/app.js` — routing, local persistence, business rules, calendar, reports

## Reset demo

In your browser's developer console: `localStorage.removeItem('roomsync_v1'); sessionStorage.removeItem('roomsync_session'); location.reload();`
