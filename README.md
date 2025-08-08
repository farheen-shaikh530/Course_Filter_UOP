# UOP Course Filter System

**Work in Progress 🚧**

A dynamic course equivalency search tool built with React.js to help students and advisors find international study abroad course matches with UOP credit equivalents.

---

##  Live Demo
Coming soon...

## Folder Structure
- `/src` – React components
- `/public` – Static assets
- `international_universities.json` – Course data file
- `uop_majors.json` – Majors list

---

##  Features
- Filter by **country**, **major**, **institution**, and **course code**
-  Accordion-based university grouping for better navigation
-  Admin-ready structured JSON integration
-  Responsive UI aligned with UOP brand guidelines
-  Helpful “no results found” messages
-  Clean dropdown logic with deduplicated values

---

##  Work In Progress
-  **Admin dashboard** for uploading or modifying course data
-  **CSV export** of search results for advisors
-  **Firebase authentication** with role-based access (Student vs Admin)
-  Real-time updates for course mappings (via GitHub Gist or JSON sync)
-  Integration-ready for Tableau dashboards (TRM-to-Tableau)

---
## Recent Changes (Aug 2025)
- Removed local `international_universities.json` and `uop_majors.json` dependencies.
- Integrated [Sheety API](https://sheety.co/) to fetch live data directly from Google Sheets/Excel.
- Benefits:
  - No need to redeploy app for data changes.
  - Countries, universities, and majors dropdowns update automatically when sheet is edited.
  - Cleaner state management since normalization happens on API response.
- Required columns in Sheety sheet:
  - **General tab**: `country`, `partner_university`, `partner_course_code`, `partner_course_name`, `pacific_course_code`, `pacific_course_name`, `pacific_major`, etc.
  - **Majors tab**: `major` (list of majors offered at UOP).
---

## To Run Locally

```bash
npm install
npm start
