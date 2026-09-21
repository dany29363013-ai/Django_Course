# Django Course Roadmap & Specifications

## 1. VERSION SPECIFICATIONS

**Django Version:** 5.0.x (Latest Stable as of January 2024)
- Current LTS: Django 4.2.x (supported until April 2026)
- We teach on 5.0 for latest features (async improvements, better validation)
- Note differences where 4.2 LTS behaves differently

**Django REST Framework:** 3.14.x (latest stable)

**SimpleJWT:** 5.3.x (latest stable, compatible with Django 5.0)

**Python:** 3.11+ (type hint improvements, performance gains)

---

## 2. COMPLETE COURSE ROADMAP

### PHASE 0: FOUNDATIONS (Total: ~8 hours)

| Module | Title | Description | Time |
|--------|-------|-------------|------|
| 0.1 | How the Web Actually Works | HTTP anatomy, client-server, REST vs SOAP, JSON, URL-to-response flow | 2h |
| 0.2 | Python Essentials for Django | Virtual envs, classes, decorators, context managers, type hints, env vars | 3h |
| 0.3 | What Django Is | MVT vs MVC, request lifecycle, WSGI/ASGI, batteries-included philosophy | 2h |
| 0.4 | Settings.py Masterclass | Complete settings breakdown, splitting configs, environ, security settings | 1h |

### PHASE 1: DJANGO CORE (Total: ~25 hours)

| Module | Title | Description | Time |
|--------|-------|-------------|------|
| 1.1 | Project Setup and Structure | startproject/startapp, file purposes, manage.py commands, app boundaries | 2h |
| 1.2 | URLs and Views | URL routing, path converters, FBV vs CBV, error handlers, reverse() | 3h |
| 1.3 | Models and the Database | Field types, Meta options, migrations deep dive, constraints, indexes | 4h |
| 1.4 | Relationships | ForeignKey, OneToOne, ManyToMany, through models, on_delete, related_name | 3h |
| 1.5 | The ORM Deep Dive | QuerySet methods, Q/F objects, aggregation, annotation, N+1 problem | 4h |
| 1.6 | Transactions and Concurrency | atomic(), savepoints, select_for_update(), race conditions, F expressions | 2h |
| 1.7 | The Admin | ModelAdmin, inlines, filters, actions, custom views, securing admin | 2h |
| 1.8 | Templates, Static and Media | Template language, inheritance, static files, uploads, S3 storage | 2h |
| 1.9 | Forms | Form/ModelForm, validation flow, CSRF, why forms still matter | 2h |
| 1.10 | Middleware, Signals, Settings Internals | Middleware chain, custom middleware, signals (and when NOT to use) | 2h |
| 1.11 | Sessions, Cookies, Messages, Caching | Session backend, cookie flags, cache framework, per-view caching | 2h |
| 1.12 | Testing Django Basics | TestCase, Client, pytest-django, factories, coverage, test DB behavior | 3h |

### PHASE 2: DRF - DJANGO REST FRAMEWORK (Total: ~20 hours)

| Module | Title | Description | Time |
|--------|-------|-------------|------|
| 2.1 | REST API Design Principles | Resource URLs, HTTP verbs, idempotency, status codes, versioning | 2h |
| 2.2 | Serializers | Serializer vs ModelSerializer, validation, nested serializers, money/dates | 3h |
| 2.3 | Views in DRF | @api_view, APIView, generics, viewsets, routers, hook methods | 3h |
| 2.4 | Requests, Responses, Parsers, Renderers | Request.data, content negotiation, custom renderers, file uploads | 2h |
| 2.5 | Pagination, Filtering, Searching, Ordering | PageNumber/LimitOffset/Cursor, django-filter, SearchFilter | 2h |
| 2.6 | Exception Handling and Error Design | DRF exceptions, custom handler, error envelopes, validation errors | 2h |
| 2.7 | Throttling and Rate Limiting | AnonRate/UserRate throttles, scoped throttles, custom throttle classes | 2h |
| 2.8 | API Documentation | OpenAPI/Swagger with drf-spectacular, auth docs, examples | 2h |
| 2.9 | Testing APIs | APIClient, testing permissions/auth, validation error testing | 2h |

### PHASE 3: AUTHENTICATION AND AUTHORIZATION (Total: ~18 hours)

| Module | Title | Description | Time |
|--------|-------|-------------|------|
| 3.1 | Auth Concepts | AuthN vs AuthZ, sessions vs tokens vs JWT, stateless vs stateful | 2h |
| 3.2 | Django's Built-in Auth System | User model, password hashing internals, permissions, groups | 2h |
| 3.3 | Custom User Models | AbstractUser vs AbstractBaseUser, email login, migration strategies | 3h |
| 3.4 | DRF Authentication Classes | SessionAuth, BasicAuth, TokenAuth, custom auth classes | 2h |
| 3.5 | JWT Authentication in Depth | JWT anatomy, simplejwt setup, token rotation, blacklisting, storage trade-offs | 4h |
| 3.6 | Registration, Login, Account Flows | Registration validation, email verification, password reset, OTP concepts | 3h |
| 3.7 | Social and Third-Party Login | OAuth2/OpenID Connect, Google login with allauth | 2h |
| 3.8 | Authorization | Permission classes, object-level permissions, RBAC, multi-tenancy patterns | 3h |

### PHASE 4: SECURITY (Total: ~8 hours)

| Module | Title | Description | Time |
|--------|-------|-------------|------|
| 4.1 | Web Security for Django Developers | OWASP Top 10, SQL injection, XSS, CSRF, CORS, HTTPS, secrets management | 4h |
| 4.2 | Production Security Checklist | check --deploy, security middleware, file upload security, webhook signatures | 2h |
| 4.3 | Multi-Tenant Security Patterns | Tenant isolation, preventing data leaks, schema strategies | 2h |

### PHASE 5: ADVANCED DJANGO / DRF (Total: ~20 hours)

| Module | Title | Description | Time |
|--------|-------|-------------|------|
| 5.1 | Performance and Optimization | Profiling, query counting, indexes, Redis caching, connection pooling | 3h |
| 5.2 | Background Tasks with Celery | Celery + Upstash Redis, retries, scheduling, idempotent tasks | 3h |
| 5.3 | Async Django and Channels | Async views, async ORM calls, WebSockets, real-time features | 4h |
| 5.4 | Fintech-Grade Patterns | DecimalField, ledger systems, idempotency keys, webhooks, audit logs | 4h |
| 5.5 | Custom Management Commands | Writing commands, fixtures, data seeding, deployment automation | 2h |
| 5.6 | Third-Party Package Tour | django-environ, cors-headers, debug-toolbar, sentry, when to add deps | 2h |
| 5.7 | Service Layer Architecture | Fat models vs service layer, selectors, organizing complex logic | 2h |

### PHASE 6: PRODUCTION (Total: ~15 hours)

| Module | Title | Description | Time |
|--------|-------|-------------|------|
| 6.1 | PostgreSQL with Django | Config, migration from SQLite, JSON fields, full-text search | 2h |
| 6.2 | Configuration and Twelve-Factor | Environment variables, secrets, .env handling, django-environ | 2h |
| 6.3 | Docker and Docker Compose | Containerizing Django, Postgres, multi-stage builds, volumes | 3h |
| 6.4 | Gunicorn/Uvicorn Production Setup | Workers, threads, async workers, process management | 2h |
| 6.5 | Deployment Walkthrough | Railway/Render/Fly.io deployment, environment setup, migrations | 3h |
| 6.6 | Logging, Monitoring, Error Tracking | Structured logging, Sentry integration, health checks | 2h |
| 6.7 | CI/CD with GitHub Actions | Test pipelines, linting, auto-deploy on merge | 2h |

### PHASE 7: CAPSTONE PROJECTS (Total: ~25 hours)

| Module | Title | Description | Time |
|--------|-------|-------------|------|
| 7.A | Capstone A: Expense Tracker API | Categories, budgets, recurring expenses, CSV export, single currency | 10h |
| 7.B | Capstone B: Loan Management Backend | Loan products, approval workflow, repayment schedules, webhooks, RBAC | 15h |

**TOTAL ESTIMATED STUDY TIME: ~139 hours**

---

## 3. DESIGN SYSTEM SPECIFICATIONS

### Color Palette (Dark Brown Theme)

```
Primary Colors:
- #1a1210 (darkest brown - background)
- #2d1f1a (dark brown - sidebar/cards)
- #4a3728 (medium brown - borders/accents)
- #8b6c5c (light brown - secondary text)
- #c9a88c (tan - primary text)
- #f5e6d3 (cream - headings/highlights)

Accent Colors:
- #d4a574 (golden brown - links/buttons hover)
- #a67c52 (copper - active states)
- #8b4513 (saddle brown - warnings)
- #cd853f (peru - callout backgrounds)

Semantic Colors:
- #4a7c59 (muted green - success/positive)
- #c44536 (muted red - errors/danger)
- #3d6b8f (muted blue - info)
- #d4a04a (muted gold - warnings)
```

### Typography

```
Headings: 'Playfair Display', serif (elegant, book-like)
Body: 'Inter', sans-serif (clean, readable)
Code: 'JetBrains Mono', monospace (developer-friendly)

Hierarchy:
- H1: 2.5rem, #f5e6d3, bold
- H2: 2rem, #f5e6d3, semibold
- H3: 1.5rem, #c9a88c, medium
- H4: 1.25rem, #c9a88c, medium
- Body: 1rem, #c9a88c, normal
- Small: 0.875rem, #8b6c5c, normal
- Code: 0.9rem, #e8dcc8, normal
```

### Component Styles

**Callout Boxes:**
- Key Idea: Left border 4px solid #d4a574, background rgba(212,165,116,0.1)
- Warning: Left border 4px solid #cd853f, background rgba(205,133,63,0.1)
- Common Mistake: Left border 4px solid #c44536, background rgba(196,69,54,0.1)
- Real-World Example: Left border 4px solid #4a7c59, background rgba(74,124,89,0.1)
- Anime Analogy: Left border 4px solid #3d6b8f, background rgba(61,107,143,0.1)
- Best Practice: Left border 4px solid #4a7c59, background rgba(74,124,89,0.1)
- Under the Hood: Left border 4px solid #8b6c5c, background rgba(139,108,92,0.1)

**Code Blocks:**
- Background: #241a15
- Border: 1px solid #4a3728
- Rounded corners: 8px
- Copy button: Top-right, subtle hover effect

**Navigation Sidebar:**
- Fixed position, dark brown background
- Section links with smooth scroll
- Active section highlighted with golden accent
- Progress bar at top showing completion percentage

**Exercise Solutions:**
- Collapsible details/summary elements
- Closed by default
- Solution header with distinctive styling
- Code walkthrough after code blocks

**Progress Tracking:**
- localStorage-based checkboxes
- Visual progress bar
- Percentage display
- Persists across page reloads

### Responsive Behavior

```
Desktop (1200px+): Full sidebar visible, wide content area
Tablet (768px-1199px): Collapsible sidebar, adjusted margins
Mobile (<768px): Hamburger menu, stacked layout, touch-friendly buttons
```

---

## 4. MODULE ADDITIONS/MODIFICATIONS

### Added Modules:

1. **Module 0.4: Settings.py Masterclass** (NEW)
   - Rationale: Settings is the most confusing part for beginners. A dedicated module covering every setting, security configurations, and how to split dev/prod settings prevents countless headaches later.

2. **Module 4.2: Production Security Checklist** (NEW)
   - Rationale: Security deserves more than one module. This covers the deploy checklist, security middleware in detail, and production hardening.

3. **Module 4.3: Multi-Tenant Security Patterns** (NEW)
   - Rationale: Given your interest in multi-tenant POS systems, this deserves explicit coverage rather than being buried in authorization.

4. **Module 5.3: Async Django and Channels** (EXPANDED from brief mention)
   - Rationale: You specifically requested async/Channels coverage. This now gets a full module covering async views, async ORM, and WebSocket implementation.

5. **Module 5.7: Service Layer Architecture** (NEW)
   - Rationale: For production-grade apps, knowing when to move beyond "fat models" is crucial. Covers service layers, selectors, and organizing complex business logic.

### Removed/Consolidated:

1. **Removed NGINX coverage** (as requested)
   - Replaced with focus on platform-specific deployment (Railway/Render handle reverse proxy)

2. **Removed local Redis** (as requested)
   - All Redis examples use Upstash (serverless Redis) for consistency with deployment

3. **Consolidated some testing modules**
   - Django testing and DRF testing remain separate but streamlined

### Settings.py Cheatsheet Integration:
- Will be included as Module 0.4 AND as an appendix reference in every module that introduces new settings
- Comprehensive table format with: Setting name, Default value, Purpose, When to change it, Security implications

---

## 5. CONFIRMATION QUESTION

Banana man, here's what I've prepared:

✅ **Versions:** Django 5.0.x (teaching), 4.2.x (LTS noted), DRF 3.14.x, SimpleJWT 5.3.x, Python 3.11+

✅ **Curriculum:** 47 modules across 7 phases, ~139 total study hours, all your requested topics plus additions

✅ **Design:** Dark brown theme (#1a1210 background, #f5e6d3 text, golden accents), Playfair Display + Inter + JetBrains Mono typography, styled callouts, collapsible solutions, progress tracking

✅ **Additions:** Settings.py masterclass module, expanded security coverage, full async/Channels module, service layer architecture module, Upstash instead of local Redis, no NGINX

✅ **Removals:** Module 6.0 (as you requested), NGINX configuration, local Redis setup

**Before I begin building Module 0.1, confirm:**

1. Are you happy with the ~139 hour curriculum scope, or should we trim/expand any phase?
2. Do you want any changes to the color palette or typography choices?
3. Any specific fintech example you want prioritized (Paystack vs Flutterwave, specific loan types, etc.)?
4. Ready for me to start generating Module 0.1 as a complete HTML file?

Reply with any adjustments, or say "begin" and I'll create Module 0.1 immediately.
