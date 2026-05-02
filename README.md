# SIDF Front-End Re-engineering

A front-end re-engineering prototype for the **Saudi Industrial Development Fund (SIDF)** loan-request and workload-management portals. Built as a static HTML demo to showcase the redesigned user flows and admin tooling.

## Pages

| File | Purpose |
| --- | --- |
| `main.html` | Landing / login screen |
| `page2.html` | Project overview |
| `page3.html` | Loan-request multi-step form (license details, feasibility study, financials) with API connection simulator and live PDF preview |
| `admin.html` | Admin dashboard — KPI cards (new orders, active requests, pending approvals, API match rate) and order-detail table with live search |
| `workload.html` | Drag-and-drop distribution board — three parallel columns: incoming requests, distribution canvas (RM / PSD / MSD departments), and work groups |
| `employees.html` | Employee management |

## Features

- **API Connection Simulator** (`page3.html`) — one-click fill of license, authorization, commercial-registry, and owner data
- **Live Feasibility Study Preview** — A4-style PDF mock that updates as the form is filled
- **Drag-and-drop Workload Distribution** — drag requests onto employees, drag employees and requests into work groups
- **Live Search** — filter orders in admin and incoming requests in workload
- **RTL Arabic UI** with Cairo font

## Tech Stack

- Plain HTML (no build step)
- [Tailwind CSS](https://tailwindcss.com/) via CDN
- [Lucide Icons](https://lucide.dev/) via CDN
- Google Fonts (Cairo)

## How to Run

Open any `.html` file directly in a modern browser:

```
start main.html
```

Or serve the folder with any static server:

```
python -m http.server 8000
```

Then visit `http://localhost:8000/main.html`.

## Notes

This is a **front-end demo only** — there is no backend, no database, no real API. All data is hard-coded and all "API calls" are simulated with `setTimeout`. State resets on page reload.
