<h1 align="center">Hi, I'm Felipe Rodrigues Leone 👋</h1>

<p align="center">
  <a href="https://git.io/typing-svg">
    <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=22&pause=1000&color=FF2E4D&center=true&vCenter=true&width=760&lines=Software+Engineer+%C2%B7+Real-time+%26+Multi-tenant+Systems;I+build+telemetry+platforms+and+offline-first+SaaS;From+device+to+dashboard%2C+at+scale" alt="Typing SVG" />
  </a>
</p>

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Felipe-R-L/Felipe-R-L/output/github-snake-red.svg" />
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/Felipe-R-L/Felipe-R-L/output/github-snake-red.svg" />
    <img alt="snake eating my contributions" src="https://raw.githubusercontent.com/Felipe-R-L/Felipe-R-L/output/github-snake-red.svg" />
  </picture>
</p>


<p align="center">
  <a href="https://www.linkedin.com/in/felipe-rodrigues-leone/" target="_blank">
    <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn">
  </a>
  <a href="mailto:leone.feliper@gmail.com">
    <img src="https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Gmail">
  </a>
  <a href="https://feliperl.space" target="_blank">
    <img src="https://img.shields.io/badge/Portfolio-feliperl.space-FF2E4D?style=for-the-badge&logo=vercel&logoColor=white" alt="Portfolio">
  </a>
  <img src="https://komarev.com/ghpvc/?username=felipe-r-l&label=Profile%20views&color=ff2e4d&style=for-the-badge" alt="profile views" />
</p>

---

### 👨‍💻 About Me

🇧🇷 **Software engineer working on real-time, multi-tenant systems** — IoT telemetry platforms at OMD do Brasil by day, my own SaaS products on the side. I take systems from the **device all the way to the dashboard**: ingestion pipelines, time-series storage, tenant isolation, and the UI on top.

- 🛰️ **High-throughput telemetry**: MQTT ingestion, queues, TimescaleDB hypertables and BI aggregations that stay fast as data grows.
- 🔐 **Multi-tenancy taken seriously**: isolation enforced in the database with per-request **Postgres RLS**, not only in application code — plus CASL for action-level authorization.
- 🧭 **Applied optimization when the problem asks for it**: I built a street-level **coverage-routing engine** (mixed CPP / capacitated arc routing) with turn costs on a line-graph and a PyVRP solver sidecar — benchmarked against the standard `egl` instances.
- 📴 **Offline-first product work**: PWAs that keep operating with zero network (IndexedDB + a sync outbox with idempotent replay).
- 🧱 **Architecture I can defend**: Clean Architecture, DDD and SOLID; monorepos (Nx, Turborepo) with business rules living in a single shared package, revalidated server-side.
- 🌐 Fluent in **English (C2)**, comfortable working directly with international clients and stakeholders.

🔭 **Currently building:** **Dallas Sync** — an offline-first, multi-tenant PMS SaaS for motels, running in a real business with real money on the line.

---

### 💼 Experience

**Fullstack Engineer @ OMD do Brasil** · *Aug 2024 – Present*

Core developer on three **multi-tenant IoT platforms** — precision agriculture, waste collection and heavy machinery — from device ingestion to the dashboard.

**🚜 OMD Farm** — precision-agriculture SaaS that ingests and visualizes planting telemetry from sugarcane fields.

- ⚡ Cut BI query times from **30s+ to under 2s** with TimescaleDB read models and indexing strategies.
- 🛰️ Built **"Uber-style" live machine tracking** over MQTT and orchestrated high-throughput ingestion with BullMQ.
- 🗺️ Shipped advanced map features (raw points + aggregated heatmaps) with the Google Maps API and weather layers.
- 🏗️ Set up **CI/CD** (GitHub Actions + Cloud Build) and Docker across dev/staging/prod, and helped migrate the codebase to an **Nx monorepo**.

**♻️ Gestão Eco 360** — telemetry and management for **waste-collection** operations: fleet, points, routes and environmental traceability.

- 🧭 Built a **street-level route-optimization engine** for collection: OpenStreetMap graph → **arc-routing (mixed CPP/CARP)** instance with per-arc costs and **turn penalties on a line-graph**, solved by a **PyVRP (hybrid genetic search)** sidecar with a heuristic fallback cascade (path-scanning → Or-opt → iterated local search). Benchmarked on the standard **`egl` instances**: **on par with Hexaly** at sector scale and **ahead of OR-Tools** across all groups, with a proven lower bound to measure the gap against.
- 🛣️ Self-hosted the geospatial stack it runs on — **OSRM with a collection-truck profile** plus open elevation data — and calibrated per-street speeds from real telemetry, so the plan matches what the truck can actually drive.
- 🗺️ Shipped the planner UI: A/B **route-variant studies** with a scoreboard, recommendation and promotion to vehicle/weekday, deadhead painted in red on the map, and truck playback over the drawn route.
- 🔐 Implemented **3-layer authorization** agreeing on tenant/branch per request: Better Auth (organization + team), **Postgres RLS** injected per request via `SET LOCAL` (**deny-all without scope**), and CASL for action decisions shared between front and back — plus a **video-telemetry microservice** (MDVR/FTCloud + FFmpeg) for live view, playback and alarms.

**⛏️ OMD Collect** — telemetry platform for **soil-sounding and mining drill rigs**, successor to the legacy OMD/HYDAC system.

- 🔧 Rebuilt the legacy platform **from scratch**, reusing the Eco 360 architecture: Turborepo, React + NestJS, Drizzle, TimescaleDB, Better Auth + CASL + RLS, MQTT ingestion over **EMQX**.
- 📈 Turned raw **CAN/J1939 and hydraulic sensor** signals into operational answers: live per-machine monitoring, free-form signal history with export, productivity (meters drilled, working hours, fuel and water) and **SPT boring logs** with blows per meter.
- 🔌 Shipped a **public query API** (OpenAPI 3.1 + integration guide) so customers pull their own telemetry into BI/ERP, plus embedded Power BI panels scoped per company.
- 🧱 Enforced module boundaries in CI (`dependency-cruiser` + Biome) so client-safe contracts never leak server-only database code.

---

### 🛠️ Tech Stack

<h3 align="left">Backend &amp; APIs</h3>
<br/>
<p align="left">
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/nestjs/nestjs-original.svg" height="30" align="center" alt="NestJS"/> <b>NestJS</b> &nbsp;&nbsp;&nbsp;
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/nodejs/nodejs-original.svg" height="30" align="center" alt="Node.js"/> <b>Node.js</b> &nbsp;&nbsp;&nbsp;
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/typescript/typescript-original.svg" height="30" align="center" alt="TypeScript"/> <b>TypeScript</b> &nbsp;&nbsp;&nbsp;
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/javascript/javascript-original.svg" height="30" align="center" alt="JavaScript"/> <b>JavaScript</b> &nbsp;&nbsp;&nbsp;
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/prisma/prisma-original.svg" height="30" align="center" alt="Prisma"/> <b>Prisma</b> &nbsp;&nbsp;&nbsp;
<img src="https://cdn.simpleicons.org/drizzle/C5F74F" height="30" align="center" alt="Drizzle ORM"/> <b>Drizzle</b> &nbsp;&nbsp;&nbsp;
<img src="https://cdn.simpleicons.org/zod/3E67B1" height="30" align="center" alt="Zod"/> <b>Zod</b> &nbsp;&nbsp;&nbsp;
<img src="https://cdn.simpleicons.org/betterauth/888888" height="30" align="center" alt="Better Auth"/> <b>Better Auth</b> &nbsp;&nbsp;&nbsp;
🛡️ <b>CASL</b> &nbsp;&nbsp;&nbsp;
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/python/python-original.svg" height="30" align="center" alt="Python"/> <b>Python</b> &nbsp;&nbsp;&nbsp;
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/fastapi/fastapi-original.svg" height="30" align="center" alt="FastAPI"/> <b>FastAPI</b> &nbsp;&nbsp;&nbsp;
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/java/java-original.svg" height="30" align="center" alt="Java"/> <b>Java</b>
</p>

<br/>

<h3 align="left">Data &amp; Messaging</h3>
<br/>
<p align="left">
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/postgresql/postgresql-original.svg" height="30" align="center" alt="PostgreSQL"/> <b>PostgreSQL</b> &nbsp;&nbsp;&nbsp;
<img src="https://cdn.simpleicons.org/timescale/FDB515" height="30" align="center" alt="TimescaleDB"/> <b>TimescaleDB</b> &nbsp;&nbsp;&nbsp;
🌍 <b>PostGIS</b> &nbsp;&nbsp;&nbsp;
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/redis/redis-original.svg" height="30" align="center" alt="Redis"/> <b>Redis</b> &nbsp;&nbsp;&nbsp;
🐂 <b>BullMQ</b> &nbsp;&nbsp;&nbsp;
<img src="https://cdn.simpleicons.org/mqtt/9C27B0" height="30" align="center" alt="MQTT"/> <b>MQTT</b> &nbsp;&nbsp;&nbsp;
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/supabase/supabase-original.svg" height="30" align="center" alt="Supabase"/> <b>Supabase</b> &nbsp;&nbsp;&nbsp;
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/firebase/firebase-original.svg" height="30" align="center" alt="Firebase"/> <b>Firebase</b>
</p>

<br/>

<h3 align="left">Cloud, DevOps &amp; Observability</h3>
<br/>
<p align="left">
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/googlecloud/googlecloud-original.svg" height="30" align="center" alt="GCP"/> <b>GCP</b> &nbsp;&nbsp;&nbsp;
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/docker/docker-original.svg" height="30" align="center" alt="Docker"/> <b>Docker</b> &nbsp;&nbsp;&nbsp;
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/githubactions/githubactions-original.svg" height="30" align="center" alt="GitHub Actions"/> <b>GitHub Actions</b> &nbsp;&nbsp;&nbsp;
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/terraform/terraform-original.svg" height="30" align="center" alt="Terraform"/> <b>Terraform</b> &nbsp;&nbsp;&nbsp;
<img src="https://cdn.simpleicons.org/nx/888888" height="30" align="center" alt="Nx"/> <b>Nx</b> &nbsp;&nbsp;&nbsp;
<img src="https://cdn.simpleicons.org/turborepo/EF4444" height="30" align="center" alt="Turborepo"/> <b>Turborepo</b> &nbsp;&nbsp;&nbsp;
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/grafana/grafana-original.svg" height="30" align="center" alt="Grafana"/> <b>Grafana</b> &nbsp;&nbsp;&nbsp;
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/prometheus/prometheus-original.svg" height="30" align="center" alt="Prometheus"/> <b>Prometheus</b> &nbsp;&nbsp;&nbsp;
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/digitalocean/digitalocean-original.svg" height="30" align="center" alt="DigitalOcean"/> <b>DigitalOcean</b>
</p>

<br/>

<h3 align="left">Frontend</h3>
<br/>
<p align="left">
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/angular/angular-original.svg" height="30" align="center" alt="Angular"/> <b>Angular</b> &nbsp;&nbsp;&nbsp;
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/react/react-original.svg" height="30" align="center" alt="React"/> <b>React</b> &nbsp;&nbsp;&nbsp;
<img src="https://cdn.simpleicons.org/nextdotjs/888888" height="30" align="center" alt="Next.js"/> <b>Next.js</b> &nbsp;&nbsp;&nbsp;
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/rxjs/rxjs-original.svg" height="30" align="center" alt="RxJS"/> <b>RxJS</b> &nbsp;&nbsp;&nbsp;
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/vitejs/vitejs-original.svg" height="30" align="center" alt="Vite"/> <b>Vite</b> &nbsp;&nbsp;&nbsp;
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/tailwindcss/tailwindcss-original.svg" height="30" align="center" alt="TailwindCSS"/> <b>Tailwind</b> &nbsp;&nbsp;&nbsp;
<img src="https://cdn.simpleicons.org/radixui/888888" height="30" align="center" alt="Radix UI"/> <b>Radix / shadcn</b> &nbsp;&nbsp;&nbsp;
📴 <b>PWA / IndexedDB</b> &nbsp;&nbsp;&nbsp;
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/sass/sass-original.svg" height="30" align="center" alt="Sass"/> <b>Sass</b> &nbsp;&nbsp;&nbsp;
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/bootstrap/bootstrap-original.svg" height="30" align="center" alt="Bootstrap"/> <b>Bootstrap</b> &nbsp;&nbsp;&nbsp;
🧩 <b>CoreUI</b> &nbsp;&nbsp;&nbsp;
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/html5/html5-original.svg" height="30" align="center" alt="HTML5"/> <b>HTML5</b>
</p>

<br/>

<h3 align="left">Data Viz &amp; Maps</h3>
<br/>
<p align="left">
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/chartjs/chartjs-original.svg" height="30" align="center" alt="Chart.js"/> <b>Chart.js</b> &nbsp;&nbsp;&nbsp;
<img src="https://cdn.simpleicons.org/apacheecharts/AA344D" height="30" align="center" alt="Apache ECharts"/> <b>ECharts</b> &nbsp;&nbsp;&nbsp;
<img src="https://cdn.simpleicons.org/googlemaps/4285F4" height="30" align="center" alt="Google Maps"/> <b>Google Maps</b> &nbsp;&nbsp;&nbsp;
<img src="https://cdn.simpleicons.org/mapbox/4264FB" height="30" align="center" alt="Mapbox"/> <b>Mapbox</b> &nbsp;&nbsp;&nbsp;
<img src="https://cdn.simpleicons.org/maptiler/008FF8" height="30" align="center" alt="MapTiler"/> <b>MapTiler</b> &nbsp;&nbsp;&nbsp;
<img src="https://cdn.simpleicons.org/openstreetmap/7EBC6F" height="30" align="center" alt="OpenStreetMap"/> <b>OSM / OSRM</b> &nbsp;&nbsp;&nbsp;
🧬 <b>PyVRP</b>
</p>

<br/>

<h3 align="left">Tooling &amp; Also Familiar</h3>
<br/>
<p align="left">
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/git/git-original.svg" height="30" align="center" alt="Git"/> <b>Git</b> &nbsp;&nbsp;&nbsp;
<img src="https://cdn.simpleicons.org/vitest/FCC72B" height="30" align="center" alt="Vitest"/> <b>Vitest</b> &nbsp;&nbsp;&nbsp;
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/playwright/playwright-original.svg" height="30" align="center" alt="Playwright"/> <b>Playwright</b> &nbsp;&nbsp;&nbsp;
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/notion/notion-original.svg" height="30" align="center" alt="Notion"/> <b>Notion</b> &nbsp;&nbsp;&nbsp;
<img src="https://cdn.simpleicons.org/obsidian/7C3AED" height="30" align="center" alt="Obsidian"/> <b>Obsidian</b> &nbsp;&nbsp;&nbsp;
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/trello/trello-plain.svg" height="30" align="center" alt="Trello"/> <b>Trello</b> &nbsp;&nbsp;&nbsp;
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/c/c-original.svg" height="30" align="center" alt="C"/> <b>C</b> &nbsp;&nbsp;&nbsp;
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/laravel/laravel-original.svg" height="30" align="center" alt="Laravel"/> <b>Laravel</b>
</p>

---

### 📊 GitHub Stats

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=Felipe-R-L&show_icons=true&include_all_commits=true&count_private=true&hide_border=true&title_color=FF2E4D&icon_color=FF6B6B&text_color=E6E6E6&bg_color=160B0E" alt="stats" height="165"/>
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Felipe-R-L&layout=compact&hide_border=true&title_color=FF2E4D&text_color=E6E6E6&bg_color=160B0E" alt="top langs" height="165"/>
</p>

<p align="center">
  <img src="https://streak-stats.demolab.com/?user=Felipe-R-L&hide_border=true&background=160B0E&border=160B0E&stroke=FF2E4D&ring=FF2E4D&fire=FF2E4D&currStreakNum=E6E6E6&currStreakLabel=FF2E4D&sideNums=E6E6E6&sideLabels=E6E6E6&dates=8B7B7E" alt="streak" />
</p>

<p align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=Felipe-R-L&bg_color=160B0E&color=FF6B6B&line=FF2E4D&point=FFFFFF&area=true&area_color=FF2E4D&hide_border=true" alt="activity graph" />
</p>

---

### 🌟 Featured Projects

**🚜 OMD Farm** · *NDA Protected*
Multi-tenant SaaS ecosystem for precision agriculture — telemetry visualization, real-time tracking and BI aggregations over sugarcane planting data.
Led major architectural decisions across front-end, back-end, CI/CD and deployments.
`Angular` · `NestJS` · `Prisma` · `PostgreSQL` · `TimescaleDB` · `MQTT` · `BullMQ` · `GCP`

**♻️ Gestão Eco 360** · *NDA Protected*
Multi-tenant platform for **waste-collection** telemetry and environmental traceability: fleet, points and routes on a live map, MQTT ingestion, time-series and MDVR video telemetry.
Home of the **coverage-routing engine** — arc routing (mixed CPP/CARP) with turn costs on a line-graph, PyVRP hybrid genetic search over a self-hosted OSRM network, benchmarked on the `egl` instances (on par with Hexaly at sector scale, ahead of OR-Tools) and exposed as A/B route studies in the planner.
`React 19` · `NestJS` · `Drizzle` · `PostGIS` · `TimescaleDB` · `MQTT` · `Python` · `PyVRP` · `OSRM` · `RLS` · `CASL`

**⛏️ OMD Collect** · *NDA Protected*
Multi-tenant telemetry for **soil-sounding and mining drill rigs**, successor to the legacy OMD/HYDAC platform: live machine monitoring, signal history, alarms, productivity (meters drilled, hours, fuel/water) and SPT boring logs.
Rebuilt from scratch on the Eco 360 architecture, with a public OpenAPI 3.1 query API so customers take their own telemetry to BI and ERP.
`React` · `NestJS` · `Drizzle` · `TimescaleDB` · `MQTT (EMQX)` · `Better Auth` · `CASL` · `Power BI`

**🏨 Dallas Sync** · *Private repo · in active development*
Offline-first **PMS SaaS for motels** — room map, folio, cash register/shift control, inventory and rate rules. Runs in a real business with real money, so correctness is the feature: amounts in **integer cents**, idempotent sync, and invariants backed by database constraints instead of app-level hope.
The front desk keeps working with **zero internet** (IndexedDB + sync outbox with idempotent replay), and every domain rule lives in one shared package revalidated on the server.
`React 19` · `NestJS` · `Drizzle` · `PostgreSQL + RLS` · `Better Auth` · `Zod` · `Vitest` · `Turborepo`

**🛍️ [Secret Boutique](https://github.com/Felipe-R-L/secret-boutique-pwa)** · *Solo build, end to end*
E-commerce **PWA** built from scratch: catalog with product variants, cart, checkout with Mercado Pago, order lifecycle and stock control, admin back-office, transactional e-mails and web push notifications.
`Next.js 16` · `React 19` · `Supabase` · `Tailwind` · `Radix / shadcn` · `Mercado Pago` · `Vercel`

**🎨 Also on the shelf** — [my-portfolio](https://github.com/Felipe-R-L/my-portfolio) ([feliperl.space](https://feliperl.space)), a [brutalist filmmaking portfolio](https://github.com/Felipe-R-L/filmmaking-portfolio) and the [Dallas Motel landing page](https://github.com/Felipe-R-L/dallas-motel-landing-page).

---

<p align="center"><em>Let's build something that scales!</em></p>
