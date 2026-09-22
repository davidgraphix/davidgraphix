<h1 align="center">David Smart</h1>

<p align="center">
  <strong>Full-Stack Software Developer</strong>
</p>

<p align="center">
  Building production-ready web applications with React, Next.js, TypeScript, C# and ASP.NET Core.<br/>
  Based in Lagos, Nigeria.
</p>

<p align="center">
  <a href="https://davidsmart-portfolio-react.vercel.app/"><img alt="Portfolio" src="https://img.shields.io/badge/Portfolio-0B0B0B?style=flat-square&logo=vercel&logoColor=white" /></a>
  <a href="https://www.linkedin.com/in/david-smart-bamidele/"><img alt="LinkedIn" src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white" /></a>
  <a href="mailto:bamideledavidsmart40@gmail.com"><img alt="Email" src="https://img.shields.io/badge/Email-EA4335?style=flat-square&logo=gmail&logoColor=white" /></a>
</p>

---

## About

I'm a full-stack developer who builds and maintains real web applications end to end — the interface, the API it talks to, the database behind it, and the deployment that keeps it running.

On the frontend I work with **React, Next.js, TypeScript and Tailwind CSS**. On the backend I work with **C#, ASP.NET Core Web API and Entity Framework Core**, backed by **PostgreSQL** or **SQL Server**. I ship to **Vercel** and **Render**, and use **Docker** and **Supabase** in my deployment workflow.

I currently work on two production client platforms under contract, and I'm studying **Statistics at Yaba College of Technology (YABATECH)** while actively building my software engineering career.

## Experience

| Role | Organisation | Period |
| --- | --- | --- |
| Contract Full-Stack Software Developer | **PrintPalash** — printing & branding e-commerce platform | Aug 2025 – Present |
| Contract Full-Stack Software Developer | **Summy Solutions & Technology Ventures** — home-appliance e-commerce platform | Dec 2025 – Present |

On the Summy platform I also work alongside a junior collaborator I trained and currently guide on implementation tasks.

Earlier, while still learning, I contributed as a **Software Developer Intern** on **Go Vote**, a startup project founded by my mentor, working alongside the project team.

## What I Build

- **E-commerce platforms** — catalogue, cart, checkout, payment verification, order tracking
- **Admin dashboards** — orders, inventory, customers, payments, analytics, audit logs
- **REST APIs** — ASP.NET Core Web API with Entity Framework Core and relational databases
- **Authentication & authorization** — JWT access/refresh flows, role- and permission-based access
- **Business web applications** — internal tools, multi-role portals, HR and operations systems
- **Production deployments** — Vercel and Render, environment-driven configuration

## Tech Stack

<p align="center">
  <img src="https://skillicons.dev/icons?i=ts,react,nextjs,tailwind,cs,dotnet,postgres,supabase,docker,git" alt="Core stack" />
</p>

| Area | Technologies |
| --- | --- |
| **Frontend** | React · Next.js (App Router) · TypeScript · JavaScript · Tailwind CSS · TanStack Query · React Hook Form + Zod |
| **Backend** | C# · ASP.NET Core · ASP.NET Core Web API · Entity Framework Core · REST APIs · JWT authentication |
| **Databases** | PostgreSQL · SQL Server · Supabase |
| **Tools & Deployment** | Git · GitHub · Docker · Vercel · Render · Postman |

## Selected Projects

### Summy Solutions — Storefront & Admin Dashboard

Customer storefront and staff admin dashboard for a Nigerian electronics and appliances retailer, built against an ASP.NET Core backend. Contract work, actively developed.

**Tech:** Next.js 15 · React 19 · TypeScript (strict) · Tailwind CSS · TanStack Query & Table · React Hook Form + Zod · Zustand · Recharts

**Highlights:**
- Typed API client that unwraps the backend response envelope, surfaces field-level validation errors, and refreshes expired tokens transparently — concurrent 401s share a single in-flight refresh
- Guest cart in `localStorage` that merges into the server cart on login, behind one interface so components never branch on session state
- Checkout through a hosted payment gateway with server-side verification as the source of truth, and retry for unpaid orders
- Admin area covering orders, payments, refunds, inventory, media, roles and permissions, with admin mutations invalidating the public storefront cache and revalidating server-rendered product pages

[Repository](https://github.com/davidgraphix/summy-web) · [Live](https://www.summysolutions.com/)

---

### PrintPalash

Production e-commerce and branding site for a printing business, with a staff admin dashboard on top of an ASP.NET Core API. Built and maintained under contract.

**Tech:** Next.js · TypeScript · Tailwind CSS · Nodemailer · ASP.NET Core API (separate service)

**Highlights:**
- Admin sign-in proxied server-side: the long-lived refresh token stays in an `httpOnly` cookie the browser's JavaScript cannot read, and only a short-lived access token reaches the client
- Permission-gated admin dashboard — orders, products, categories, brands, customers, payments, staff, analytics and audit logs — with every backend call defined in one typed API module
- Public order tracking served through a same-origin proxy that validates tracking numbers before forwarding, keeping the API origin out of the public bundle
- Statically built public catalogue for fast, SEO-friendly product pages; printable job cards with tracking QR codes; order emails over SMTP
- Node-based test suite covering admin auth, permission rules and formatting

[Repository](https://github.com/davidgraphix/printpalash) · [Live](https://printpalash.com)

---

### Workeva — Workforce Management App

Web client for a multi-tenant HR and workforce platform: attendance, leave, tasks, departments, reporting and audit trails.

**Tech:** Next.js 16 · React 19 · TypeScript (strict) · Tailwind CSS 4 · TanStack Query · Supabase Auth · Recharts · Vitest · Playwright

**Highlights:**
- Full auth lifecycle — sign-up, email confirmation via a server-side code exchange, password reset, invitation preview and acceptance, and an onboarding wizard for new companies
- One data hook per API resource, with an in-house UI component layer (fields, dialogs, tables, toasts, state placeholders) shared across the app
- Authorization and tenant isolation deliberately enforced by the API, with the client treating hidden UI as presentation rather than a security control
- Unit tests with Vitest and end-to-end coverage with Playwright, plus a strict typecheck step

[Repository](https://github.com/davidgraphix/workeva-frontend)

---

### YCT Connect Plus

Campus learning platform with three separate role experiences — student, lecturer and administrator — on top of a JWT-secured REST API.

**Tech:** Next.js · TypeScript · Tailwind CSS · Zustand · Recharts · Cloudinary

**Highlights:**
- Role-aware routing: separate registration and login flows per role, each landing in its own dashboard
- Lecturer tools for uploading course materials, posting announcements and viewing class analytics; admin tools for users, departments, materials approval and reports
- Central fetch client that attaches the bearer token and normalises API errors in one place
- Cloudinary-backed file uploads and PDF export of reports

[Repository](https://github.com/davidgraphix/yct-connect-plus) · [Live](https://yct-connect-plus.vercel.app)

---

### SmartScheduler API

A compact ASP.NET Core Web API showing how I structure backend services: controllers, DTOs, EF Core data layer and token-based auth.

**Tech:** C# · ASP.NET Core 9 · Entity Framework Core · SQL Server · JWT Bearer

**Highlights:**
- Registration and login endpoints issuing signed JWTs, with full token validation (issuer, audience, lifetime, signing key) configured at startup
- Password hashing kept out of the controller in a dedicated helper, and roles assigned at registration
- EF Core `DbContext` with code-first migrations and a design-time factory
- Request/response DTOs separated from entity models

[Repository](https://github.com/davidgraphix/SmartSchedulerApi)

---

### RiseClear Property Services

Conversion-focused website for a Canadian property-cleaning business.

**Tech:** Next.js 14 (App Router) · TypeScript · Tailwind CSS · Framer Motion · Nodemailer

**Highlights:**
- Dedicated quote forms per service type with loading, success and error states
- Server-side contact route that notifies the business and sends the client an auto-reply
- SEO groundwork — metadata, OpenGraph and JSON-LD structured data
- Mobile-first responsive layout deployed on Vercel

[Repository](https://github.com/davidgraphix/riseclear) · [Live](https://www.risecleaning.ca/)

---

**More on my GitHub:** [BlackCircle](https://github.com/davidgraphix/blackcircle) (finance & markets platform) · [Summy storefront](https://github.com/davidgraphix/summysolutionsandtechnology) (catalogue, cart and checkout) · [Brandlift Technologies](https://github.com/davidgraphix/brandlift-technologies) · [Portfolio](https://github.com/davidgraphix/davidsmart-portfolio)

## Current Focus

- Advanced ASP.NET Core Web API development
- Full-stack architecture across a Next.js client and a .NET API
- Production-grade e-commerce systems
- PostgreSQL and database design
- Docker and deployment workflows
- Stronger engineering practices — typed contracts, testing, code review

## Education

**Yaba College of Technology (YABATECH)** — Statistics · currently studying

## Open to Opportunities

I'm actively looking for:

- Junior Software Engineer / Junior Full-Stack Developer roles
- Junior Frontend Developer, React and Next.js roles
- C# / ASP.NET Core backend roles
- Software engineering internships
- Remote or hybrid engineering teams

If you're hiring or want to talk about a role, the fastest way to reach me is [email](mailto:bamideledavidsmart40@gmail.com) or [LinkedIn](https://www.linkedin.com/in/david-smart-bamidele/).

## GitHub Activity

<p align="center">
  <img height="165" alt="David Smart's GitHub stats" src="https://github-readme-stats.vercel.app/api?username=davidgraphix&show_icons=true&hide_border=true&rank_icon=github&theme=transparent&title_color=2F81F7&icon_color=2F81F7&text_color=767676" />
  <img height="165" alt="Most used languages" src="https://github-readme-stats.vercel.app/api/top-langs?username=davidgraphix&layout=compact&langs_count=8&hide_border=true&theme=transparent&title_color=2F81F7&text_color=767676" />
</p>

## Contact

- **Email:** [bamideledavidsmart40@gmail.com](mailto:bamideledavidsmart40@gmail.com)
- **LinkedIn:** [david-smart-bamidele](https://www.linkedin.com/in/david-smart-bamidele/)
- **Portfolio:** [davidsmart-portfolio-react.vercel.app](https://davidsmart-portfolio-react.vercel.app/)
- **GitHub:** [@davidgraphix](https://github.com/davidgraphix)
