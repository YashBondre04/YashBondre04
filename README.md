# Hi there, I'm Yash Bondre 👋

### 👨‍💻 Full-Stack Developer | AI & Browser Systems Enthusiast | AI & Data Analytics

I specialize in building scalable web applications and advanced browser-native systems. I love combining modern frontend frameworks like React and Next.js with robust backend architectures and powerful AI integrations.

---

### 🙋 About Me

- 🎓 **Education:** Bachelor's degree in Computer Science & Design from New Horizon Institute of Technology and Management.
- 💼 **Experience:** Recently worked as a **Full Stack Developer Intern** at Blood Nexus Studios, building a scalable CMS-driven web application with React.js, Strapi, and PostgreSQL.
- 🔭 **Currently Building:** **SnapFlow**, an advanced Chrome extension that captures live webpages as editable documents with powerful export, annotation, and document workflow features.
- 🌱 **Learning & Exploring:** Browser internals, advanced Chrome extension architecture, AI workflows, and scalable full-stack systems.
- 📫 **How to reach me:** [yashbondre092@gmail.com](mailto:yashbondre092@gmail.com)

---

### 🛠️ Tech Stack & Tools

**Frontend:**
<br/>
<img src="https://img.shields.io/badge/JavaScript-323330?style=for-the-badge&logo=javascript&logoColor=F7DF1E" alt="JavaScript"/>
<img src="https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript"/>
<img src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" alt="React"/>
<img src="https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=next.js&logoColor=white" alt="Next.js"/>
<img src="https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white" alt="Tailwind CSS"/>

**Backend & Databases:**
<br/>
<img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python"/>
<img src="https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white" alt="Flask"/>
<img src="https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white" alt="PostgreSQL"/>
<img src="https://img.shields.io/badge/Supabase-3ECF8E?style=for-the-badge&logo=supabase&logoColor=white" alt="Supabase"/>
<img src="https://img.shields.io/badge/Strapi-2E7EEA?style=for-the-badge&logo=strapi&logoColor=white" alt="Strapi"/>

**DevOps, Tools & AI:**
<br/>
<img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" alt="Docker"/>
<img src="https://img.shields.io/badge/Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white" alt="Vercel"/>
<img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white" alt="Git"/>
<img src="https://img.shields.io/badge/Chrome_Extensions-4285F4?style=for-the-badge&logo=googlechrome&logoColor=white" alt="Chrome Extensions"/>

---

### 🚀 Featured Projects

#### 1. **AI Tech Lead – Agentic AI GitHub App** | [Repo](https://github.com/YashBondre04/Agentic-AI-Tech-Lead)

**What & Why:** An **autonomous pull request review system** that transforms GitHub webhooks into a multi-agent AI workflow. When developers open or update PRs, the system automatically generates structured code reviews and pytest test suites—eliminating manual review bottlenecks while maintaining output safety through validation gates.

**Technical Architecture:**
- **Multi-Agent Orchestration:** Uses **CrewAI** framework to coordinate three specialized agents (Reviewer, Tester, Reporter) that work in parallel on each changed file, then synthesize findings into a unified Markdown report
- **Diff-Scoped Analysis:** Agents focus exclusively on changed files via PR diff API, reducing context noise and LLM costs
- **Structured LLM Output:** **Google Gemini API** generates deterministic test code and reviews; output validated against actual PR filenames to prevent hallucination artifacts
- **Webhook Security:** HMAC signature verification, idempotency guards (dedup by repo + PR + head SHA), and background queue with bounded ThreadPoolExecutor prevents replay and duplicate runs
- **Production-Grade Reliability:** Exponential backoff retry logic, stateless agent memory, health checks, and containerized deployment with Gunicorn

**Tech Stack:**
- **Languages & Frameworks:** Python 3.10+, Flask, CrewAI
- **AI & LLM Integration:** Google Gemini 2.5 Flash, LiteLLM with configurable retry/timeout
- **GitHub Integration:** PyGithub, webhook signature verification (x-hub-signature-256)
- **DevOps & Deployment:** Docker, Gunicorn, environment-based configuration (GitHub PAT or App credentials)

**Key Highlights:**
- ✅ **Production-Ready:** Full deployment guide, Docker Compose with health checks, non-root container runtime
- ✅ **Intelligent Safeguards:** Output validation blocks PR comments if filenames outside diff appear in LLM response
- ✅ **Scalable Design:** Stateless agents + background queue handle concurrent PR events without database dependency
- ✅ **Clean Code Architecture:** Modular agents/tasks/tools separation, comprehensive error handling and logging

---

#### 2. **Revolver Rift Website** | [Live](https://revolverrift.com) | [Repo](https://github.com/YashBondre04/revolverrift_dev)

**What & Why:** A **CMS-driven full-stack gaming brand platform** that showcases game content and brand storytelling through cinematic visuals. Decoupled architecture separates the content layer (Strapi) from the presentation layer (React frontend), enabling rapid content updates without redeployment while maintaining production-grade performance and scalability.

**Technical Architecture:**
- **Decoupled CMS Strategy:** Backend (Strapi v5) serves REST API with structured content collections (pages, media, hero configurations); frontend consumes and renders dynamically, enabling marketers to update site content without code changes
- **High-Fidelity Animations:** **Framer Motion** orchestrates smooth hero animations, section transitions, and micro-interactions; **Swiper** handles cinematic slider galleries with responsive breakpoints
- **Media Optimization:** **Supabase Storage** integration for CDN-accelerated image/video delivery; lazy loading prevents above-the-fold bloat
- **Responsive Architecture:** Mobile-first Tailwind CSS with adaptive layouts across breakpoints; contact form submits to Supabase with fallback to legacy API for reliability
- **Deployment Pipeline:** Separate Railway deployment for Strapi backend (managed Node.js + PostgreSQL), static frontend deployment on edge network

**Tech Stack:**
- **Frontend:** React 18, Vite, React Router, Framer Motion, Swiper, Tailwind CSS, Radix UI, AOS animations
- **Backend & CMS:** Strapi 5.38.0, Node.js, PostgreSQL, Supabase (storage + contact form backend)
- **Styling & Animation:** Tailwind CSS, PostCSS, Autoprefixer, class-variance-authority
- **DevOps & Hosting:** Railway (backend), Vercel/static hosting (frontend), environment variable management

**Key Highlights:**
- ✅ **Content Scalability:** Strapi CMS enables non-technical team to manage pages, media, and structured data post-launch
- ✅ **Performance Optimized:** Code splitting via Vite, lazy image loading, CDN-backed media delivery
- ✅ **Seamless UX:** Advanced animations with Framer Motion create cinematic gaming brand experience
- ✅ **Production Reliability:** Fallback contact form handling, CORS-aware backend configuration, health-monitored deployments

---

#### 3. **Ledgerly SaaS Platform** | [Live](https://ledgerly-chi.vercel.app/) | [Repo](https://github.com/YashBondre04/Ledgerly)

**What & Why:** A **B2B/B2C SaaS marketing website** for a financial software platform. High-fidelity design-to-code translation with fluid animations and responsive layouts demonstrates modern SaaS UI patterns—gradient overlays, glass-morphism effects, 3D WebGL graphics, and smooth motion choreography drive user engagement and conversion.

**Technical Architecture:**
- **Next.js Full-Stack:** Hybrid rendering (static generation for marketing pages, ISR for dynamic content); built-in API routes for backend integration
- **Advanced Visual Effects:** **OGL** (WebGL library) renders 3D graphics for interactive visual sections; **Motion library** creates smooth scroll-triggered animations; Framer Motion handles component-level transitions
- **Email Integration:** **Resend** + **Mailersend** for transactional emails; Nodemailer fallback for SMTP compatibility
- **Responsive Component Library:** Radix UI + shadcn for accessible, unstyled component primitives; Tailwind CSS v4 with PostCSS for utility-first styling at scale
- **Analytics & Monitoring:** Vercel Analytics integration for production performance tracking

**Tech Stack:**
- **Frontend & Framework:** Next.js 16, React 19, TypeScript, Vite
- **Styling & Animation:** Tailwind CSS v4, PostCSS, Motion (Framer Motion alternative), class-variance-authority
- **Advanced Graphics:** OGL (WebGL 3D graphics), Three.js (3D math library), @types/three
- **UI Components:** Radix UI, Base UI, shadcn, Lucide React icons
- **Email & Messaging:** Resend, Mailersend, Nodemailer
- **Analytics & Deployment:** Vercel Analytics, Vercel (platform-native deployment)

**Key Highlights:**
- ✅ **High-Fidelity Design Translation:** Pixel-perfect Figma-to-code implementation with smooth animations
- ✅ **Enterprise-Grade Performance:** Next.js ISR + Vercel Edge Network = fast global delivery
- ✅ **Modern SaaS Aesthetics:** 3D WebGL effects, glass-morphism, gradient overlays, motion choreography
- ✅ **Accessibility First:** Radix UI primitives ensure semantic HTML and keyboard navigation
- ✅ **Conversion Optimized:** Strategic CTAs, email capture, analytics-driven UX iteration

---

#### 4. **Dev Habit Tracker** | [Repo](https://github.com/YashBondre04/DevhabitTracker)

**What & Why:** A **stateless AI-powered developer productivity API** built as a **24-hour take-home assignment**. Demonstrates clean code execution under strict time constraints while prioritizing production-readiness: hybrid rule-based + LLM analysis detects behavioral patterns in developer activity logs (fragmented workflows, burnout cycles, deep focus) and delivers personalized coaching insights without database overhead.

**Technical Architecture:**
- **Hybrid Analysis Pipeline:** 4-step architecture—Data Ingestion → Rule-Based Metrics (pure Python math) → Pattern Classification (5 behavior types with evidence) → LLM Insight Generation (Google Gemini provides coaching)
- **Stateless Design:** No persistent storage; all computation happens in-request via Docker container, enabling zero-setup reviewer execution and simplified deployment
- **Pattern Detection Engine:** Deterministic Python logic calculates: total active time, app distributions, distraction %, context switches, focus session duration; thresholds trigger pattern classification
- **Structured LLM Integration:** **Google Gemini API** generates human-readable coaching tied to detected patterns; response post-processed to ensure actionable insights
- **Docker-First Deployment:** Containerized Flask app with health checks, environment variable injection, non-root runtime

**Tech Stack:**
- **Backend & Framework:** Python 3.11, Flask 3.0.3, Google Generative AI SDK
- **Core Libraries:** python-dotenv (environment config)
- **Deployment & Infrastructure:** Docker, Gunicorn (production server)
- **Quality:** Clean separation of concerns (rule_engine.py, llm_service.py, validators.py)

**Key Highlights:**
- ✅ **Agile Execution:** 24-hour turnaround with zero technical debt; clean layered architecture
- ✅ **Reviewer-Friendly:** Stateless design = no database setup or migrations; Docker Compose `up --build` → ready to test
- ✅ **Hybrid AI Approach:** Combines deterministic rules (low hallucination risk) with LLM insights (human-like coaching)
- ✅ **Production-Grade Reliability:** Health endpoints, structured error handling, detailed API responses
- ✅ **Extensible Foundation:** Ready for future additions (persistence, auth, async processing, React dashboard)

---

#### 5. **Rishab Motor Driving Training School Website** | [Live](https://rishabmotor.vercel.app) | [Repo](https://github.com/YashBondre04/DrivingTrainingSchool)

**What & Why:** A **high-performance local business SPA** built for a driving school client. Demonstrates end-to-end **SEO strategy** (local, on-site, off-site, GEO, AEO) that **directly drove customer acquisition**—schema markup, keyword targeting, and WhatsApp CRM integration converted search traffic into qualified leads while maintaining pixel-perfect responsive design and <2s page load times.

**Technical Architecture:**
- **SEO-Optimized Stack:** React 19 + TypeScript + Vite for fast builds; semantic HTML for crawlability; JSON-LD LocalBusiness schema with service area coverage
- **Local SEO Strategy:**
  - **On-Page:** Target keywords ("driving training Najafgarh", "motor classes Delhi", "RTO assistance") embedded in headings, meta tags, structured content
  - **Schema Markup:** LocalBusiness JSON-LD with exact coordinates, service boundaries (Najafgarh, Dwarka, Vikas Puri), multiple phone numbers
  - **FAQ Section:** Natural language question/answer pairs optimized for "People Also Ask" SERP features
  - **Technical SEO:** Mobile-responsive design, image optimization (WebP format), lazy loading, fast Vite-powered builds
- **Lead Capture & CRM:** WhatsApp Web API integration enables one-click lesson booking with pre-filled messages; seamless handoff to business communication
- **Advanced Visual Effects:** **Framer Motion** animations on hero section and CTAs; **OGL WebGL** for 3D graphical elements; **LightRays** custom component for interactive mouse-following particle effects
- **Performance Optimization:** Vite code splitting, CSS purging, WebP images with lazy loading = consistent <2s page load times

**Tech Stack:**
- **Frontend & Build:** React 19, TypeScript, Vite 8.0.12, React Router
- **Styling & Animation:** Tailwind CSS 3.4.19, Framer Motion 12.40.0, OGL 1.0.11, Lucide React icons
- **SEO & Analytics:** Schema.org JSON-LD, Open Graph meta tags, Google Site Verification
- **CRM Integration:** WhatsApp Web API (contact form integration), Google Maps embedding
- **DevOps & Deployment:** Vercel (serverless deployment with automatic CI/CD), PostCSS + Autoprefixer

**Key Highlights:**
- ✅ **Proven Business Impact:** SEO strategy directly contributed to customer acquisition; WhatsApp CRM drove qualified leads
- ✅ **Local SEO Excellence:** Schema markup, geo-targeted keywords, FAQ optimization = top SERP positions for local searches
- ✅ **Performance-First:** Vite optimized builds, WebP images, lazy loading = sub-2s load times on 4G
- ✅ **Modern UX:** Advanced animations (Framer Motion), 3D WebGL effects, micro-interactions build brand credibility
- ✅ **Freelance Professional Standards:** Full responsibility for design translation, SEO strategy, deployment, and post-launch optimization

---

#### 6. **Data Science & Analytics Projects**

<details>
<summary><strong>📊 E-commerce Machine Learning Data Analysis</strong> | <a href="https://github.com/YashBondre04/Ecommerce-_Machine_Learning_Data_Analysis">Repo</a></summary>

**Project:** Customer behavior analysis to determine mobile app vs. website focus strategy.

**Technical Approach:**
- **EDA & Visualization:** Pandas DataFrames for data loading/cleaning; Matplotlib + Seaborn for distribution analysis and correlation heatmaps
- **Feature Engineering:** Derived metrics from session length, time-on-app, time-on-website, membership duration
- **Linear Regression Modeling:** Scikit-Learn pipeline for model training and coefficient interpretation
- **Business Insight:** Identified platform with higher influence on yearly spending; strategic recommendations for marketing and UX prioritization

**Tech Stack:** Python, Pandas, NumPy, Matplotlib, Seaborn, Scikit-Learn, Jupyter Notebook

**Impact:** Data-driven recommendation reduced marketing spend allocation ambiguity; enabled A/B testing strategy.

</details>

<details>
<summary><strong>💧 Water Usage Prediction Model</strong> | <a href="https://github.com/YashBondre04/Water_Usage_Prediction_Model">Repo</a></summary>

**Project:** Predictive modeling for total water consumption based on demographic & environmental factors.

**Technical Approach:**
- **Data Preprocessing:** Handled missing values, feature scaling, train/test split
- **Feature Engineering:** Population, rainfall, agricultural/industrial/domestic usage as predictors
- **Model Selection:** Tested Linear Regression and Decision Tree; evaluated via RMSE, MAE, R²
- **Results Interpretation:** Identified most important factors for resource planning

**Tech Stack:** Python, Pandas, NumPy, Scikit-Learn, Matplotlib, Seaborn, Jupyter Notebook

**Impact:** Model predictions support government/municipal water resource allocation planning.

</details>

<details>
<summary><strong>🚨 911 Calls Data Capstone Project</strong> | <a href="https://github.com/YashBondre04/911-calls-Data-Capstone-">Repo</a></summary>

**Project:** Emergency call pattern analysis for Montgomery County, PA dataset (Kaggle).

**Technical Approach:**
- **Time-Series Analysis:** Examined call distributions by hour, day-of-week, month; identified peak demand periods
- **Categorical Analysis:** Countplots for call types (Traffic, Fire, EMS); heatmaps for temporal/categorical intersections
- **Geographical Insights:** Zip code + township data enabled regional demand mapping
- **Advanced Visualizations:** Clustermaps, line plots, and multi-variate plots for storytelling

**Tech Stack:** Python, Pandas, NumPy, Matplotlib, Seaborn, Jupyter Notebook

**Impact:** Insights inform emergency response resource allocation; predictive staffing models for municipal planning.

</details>

---

**Key Data Science Highlights (All Projects):**
- ✅ **End-to-End Pipelines:** Data ingestion → cleaning → EDA → modeling → insights
- ✅ **Statistical Rigor:** Proper train/test splits, cross-validation, performance metrics interpretation
- ✅ **Business Translation:** Converted technical findings into actionable recommendations
- ✅ **Visualization Excellence:** Multi-format storytelling (distributions, correlations, time-series, heatmaps)
- ✅ **Jupyter Mastery:** Clean notebook structure, markdown documentation, reproducible analysis

---

### 📄 Resume Preview

[![Yash Bondre Resume](./image.png)](./Yash_Bondre_April_2026.pdf)

> 📥 **[Download PDF Resume](./Yash_Bondre_April_2026.pdf)**

---

### 📊 GitHub Stats

<p align="center">
  <img height="170" src="https://github-readme-stats.vercel.app/api?username=YashBondre04&show_icons=true&theme=github_dark&hide_border=true&rank_icon=github" />
  <img height="170" src="https://github-readme-stats.vercel.app/api/top-langs/?username=YashBondre04&layout=compact&theme=github_dark&hide_border=true" />
</p>

<p align="center">
  <img src="https://streak-stats.demolab.com?user=YashBondre04&theme=github-dark-blue&hide_border=true" />
</p>

---

### 🤝 Let's Connect!

[<img align="left" alt="LinkedIn" width="26px" src="https://cdn.jsdelivr.net/npm/simple-icons@v3/icons/linkedin.svg" />](https://linkedin.com/in/yash-bondre)
[<img align="left" alt="Email" width="26px" src="https://cdn.jsdelivr.net/npm/simple-icons@v3/icons/gmail.svg" />](mailto:yashbondre092@gmail.com)

<br />
