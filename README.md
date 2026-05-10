# SIDF Front-End Re-engineering

A front-end re-engineering prototype for the **Saudi Industrial Development Fund (SIDF)** loan-request and workload-management portals. Built as a static HTML demo to showcase the redesigned customer journey, admin tooling, and Relationship-Manager (RM) workspace.

The UI is fully **RTL Arabic** with mobile-responsive layouts across every page.

## Pages

### Customer-facing

| File | Purpose |
| --- | --- |
| `index.html` | Landing page (Energy-sector microsite) and entry to the loan flow |
| `page2.html` | Customer dashboard — projects overview, status cards, detail modal |
| `page2-active.html` | Active-project variant of the dashboard with live phase tracking |
| `page3.html` | Loan-request multi-step form (license, feasibility study, financials) with API-fill simulator and live A4 PDF preview |
| `submitted.html` | Post-submission confirmation + ongoing project timeline / phase dots |

### Admin / back-office

| File | Purpose |
| --- | --- |
| `admin.html` | KPI dashboard (new orders, active requests, pending approvals, API match rate) with searchable orders table and risk highlighting |
| `workload.html` | Drag-and-drop distribution board — incoming requests → departments (RM / PSD / MSD) → work groups |
| `employees.html` | Employee management with quick-assign, edit, and delete actions |

### Relationship-Manager (RM) portal

| File | Purpose |
| --- | --- |
| `rm.html` | RM dashboard — assigned portfolio and phase overview |
| `rm-workload.html` | Group-level file distribution; lists all orders per group with inline per-order required-files checklist |
| `rm-tasks.html` | RM task queue — per-order missing-files checklist, upload, and submit |
| `rm-chats.html` | Customer conversations with a "request missing documents" checklist modal |

## Features

- **API Connection Simulator** (`page3.html`) — one-click pre-fill of license, authorization, commercial-registry, and owner data
- **Live Feasibility Study Preview** — A4-style PDF mock that renders all four sections as the form is filled
- **Drag-and-drop Workload Distribution** — drag requests onto employees, drag both into work groups (with a single-order cap per group on the RM side)
- **Missing-files Checklist** — per-order required-document tracking surfaced to both customer and RM
- **Live Search** — filter orders in admin and incoming requests in workload
- **Project Detail Modal** — shared modal across customer, admin, RM, and tasks views
- **Mobile-responsive** — sidebars collapse, timelines/phase-dots become horizontally scrollable on small screens

## Tech Stack

- Plain HTML (no build step)
- [Tailwind CSS](https://tailwindcss.com/) via CDN
- [Lucide Icons](https://lucide.dev/) via CDN
- Google Fonts (Cairo)

## How to Run

Open `index.html` directly in any modern browser, or serve the folder with a static server:

```
python -m http.server 8000
```

Then visit `http://localhost:8000/`.

The site is also deployable as-is to Netlify or any static host (`index.html` is the default entry).

## Notes

This is a **front-end demo only** — there is no backend, no database, no real API. All data is hard-coded and all "API calls" are simulated with `setTimeout`. State resets on page reload.
