# 🚀 SIH 2026 — Shortlisted Ideas

> A curated collection of shortlisted Smart India Hackathon 2026 problem statements.
> Ranked by SIH feasibility and selection potential.

---

## 📑 Table of Contents

| # | Problem Statement | Theme | Organization | Rank |
|---|---|---|---|---|
| 1 | [26107](#26107) — AI Assistant for Indian Standards (BIS) | 🤖 Smart Automation | Consumer Affairs | 🥇 |
| 2 | [26031](#26031) — AI-Based Onion Quality Grading | 🤖 Smart Automation | Consumer Affairs | 🥈 |
| 3 | [26090](#26090) — AI Market Linkage for Artisans | 🎭 Heritage & Culture | MoSJE | 🥉 |
| 4 | [26032](#26032) — Farmer Procurement Platform | 🤖 Smart Automation | Consumer Affairs | 4th |
| 5 | [26092](#26092) — AI Scheme Matching for Entrepreneurs | 🤖 Smart Automation | MoSJE | 5th |
| 6 | [26132](#26132) — Market Linkages for Farmers | 🌾 Agriculture & FoodTech | Maharashtra | 6th |
| 7 | [26062](#26062) — Polar Expedition Logistics | 🤖 Smart Automation | MoES / NCPOR | 7th |
| 8 | [26135](#26135) — Skilling Outcomes Tracking | 📊 Miscellaneous | Maharashtra | 8th |
| 9 | [26108](#26108) — AI Recommendation Engine for Standards | 🤖 Smart Automation | Consumer Affairs | 9th |
| 10 | [26061](#26061) — Energy Management for Polar Stations | 🌿 Clean & Green Technology | MoES / NCPOR | 10th |
| 11 | [26122](#26122) — Data Capture for Infrastructure Projects | 🤖 Smart Automation | Oil India | 11th |
| 12 | [26163](#26163) — Security Assessment of World Monitor | 🤖 Smart Automation | NTRO | 12th |
| 13 | [26002](#26002) — AI-Based Smart Logistics for NER | 🚚 Transportation & Logistics | MDoNER | 13th |
| 14 | [26197](#26197) — Cultural Heritage Showcase | 🎭 Heritage & Culture | AICTE | 14th |
| 15 | [26204](#26204) — Tourism Industry Solution | ✈️ Travel & Tourism | AICTE | 15th |
| 16 | [26027](#26027) — AI-Powered Block Planning for Railways | 🚚 Transportation & Logistics | Railways | 16th |
| 17 | [26051](#26051) — Area-Specific Shelter Design | 🛡️ Miscellaneous | DRDO | 17th |
| 18 | [26037](#26037) — Autonomous Vehicle Path Planning | 🚗 Smart Vehicles | MathWorks | 18th |

---

### 🏆 Ranking Methodology

Each idea is evaluated on:

| Factor | Weight | What it means |
|---|---|---|
| **SIH Feasibility** | 40% | Can we build a working prototype in 36 hours? Are the tech stacks familiar? |
| **Wow Factor** | 30% | Will the panel be impressed? Is there a clear demo moment? |
| **Real-World Impact** | 20% | Does it solve a genuine, large-scale problem? |
| **Low Dependency Risk** | 10% | Do we need external datasets, APIs, or domain expertise we don't have? |

---

## 🥇 TIER 1 — Best Bets (High Feasibility + High Impact)

---

### <a id="26107"></a>Problem Statement 26107

| **Problem Statement ID** | 26107 |
|---|---|
| **Problem Statement Title** | AI-powered Intelligent Assistant for Indian Standards and BIS Services for Industries and Consumers |
| **Organization** | Ministry of Consumer Affairs, Food & Public Distribution |
| **Department** | Department of Consumer Affairs (DoCA) |
| **Category** | Software |
| **Theme** | Smart Automation |

**Description:**

• **Background** The Bureau of Indian Standards publishes thousands of Indian Standards and provides various services such as product certification, hallmarking, laboratory recognition, Standards Clubs, training, consumer affairs, and conformity assessment.

• At present, users often struggle to identify:
• Applicable Indian Standards for their products,
• Certification requirements,
• Relevant BIS schemes,
• Licensing procedures,
• Testing requirements,
• Related standards, and
• Answers to technical queries.

Searching through multiple documents, portals, and PDFs is time-consuming, particularly for MSMEs, startups, students, and consumers.

• **Description** Develop an Al-powered conversational assistant that enables users to obtain accurate, context-aware, and source-backed information related to Indian Standards and BIS services through natural language interactions.

The assistant should understand user queries in plain language, retrieve relevant information from authorized BIS knowledge sources, and provide responses with references to the documents or clauses which ever are applicable.

• **Expected Solution** The software solution consists of an Intelligent Assistant or Agent which can
• Answer questions related to Indian Standards.
• Recommend applicable standards based on product descriptions.
• Provide guidance on BIS certification schemes.
• Explain certification processes.
• Answer consumer-related queries.
• Guide users regarding hallmarking.
• Suggest relevant testing laboratories.
• Support multilingual interaction.

> **💡 Detailed Solution Approach:**
>
> **Core Architecture:** Build a **RAG (Retrieval-Augmented Generation)** system. Scrape/index all BIS standards PDFs and documentation into a vector database (Pinecone/ChromaDB/Weaviate). Use an LLM (OpenAI GPT-4 or open-source Llama 3) as the generation backbone.
>
> **How it works:**
> 1. **Data Ingestion:** Scrape bis.gov.in for standards catalogs, certification procedures, hallmarking guidelines, and lab listings. Parse PDFs using libraries like `PyMuPDF` or `pdfplumber`. Chunk documents intelligently (by section/clause, not fixed size).
> 2. **Vector Store:** Embed chunks using `sentence-transformers` (all-MiniLM-L6-v2) and store in ChromaDB or Pinecone.
> 3. **Conversational Interface:** Build a clean chat UI (Next.js + Tailwind or Streamlit for speed). User asks a question in natural language → embed the query → retrieve top-K relevant chunks → pass to LLM with context → generate answer with citations (clause numbers, document references).
> 4. **Multilingual:** Use Google Translate API or `deep-translator` for Hindi/regional language input → translate to English → process → translate response back.
> 5. **Features to showcase:**
>    - "What standard applies to electric fans?" → retrieves IS 302, highlights relevant clauses
>    - "How do I get BIS certification for steel?" → step-by-step guide with document links
>    - "Where is the nearest testing lab in Mumbai?" → geolocation-based lab listing
>
> **Tech Stack:** Python (FastAPI backend), ChromaDB/Pinecone, OpenAI API or Llama 3, Next.js/Streamlit frontend, sentence-transformers for embeddings.
>
> **Why this ranks #1:**
> - ✅ RAG is a proven, well-understood architecture — we can build a solid demo in 36 hours
> - ✅ BIS has publicly available data — no dependency on external APIs or datasets
> - ✅ Clear "wow moment" — ask any question, get a sourced answer with document references
> - ✅ Addresses a real pain point for MSMEs and startups (huge audience)
> - ✅ Multilingual support adds impressiveness without much complexity
> - ✅ Panel will love the practical utility — it solves a government problem directly

---

### <a id="26031"></a>Problem Statement 26031

| **Problem Statement ID** | 26031 |
|---|---|
| **Problem Statement Title** | Quality assessment and grading of onions are often subjective and vary across procurement centers, resulting in disputes and inconsistencies. |
| **Organization** | Ministry of Consumer Affairs, Food & Public Distribution |
| **Department** | Department of Consumer Affairs (DoCA) |
| **Category** | Software |
| **Theme** | Smart Automation |

**Description:**

**Expected Solution:**

Develop an AI-based mobile application that:

• Uses image processing to assess onion quality.
• Identifies damaged, rotten, sprouted, or undersized onions.
• Estimates Grade A and URS percentages.
• Generates a digital quality report instantly.
• Reduces human bias and improves transparency.

> **💡 Detailed Solution Approach:**
>
> **Core Architecture:** Build a **mobile image classification app** using a fine-tuned CNN model (transfer learning on MobileNetV2 or EfficientNet-Lite for on-device inference).
>
> **How it works:**
> 1. **Data Collection:** Gather onion images from Google Images, Kaggle datasets, or scrape from agricultural sites. Label them into categories: Grade A (healthy, full-size), damaged, rotten, sprouted, undersized. Aim for ~2000-5000 images. Use data augmentation (rotation, brightness, flip) to expand dataset.
> 2. **Model Training:** Fine-tune MobileNetV2 using TensorFlow Lite or PyTorch Mobile. Train for multi-class classification (healthy/damaged/rotten/sprouted/undersized). Achieve ~85-90% accuracy.
> 3. **Grading Logic:** For a batch of onion images, classify each onion → calculate percentage of Grade A vs. URS (undersized/rotten/sprouted) → generate a pie chart breakdown.
> 4. **Mobile App:** Build with Flutter or React Native. Camera captures → model runs on-device (TFLite) → instant results → generates a shareable PDF report with quality breakdown, timestamp, and grading certificate.
> 5. **Demo Flow:** Point camera at a box of onions → app classifies each visible onion → shows real-time quality breakdown → generates digital report.
>
> **Tech Stack:** Python (training), TensorFlow Lite/ONNX Runtime (inference), Flutter/React Native (mobile), Chart.js or native charts for visualization, PDF generation library.
>
> **Why this ranks #2:**
> - ✅ Image classification is our bread and butter — well-understood, proven approach
> - ✅ Mobile demo is extremely visual and impressive for the panel
> - ✅ Can build a working prototype with a small, curated dataset
> - ✅ On-device inference (TFLite) means no cloud dependency — works offline
> - ✅ Directly solves a real problem (onion procurement disputes affect millions of farmers)
> - ⚠️ Need to collect/curate training data, but synthetic augmentation helps

---

### <a id="26090"></a>Problem Statement 26090

| **Problem Statement ID** | 26090 |
|---|---|
| **Problem Statement Title** | AI-Driven Market Linkage and Smart Cataloging Mobile Application for Marginalized Artisans |
| **Organization** | Ministry of Social Justice and Empowerment (MoSJE) |
| **Department** | Department of Social Justice and Empowerment |
| **Category** | Software |
| **Theme** | Heritage & Culture |

**Description:**

• **Background** The government actively supports the socio-economic upliftment of marginalized communities, particularly micro-entrepreneurs, artisans, and weavers. Financial assistance is provided to establish small-scale manufacturing and handicraft units. To help these beneficiaries sell their goods, market exposure is facilitated through periodic physical exhibitions, cluster development programs, and trade fairs (such as Shilp Samagam, Surajkund Mela, and Dilli Haat). While physical exhibitions provide a temporary boost in sales, these micro-entrepreneurs lack continuous, year-round access to broader digital markets. Transitioning to the digital economy is hindered by low digital literacy, language barriers, and a lack of technical skills required to professionally photograph, price, and catalog products for modern e-commerce.

• **Challenge** There is a critical need to bridge the gap between traditional craftsmanship and modern digital commerce. Beneficiaries struggle to present their products competitively online. They often fail to capture high-quality images, write compelling product descriptions, or understand dynamic market pricing. The challenge is to build an intuitive, AI-driven mobile application that acts as a 'virtual business manager' for these artisans. The app must empower them to seamlessly digitize their inventory, optimize their listings using AI, and connect directly with larger B2B buyers or government e-marketplaces without requiring advanced technical knowledge.

• **Expected Solution** Participants are expected to develop an AI-powered, cross-platform mobile application supported by a robust, scalable backend architecture. To ensure high adoption among low-literacy users, the application must feature a highly responsive, minimalist UI/UX design (incorporating modern, clean visual hierarchies and accessible layouts).

**Key features should include:**

1. **AI Image Enhancer & Studio:** A built-in camera module that utilizes AI to automatically remove cluttered backgrounds, correct lighting, and format product photos (e.g., textiles, handicrafts) to professional e-commerce standards.

2. **Multilingual Auto-Cataloger:** An NLP-based engine that allows artisans to describe their product via voice notes in regional languages. The AI should translate and generate SEO-friendly, professional product descriptions in English and Hindi.

3. **Dynamic Pricing Assistant:** A machine learning algorithm that analyzes the uploaded product image and description to suggest an optimal, competitive selling price based on current market trends and raw material costs.

• **Impact Goals**
• Provide marginalized micro-entrepreneurs with a continuous, year-round digital sales channel, reducing their dependency on periodic physical fairs.
• Drastically lower the barrier to entry for digital commerce through intuitive AI automation.
• Improve digital literacy and financial independence, ultimately increasing the average annual income of the target demographic.

> **💡 Detailed Solution Approach:**
>
> **Core Architecture:** A **Flutter/React Native mobile app** with 3 AI-powered modules backed by a Python FastAPI backend.
>
> **Module 1 — AI Image Enhancer:**
> - Use `rembg` (background removal, uses U2-Net model) for instant background removal
> - Apply OpenCV for auto-brightness/contrast correction
> - Optional: Use `clipdrop` API or `remove.bg` API for production-quality results
> - Format output to standard e-commerce dimensions (1000x1000px, white background)
>
> **Module 2 — Multilingual Auto-Cataloger:**
> - Voice input → Google Speech-to-Text API (supports Hindi, Bengali, Tamil, etc.)
> - Transcribed text → Pass to GPT-4/Llama 3 prompt: "Generate an SEO-friendly product description for an e-commerce listing based on this artisan description: [text]. Output title, description, tags."
> - Translate to English/Hindi using Google Translate API
>
> **Module 3 — Dynamic Pricing Assistant:**
> - Scrape prices from Flipkart, Amazon, IndiaMART for similar handicraft categories
> - Build a simple regression model (or use LLM reasoning) to suggest price based on: product category, material, size, market average, competitor pricing
> - Show the artisan: "Similar products sell for ₹500-800. Suggested price: ₹650"
>
> **Demo Flow:** Artisan opens app → takes photo of handicraft → AI removes background → speaks product description in Hindi → AI generates English catalog listing → gets price suggestion → one-click publish to marketplace.
>
> **Tech Stack:** Flutter (mobile), Python FastAPI (backend), rembg + OpenCV (image), Google Speech-to-Text + GPT-4 (NLP), BeautifulSoup (price scraping), PostgreSQL (database).
>
> **Why this ranks #3:**
> - ✅ 3 distinct AI features = impressive multi-module demo
> - ✅ Strong social impact narrative — judges love "empowerment" stories
> - ✅ Each module is independently buildable — can prioritize if time runs short
> - ⚠️ Image enhancement and voice recognition add complexity, but APIs handle the heavy lifting
> - ⚠️ Need to ensure the demo showcases a real artisan workflow

---

## 🥈 TIER 2 — Strong Contenders (Good Feasibility + Good Impact)

---

### <a id="26032"></a>Problem Statement 26032

| **Problem Statement ID** | 26032 |
|---|---|
| **Problem Statement Title** | Farmers often face long waiting times, lack of information regarding procurement schedules, and uncertainty about procurement status. |
| **Organization** | Ministry of Consumer Affairs, Food & Public Distribution |
| **Department** | Department of Consumer Affairs (DoCA) |
| **Category** | Software |
| **Theme** | Smart Automation |

**Description:**

**Expected Solution:**

Develop a platform that:

• Enables farmer registration and slot booking.
• Provides real-time queue management.
• Sends SMS/app notifications.
• Tracks procurement and payment status.
• Reduces congestion and waiting time at procurement centres.

> **💡 Detailed Solution Approach:**
>
> **Core Architecture:** A **full-stack web + mobile platform** — essentially a smart booking and queue management system for procurement centres.
>
> **How it works:**
> 1. **Farmer Registration:** Aadhaar-linked or phone-number-based signup. Profile includes farm size, crop type, expected quantity.
> 2. **Slot Booking:** Farmers select a procurement centre, choose a date/time slot. System shows available slots (capacity-based). Confirmation via SMS (using Twilio or MSG91).
> 3. **Real-Time Queue:** Live queue dashboard showing current position, estimated wait time, and number of farmers ahead. Push notifications when slot is 30 min away.
> 4. **Procurement Tracking:** After delivery — status updates: "Received → Weighing → Quality Check → Approved → Payment Initiated → Payment Complete."
> 5. **Payment Integration:** UPI/payment tracking with transaction IDs. Farmer gets SMS confirmation on payment.
> 6. **Admin Dashboard:** For procurement centre officials — view today's slots, manage queue, mark completion, generate daily reports.
>
> **Tech Stack:** React.js (web), Flutter (mobile), Node.js/Express or Django (backend), PostgreSQL (database), Twilio/MSG91 (SMS), Redis (real-time queue), WebSocket (live updates).
>
> **Why this ranks #4:**
> - ✅ Well-defined problem with clear features — no ambiguity
> - ✅ Standard booking/queue system — familiar architecture
> - ✅ SMS notifications add a nice real-world touch
> - ⚠️ Less "AI" focused — more of a clean full-stack product
> - ⚠️ Panel might want to see more intelligence/automation
> - ✅ But: very practical, very demoable, solves a real farmer pain point

---

### <a id="26092"></a>Problem Statement 26092

| **Problem Statement ID** | 26092 |
|---|---|
| **Problem Statement Title** | AI-Driven Scheme Matching for Marginalized Entrepreneurs |
| **Organization** | Ministry of Social Justice and Empowerment (MoSJE) |
| **Department** | Department of Social Justice and Empowerment |
| **Category** | Software |
| **Theme** | Smart Automation |

**Description:**

• **Background** To promote the socio-economic empowerment of the Scheduled Caste (SC) population, the government provides concessional financial assistance and educational loans. Beneficiaries with an annual family income of up to ₹5.00 Lakhs are eligible for various tailored financial products covering up to 90% of their project or education costs at highly concessional interest rates (typically 6.5% to 8% per annum).

However, direct loan applications are not entertained. Instead, funds are routed through a 'Channel Finance System' comprising over 100 Channel Partners, including State Channelizing Agencies (SCAs), Public Sector Banks (PSBs), Regional Rural Banks (RRBs), and NBFC-MFIs.

• **Challenge** Citizens often lack awareness regarding which specific credit scheme fits their needs—such as distinguishing between a Micro Finance Scheme for small projects (up to ₹1.40 lakh), a Term Loan for larger projects (up to ₹50.00 lakh), or an Educational Loan Scheme. Furthermore, applicants face difficulties identifying and locating the nearest authorized Channel Partner equipped to process their specific loan category. This fragmentation leads to offline confusion, misrouted applications, and delays in disbursement.The challenge is to develop an intelligent, multi-lingual digital platform or mobile application that bridges the gap between the beneficiaries and the channelizing agencies.

• **Expected Solution** Participants are expected to develop a comprehensive platform that includes:

1. **Smart Scheme Recommender:** An AI/rule-based engine that takes basic user inputs (project type, estimated cost, income level, education status) and automatically recommends the most suitable credit or educational loan scheme.

2. **Financial Calculator:** A dynamic tool to calculate projected EMIs, accounting for specific scheme guidelines like maximum loan limits, interest rates (e.g., 6.5% to 15% depending on the scheme), and moratorium periods (3 to 12 months).

3. **Geo-Spatial Partner Locator & Router:** Integration of a mapping service to identify the nearest eligible Channel Partner (SCA/Bank/NBFC-MFI) based on the user's location and the partner's current fund utilization eligibility (ensuring applications aren't sent to partners with high NPAs or overdues).

• **Impact Goals**
• Enhance financial literacy among the target demographic regarding concessional lending.
• Improve transparency and efficiency in the channel finance ecosystem, ensuring faster disbursements and better fund utilization.

> **💡 Detailed Solution Approach:**
>
> **Core Architecture:** A **mobile app with a recommendation engine + map integration** — guide SC beneficiaries to the right scheme and nearest Channel Partner.
>
> **How it works:**
> 1. **Smart Scheme Recommender:** Build a decision tree / rule-based engine. User inputs: project type (micro/term/education), estimated cost, annual income, education level. Engine matches against a structured database of schemes (we can manually compile ~20-30 schemes with eligibility criteria). Output: top 3 matching schemes with details.
>    - *AI upgrade:* Use GPT-4 to do fuzzy matching on free-text project descriptions → map to scheme categories.
> 2. **Financial Calculator:** Standard EMI calculator with scheme-specific parameters. Input: loan amount, scheme → Output: EMI, total interest, moratorium period, repayment schedule.
> 3. **Geo-Spatial Partner Locator:** Use Google Maps API or Mapbox. Input: user location + scheme type → Query database of Channel Partners (SCA/Bank/NBFC-MFI) → Show nearest eligible partners on map with distance, contact info, and availability status.
> 4. **Multilingual:** Use Google Translate or a lightweight translation library for Hindi/regional language UI.
>
> **Tech Stack:** Flutter (mobile), Python FastAPI (backend), PostgreSQL (scheme + partner database), Google Maps API (location), GPT-4 API (fuzzy matching), Google Translate (multilingual).
>
> **Why this ranks #5:**
> - ✅ Clear 3-feature structure — easy to plan and demo
> - ✅ Rule-based recommendation is fast to build and reliable
> - ✅ Map integration adds visual appeal to the demo
> - ✅ Strong social impact narrative (SC empowerment)
> - ⚠️ Need to compile scheme database manually (research task)
> - ⚠️ Channel Partner data might need to be synthetic for demo

---

### <a id="26132"></a>Problem Statement 26132

| **Problem Statement ID** | 26132 |
|---|---|
| **Problem Statement Title** | Strengthening market linkages and price discovery for farmers |
| **Organization** | Government Of Maharashtra |
| **Department** | Maharashtra State Innovation Society, Department of Skills, Employment, Entrepreneurship and Innovation |
| **Category** | Software |
| **Theme** | Agriculture, FoodTech & Rural Development |

**Description:**

• **Problem Description** Many farmers, especially smallholders and producer groups, have limited visibility of current and expected prices across nearby markets, processors, institutional buyers and digital trading channels. Information on quality specifications, demand, logistics, storage, payment reliability and buyer credentials may be fragmented. Farmers may sell immediately after harvest because of liquidity or storage constraints and may have weak bargaining power. Buyers, meanwhile, may struggle to aggregate consistent volumes and verify quality. The challenge is to improve transparent price discovery and create reliable, efficient linkages from farm gate to suitable buyers.

• **Expected Solution / Outcome** A market-intelligence and transaction enablement solution that aggregates mandi prices, buyer demand, quality requirements, arrival volumes, transport and storage options; provides localised price trends and sale-window recommendations; matches farmers/FPOs with verified buyers; enables lot creation, quality grading, digital offers, logistics coordination and payment tracking; and supports dispute or grievance processes. Expected outcomes include improved farmer price realisation, reduced information asymmetry, lower transaction cost, stronger FPO aggregation, reduced post harvest loss, more reliable buyer sourcing and transparent transaction records.

> **💡 Detailed Solution Approach:**
>
> **Core Architecture:** A **marketplace + analytics platform** — aggregate mandi prices, match farmers with buyers, enable transactions.
>
> **How it works:**
> 1. **Price Aggregation:** Scrape mandi prices from government portals (agmarknet.gov.in has public APIs/data). Build a real-time price dashboard by crop, district, and mandi.
> 2. **Price Trends & Recommendations:** Analyze historical prices (30/60/90 day trends). Use simple time-series forecasting (Prophet or moving averages) to suggest: "Wheat prices in Pune mandi are expected to rise 5% in the next 2 weeks — hold if possible."
> 3. **Buyer-Seller Matching:** FPO registers with crop type, quantity, location → System matches with verified buyers (processors, institutional buyers, export companies) based on crop, volume, and location.
> 4. **Lot Creation & Quality Grading:** Farmer creates a lot → uploads photos → AI suggests grade (reuse onion grading model concept) → lot listed on marketplace.
> 5. **Logistics & Payment:** Coordinate transport (integrate with existing logistics APIs or manual matching). Track payment status.
>
> **Tech Stack:** React.js (web), Flutter (mobile), Python/Django (backend), PostgreSQL (database), agmarknet data (price scraping), Prophet/ARIMA (forecasting), Google Maps (logistics).
>
> **Why this ranks #6:**
> - ✅ Well-scoped with clear deliverables
> - ✅ Real data available from agmarknet — no synthetic data problem
> - ✅ Price forecasting adds an AI/ML element
> - ⚠️ Marketplace features (buyer matching, logistics) are complex to fully implement in 36 hours
> - ⚠️ Need to prioritize — focus on price dashboard + matching, defer logistics

---

### <a id="26062"></a>Problem Statement 26062

| **Problem Statement ID** | 26062 |
|---|---|
| **Problem Statement Title** | Integrated Polar Expedition Logistics and Asset Management System |
| **Organization** | Ministry of Earth Sciences (MoES) |
| **Department** | National Centre for Polar and Ocean Research (NCPOR) |
| **Category** | Software |
| **Theme** | Smart Automation |

**Description:**

Develop a centralized digital platform for expedition planning, cargo tracking, inventory management, personnel movement and emergency response.

> **💡 Detailed Solution Approach:**
>
> **Core Architecture:** A **dashboard-centric logistics management system** — think "project management for polar expeditions."
>
> **How it works:**
> 1. **Expedition Planning:** Timeline/Gantt chart view of expedition phases. Assign tasks, resources, and personnel to each phase.
> 2. **Cargo Tracking:** Barcode/QR-based cargo tracking. Each item has: name, weight, destination camp, status (in-transit/delivered/stored). Live tracking view on a map.
> 3. **Inventory Management:** Real-time stock levels at each camp/station. Low-stock alerts. consumption forecasting.
> 4. **Personnel Movement:** Check-in/check-out system at each station. Current location of all team members. Movement history.
> 5. **Emergency Response:** SOS button with GPS location. Emergency protocol checklist. Communication log.
>
> **Tech Stack:** React.js (web dashboard), Node.js/Express (backend), PostgreSQL + PostGIS (geospatial data), Leaflet/Mapbox (maps), Socket.io (real-time updates), QR/barcode generation libraries.
>
> **Why this ranks #7:**
> - ✅ Standard CRUD + dashboard — straightforward to build
> - ✅ Map visualization makes the demo visually impressive
> - ⚠️ Niche domain — judges might not connect with "polar expedition" as much
> - ⚠️ Less AI/ML — more of a well-built management tool
> - ✅ But: clean execution of a focused product can still impress

---

### <a id="26135"></a>Problem Statement 26135

| **Problem Statement ID** | 26135 |
|---|---|
| **Problem Statement Title** | Difficulties in tracking employment outcomes, skill gaps, and the impact of skilling initiatives |
| **Organization** | Government Of Maharashtra |
| **Department** | Maharashtra State Innovation Society, Department of Skills, Employment, Entrepreneurship and Innovation |
| **Category** | Software |
| **Theme** | Miscellaneous |

**Description:**

• **Problem Description** Training systems frequently capture enrolment, attendance, assessment and certification, but reliable information on employment, self-employment, job retention, wage progression, relevance of training and longer-term livelihood outcomes may remain incomplete. Trainees may change phone numbers or locations, employers may not report consistently, and multiple programmes may use different identifiers and definitions. Without longitudinal outcomes, it is difficult to compare providers, improve courses, target future investments or demonstrate public value. The challenge is to establish credible, low-burden and privacy conscious outcome tracking.

• **Expected Solution / Outcome** A longitudinal skilling-outcomes and impact-measurement system that creates consent-based trainee records, links training with placement and employment signals, conducts automated and assisted follow-ups, captures self-employment and apprenticeship outcomes, validates employer information, measures wage and retention progression, and provides cohort, course, provider, district and demographic analytics. It should identify skill gaps and reasons for non-placement or attrition. Expected outcomes include higher-quality outcome data, better programme and provider accountability, targeted remedial actions, improved resource allocation and evidence-based policy design.

> **💡 Detailed Solution Approach:**
>
> **Core Architecture:** A **data analytics + CRM platform** — track trainees longitudinally from enrollment through employment.
>
> **How it works:**
> 1. **Trainee Profiles:** Consent-based records with: demographics, course enrolled, completion status, certification.
> 2. **Placement Linking:** Post-training survey → employment status, employer name, job role, salary. Automated follow-up emails/SMS at 3, 6, 12 months.
> 3. **Employer Validation:** Cross-reference employer details. Flag inconsistencies.
> 4. **Analytics Dashboard:** Cohort-level metrics — placement rate, average salary, retention at 6/12 months, skill gaps (which courses have lowest placement). District-wise and provider-wise comparison.
> 5. **Skill Gap Identification:** Analyze which courses have high enrollment but low placement → suggest curriculum improvements.
>
> **Tech Stack:** React.js (dashboards), Python/Django (backend), PostgreSQL (database), Chart.js/D3.js (visualizations), Celery + Redis (automated follow-ups), SMTP/Twilio (notifications).
>
> **Why this ranks #8:**
> - ✅ Analytics dashboards are visually impressive
> - ✅ Clear data model and features
> - ⚠️ Longitudinal tracking is hard to demo without real historical data
> - ⚠️ More of an analytics/CRM tool — less "AI" flash
> - ✅ But: strong government relevance and policy impact angle

---

## 🥉 TIER 3 — Feasible but Challenging

---

### <a id="26108"></a>Problem Statement 26108

| **Problem Statement ID** | 26108 |
|---|---|
| **Problem Statement Title** | AI-Powered Recommendation Engine for Identifying Applicable Indian Standards for Procurement Specifications |
| **Organization** | Ministry of Consumer Affairs, Food & Public Distribution |
| **Department** | Department of Consumer Affairs (DoCA) |
| **Category** | Software |
| **Theme** | Smart Automation |

**Description:**

• **Background** Government departments, Public Sector Enterprises (PSEs), procurement agencies, and private organizations procure a wide range of products and services through e-procurement portals. Procurement officials are often required to prepare technical specifications that reference the appropriate Indian Standards (IS). However, identifying the correct standard(s) is challenging due to the large number of published standards, overlapping scopes, frequent revisions, and the need to consider associated or normative reference standards. Consequently, tender specifications may omit relevant standards, reference outdated versions, or include incomplete technical requirements, leading to ambiguity, reduced product quality, and procurement disputes.

An intelligent system is required that can automatically analyze a product description or technical specification and recommend the most relevant Indian Standard(s), along with allied, cross-referenced, or normative standards that should also be considered.

• **Description** Develop an Al-powered recommendation engine that integrates with procurement portals and assists procurement officials in identifying the most relevant Indian Standards and related standards while preparing tender specifications.

• **Expected Features**
• Accept product descriptions, technical specifications, or tender documents as input.
• Recommend the most relevant Indian Standard(s) based on semantic understanding rather than keyword matching.
• Identify allied standards, including normative references, test methods, terminology standards, safety standards, installation standards, and related product standards.
• Highlight the latest published version and amendments of the recommended standards.
• Suggest mandatory certification requirements, where applicable (e.g., BIS Product Certification, CRS, Hallmarking).
• Support multilingual input and natural language queries.

> **💡 Detailed Solution Approach:**
>
> **Core Architecture:** Very similar to 26107 (BIS Assistant) but focused on **procurement document analysis** rather than conversational Q&A. Could potentially be combined or built as a companion module.
>
> **How it works:**
> 1. Upload a tender document or paste a product specification
> 2. Use NLP/LLM to extract key product categories, technical requirements, and material types
> 3. Query the Indian Standards database (same vector store as 26107) to find matching standards
> 4. For each matched standard, also find normative references, test methods, and allied standards
> 5. Output a structured report: recommended standards, versions, certification requirements
>
> **Tech Stack:** Same as 26107 — Python, FastAPI, ChromaDB, GPT-4/Llama 3, PDF parsing.
>
> **Why this ranks #9:**
> - ✅ Similar tech to 26107 — could be a dual submission or combined project
> - ⚠️ More niche audience (procurement officials vs. general consumers)
> - ⚠️ Document parsing adds complexity
> - 💡 **Best strategy:** Build 26107 first, then adapt the same core engine for 26108 if time permits

---

### <a id="26061"></a>Problem Statement 26061

| **Problem Statement ID** | 26061 |
|---|---|
| **Problem Statement Title** | AI-Driven Smart Energy Management System for Polar Research Stations |
| **Organization** | Ministry of Earth Sciences (MoES) |
| **Department** | National Centre for Polar and Ocean Research (NCPOR) |
| **Category** | Software |
| **Theme** | Clean & Green Technology |

**Description:**

Develop an intelligent energy-management system using AI for load forecasting, renewable energy integration and fuel optimization under extreme polar conditions.

> **💡 Detailed Solution Approach:**
>
> **Core Architecture:** An **AI energy dashboard** with forecasting and optimization modules.
>
> **How it works:**
> 1. **Load Forecasting:** Time-series model (Prophet/LSTM) trained on historical energy consumption data. Predicts hourly/daily load based on: temperature, sunlight hours, occupancy, equipment usage patterns.
> 2. **Renewable Integration:** Model solar panel output based on polar sunlight data. Optimize battery charge/discharge cycles. Show energy mix: solar vs. diesel vs. battery.
> 3. **Fuel Optimization:** Linear programming model to minimize diesel consumption while meeting energy demands. Factor in: fuel delivery schedules, storage capacity, weather forecasts.
> 4. **Dashboard:** Real-time energy monitoring, consumption trends, forecasting charts, optimization recommendations.
>
> **Tech Stack:** Python (Flask/FastAPI), Prophet/LSTM (forecasting), PuLP/SciPy (optimization), React.js (dashboard), PostgreSQL (data storage).
>
> **Why this ranks #10:**
> - ✅ AI forecasting is impressive and well-scoped
> - ⚠️ Domain-specific — need polar energy data (might need synthetic data)
> - ⚠️ "Energy optimization" requires some operations research knowledge
> - ⚠️ Panel may not connect deeply with polar research context

---

### <a id="26122"></a>Problem Statement 26122

| **Problem Statement ID** | 26122 |
|---|---|
| **Problem Statement Title** | Intelligent Data Capture & Schedule-Linking Layer for Infrastructure Project Management: Real-Time Actual Progress Tracking (Planning-to-Execution Bridge) |
| **Organization** | Oil India Limited |
| **Department** | Oil India Limited |
| **Category** | Software |
| **Theme** | Smart Automation |

**Description:**

• **Background** Infrastructure project schedules cascade from macro milestones (L1) down to micro, executable activities (L5/L6), spanning multiple engineering disciplines - civil, piping, static/rotating equipment, electrical, instrumentation, HSE- each executing and reporting in parallel. While the baseline plan is well-structured (Primavera/MS Project), actual execution data flows back through daily progress reports, site diaries, discipline-wise spreadsheets, and verbal supervisor updates, each in its own format and cadence, largely disconnected from the L5/L6 activity IDs in the plan.

• **Problem Description** There is no reliable, low-friction mechanism to capture actual start/end times of L5/L6 activities across disciplines and auto-link them back to the plan. Input quality varies with manpower skill, reporting discipline, and format. Field execution is often more granular than the planned WBS, and different disciplines describe the same physical progress differently (e.g., 'spool erected' vs. the plan's 'Erect Line 24?-XX'). Consequently:

- Actual progress data is fragmented, delayed, and inconsistently structured across disciplines and contractors.
- Manual reconciliation with the baseline schedule is slow, error-prone, and often lags the schedule update cycle by days or weeks.
- Downstream performance analytics, delay/risk analysis, and forecasting inherit this poor-quality, late data- undermining the AI performance-monitoring stack that depends on it.
- Once a project closes, the hard-won knowledge of what actually happened - real durations, real bottlenecks, real deviations from plan - is rarely captured in a structured, queryable form, so it is lost rather than feeding future project planning.

• **Expected Outcome/Solution**
- Ingest heterogeneous discipline-wise inputs - free-text daily reports, spreadsheets, scanned diaries, Primavera/MS Project exports - and extract activity-level actual start/end events.
- Offer an LLM-based conversational or voice interface ('time agent') for site supervisors across disciplines to log activity start/end with minimal friction, replacing rigid manual forms while still producing structured output.
- Fuzzy-match and link extracted discipline-specific activity descriptions to the correct L5/L6 plan node, handling terminology differences and granularity mismatches, and flag unmatched/new activities for planner review rather than silently dropping them.
- Auto-update actual start/end dates in the schedule/PMIS in near real time, with a confidence score and audit trail per entry.
- Produce a clean, structured, discipline-tagged actual-progress dataset that serves two purposes: (a) live input for performance analytics, delay/risk pattern discovery, and forecasting, and (b) a foundation for institutional memory building - a growing, queryable repository of real project execution patterns (actual durations, recurring delay causes, discipline-wise productivity) that future projects can learn from, instead of that knowledge staying locked in individual supervisors' experience or scattered paper records.

A working prototype demonstrating ingestion of 2–3 varied input formats (e.g., a free-text daily report and a discipline spreadsheet), extraction, and schedule-linking logic would be ideal; full production-grade OCR/ASR is not required.

• **Relevant Data Availability** Anonymized/ sample daily progress report formats, sample L5/L6 schedule extracts, and illustrative discipline-wise (civil/ piping/ electrical) site-diary or spreadsheet templates can be shared under NDA with Institute/ Authorised person. Live project data will not be shared; teams should work with synthetic/sample data of similar structure.

> **💡 Detailed Solution Approach:**
>
> **Core Architecture:** An **LLM-powered data extraction + schedule linking system** — parse free-text reports, extract structured activity data, and fuzzy-match to schedule nodes.
>
> **How it works:**
> 1. **Input Ingestion:** Accept daily reports (free-text), spreadsheets (CSV/Excel), and Primavera XML exports. Parse them into a common format.
> 2. **LLM Extraction:** Use GPT-4 with structured output (JSON mode) to extract: activity name, discipline, start date, end date, status from free-text reports. Example prompt: "Extract activity start/end events from this daily report: [text]. Output as JSON array."
> 3. **Fuzzy Matching:** Use sentence embeddings + cosine similarity to match extracted activity descriptions to L5/L6 schedule nodes. Handle synonyms and granularity mismatches (e.g., "spool erected" → "Erect Line 24-XX").
> 4. **Schedule Update:** Auto-update PMIS with extracted dates + confidence score. Flag low-confidence matches for manual review.
> 5. **Voice Interface:** Optional — use Whisper API for voice input from site supervisors.
>
> **Tech Stack:** Python (FastAPI), OpenAI GPT-4 API (extraction), sentence-transformers (fuzzy matching), pandas (spreadsheet parsing), React.js (dashboard).
>
> **Why this ranks #11:**
> - ✅ LLM-based extraction is cutting-edge and impressive
> - ✅ Fuzzy matching is a genuinely smart solution
> - ⚠️ Very niche domain — infrastructure project management
> - ⚠️ Synthetic data needed — no real Primavera files available
> - ⚠️ Complex integration of multiple components

---

### <a id="26163"></a>Problem Statement 26163

| **Problem Statement ID** | 26163 |
|---|---|
| **Problem Statement Title** | Security Assessment of the World Monitor application |
| **Organization** | National Technical Research Organisation (NTRO) |
| **Department** | National Technical Research Organisation (NTRO) |
| **Category** | Software |
| **Theme** | Smart Automation |
| **Youtube Link** | https://www.youtube.com/watch?v=-wws31Ol3mc |
| **Dataset Link** | App link - https://www.worldmonitor.app / Source Code: https://github.com/koala73/worldmonitor |

**Description:**

• **Background** The World Monitor application is a Web/ Mobile platform that provides users with real-time monitoring, analytics, and reporting features. The application handles user authentication, data visualization, API communication, and role-based access controls.

As a security analyst, the task is to evaluate the application's security posture and identify vulnerabilities that could compromise the confidentiality, integrity, or availability of the system.

• **Description** Conduct an authorized security assessment of the World Monitor application to:

1. Identify security vulnerabilities in the application.
2. Assess the potential impact of each vulnerability.
3. Demonstrate proof-of-concept exploitation in a controlled environment.
4. Recommend remediation measures to mitigate the identified risks.

• **Scope** The assessment should focus on:
• Authentication and session management
• Authorization and access control
• Input validation and data handling
• API security
• Client-side security controls
• Secure communication mechanisms
• Data storage and privacy protections

• **Success Criteria** The assessment is considered successful if:
• At least one valid vulnerability is identified and documented.
• Evidence supports the existence of the vulnerability.
• Risk and impact are clearly explained.
• Practical mitigation strategies are provided

• **Expected Solution/Deliverables:**

For each vulnerability discovered, provide:

• Vulnerability title
• Description
• Affected component
• Severity rating (e.g., CVSS)
• Steps to reproduce
• Proof of concept demonstrating the issue in a safe testing environment
• Business impact assessment
• Remediation recommendations

**Constraints:**
• Testing must be performed only on authorized systems.
• No actions should affect production users or data.
• Exploitation should be limited to proof-of-concept validation.
• Compliance with applicable laws, policies, and ethical hacking guidelines is required.

> **💡 Detailed Solution Approach:**
>
> **Core Architecture:** A **security audit + penetration testing project** — different from all others because it's an assessment, not a product build.
>
> **How it works:**
> 1. **Reconnaissance:** Analyze the GitHub source code for hardcoded secrets, API keys, exposed endpoints. Map the application's architecture.
> 2. **OWASP Top 10 Testing:** Systematically test for:
>    - SQL Injection (try input fields)
>    - XSS (inject scripts in input fields)
>    - Broken Authentication (test session management, JWT handling)
>    - IDOR (access other users' data by changing IDs)
>    - Insecure API endpoints (test without auth, with wrong roles)
>    - CSRF (test state-changing operations)
>    - Information disclosure (error messages, headers)
> 3. **Tools:** Burp Suite (intercept/proxy), OWASP ZAP (automated scanning), Postman (API testing), Nmap (port scanning), manual code review.
> 4. **Documentation:** Professional vulnerability report with CVSS scores, PoC screenshots/videos, and remediation code snippets.
>
> **Tech Stack:** Burp Suite, OWASP ZAP, Postman, Nmap, GitHub (code review), Markdown/PDF (reporting).
>
> **Why this ranks #12:**
> - ✅ Unique and different — stands out from typical "build an app" projects
> - ✅ NTRO is a prestigious organization — good for resume
> - ⚠️ Requires cybersecurity expertise — not everyone on the team may have it
> - ⚠️ No "product" to demo — it's a report and PoC
> - ⚠️ Risk: if the app is well-secured, finding vulnerabilities in 36 hours is hard
> - 💡 **Best for:** Teams with CTF/security backgrounds

---

## ⚠️ TIER 4 — High Risk / Low Feasibility

---

### <a id="26002"></a>Problem Statement 26002

| **Problem Statement ID** | 26002 |
|---|---|
| **Problem Statement Title** | Al-Based Smart Logistics and Accessibility Intelligence Platform for North Eastern Region (NER) |
| **Organization** | Ministry of Development of North Eastern Region (MDoNER) |
| **Department** | Ministry of Development of North Eastern Region (MDoNER) |
| **Category** | Software |
| **Theme** | Transportation & Logistics |

**Description:**

**Background:**

The North Eastern Region (NER) faces major logistics and accessibility challenges due to difficult terrain, extreme weather conditions, limited transport connectivity, and frequent road disruptions caused by landslides, floods, and infrastructure gaps. Transportation of essential goods such as medicines, food supplies, construction materials, and agricultural produce to remote districts often gets delayed, leading to supply shortages, increased costs, and disruption in public service delivery. Currently, there is no integrated intelligent platform that can provide real-time logistics visibility, route accessibility status, predictive disruption alerts, and optimized transportation planning for the region. To strengthen regional connectivity and support infrastructure-led development initiatives, there is a need for an Al-enabled logistics intelligence system tailored for the unique geographical and operational challenges of NER.

**Description:**

This problem statement seeks the development of an Al-powered Smart and in Logistics Accessibility Intelligence Platform for the North Eastern Region (NER) to address challenges related to difficult terrain, weather-induced disruptions, and limited transport connectivity remote areas. The platform should use Artificial Intelligence (Al), Machine Learning (ML), GIS mapping, weather data, and real-time field inputs to monitor transportation networks and improve movement of essential goods and services across the region. The platform should:

a. Monitoring real-time road, bridge, and transport accessibility across districts and remote locations b. Predicting possible route disruptions caused by landslides, floods, heavy rainfall, road damage, or traffic congestion c. Providing Al-based alternate route suggestions and estimated travel delays d. Tracking movement of vehicles carrying essential commodities, medicines, agricultural produce, and construction materials through GPS integration e. Generating automated alerts for blocked roads, inaccessible regions, delayed deliveries, and high-risk transport corridors f. Enabling field officials and local authorities to upload geo-tagged updates, photographs, and incident reports from remote locations g. Creating centralized dashboards for visualizing:

• District-wise connectivity status
• Logistics bottlenecks and supply chain gaps Emergency and disaster-time accessibility routes
• Real-time movement and delivery status of essential supplies h. Supporting multilingual notifications and offline data synchronization for low-network areas The platform should help improve regional connectivity, strengthen emergency response systems, reduce supply chain disruptions, and support efficient planning and monitoring of logistics operations in the North Eastern Region.

**Expected Solution:**

• A scalable Al-based software platform integrated with GIS and real-time analytics featuring:
• Al-powered route prediction and optimization engine
• GIS-enabled accessibility monitoring dashboard
• GPS-based vehicle tracking system
• Real-time alert and notification mechanism
• Mobile/web application for field-level reporting and monitoring Integration capability with weather APIs, transport databases, and government monitoring systems
• Cloud-based infrastructure with secure data management and offline support The platform should improve regional logistics efficiency, reduce supply disruptions, strengthen emergency response capability, and support infrastructure and economic development across the North Eastern Region.

> **💡 Detailed Solution Approach:**
>
> **Core Architecture:** A **GIS + logistics platform** — real-time road monitoring, predictive alerts, and vehicle tracking for the North East.
>
> **How it works (simplified):**
> 1. **GIS Dashboard:** Use Leaflet/Mapbox to display NER road network. Color-code roads by status (green/yellow/red).
> 2. **Disruption Prediction:** Train a classifier on historical weather + road closure data to predict disruptions.
> 3. **Vehicle Tracking:** Simulated GPS tracking with mock vehicle data.
> 4. **Alert System:** Automated notifications when disruptions are predicted.
>
> **Why this ranks #13:**
> - ⚠️ **Massive scope** — 8 major requirements is too many for 36 hours
> - ⚠️ Needs real GIS data for NER roads — hard to obtain
> - ⚠️ Weather API + prediction model + vehicle tracking + dashboards = too many moving parts
> - ⚠️ Hard to demo convincingly without real data
> - 💡 Could work if we drastically reduce scope to just the dashboard + alert system

---

### <a id="26197"></a>Problem Statement 26197

| **Problem Statement ID** | 26197 |
|---|---|
| **Problem Statement Title** | Student Innovation-Ideas that showcase the rich cultural heritage and traditions of India. |
| **Organization** | AICTE |
| **Department** | AICTE, MIC-Student Innovation |
| **Category** | Software |
| **Theme** | Heritage & Culture |

**Description:**

Student Innovation-Ideas that showcase the rich cultural heritage and traditions of India.

> **💡 Detailed Solution Approach:**
>
> This is open-ended — we can build anything related to Indian culture. Some ideas:
> 1. **AI-powered Heritage Guide:** Upload a photo of a monument/artifact → AI identifies it and narrates its history (image classification + knowledge base)
> 2. **Virtual Museum:** 3D walkthrough of Indian heritage sites using Three.js/WebXR
> 3. **Cultural Recipe Platform:** Regional recipes with AI-based ingredient substitution and video tutorials
> 4. **Language Preservation App:** Record and catalog endangered Indian languages with AI transcription
>
> **Why this ranks #14:**
> - ⚠️ Too vague — no clear problem to solve, hard to stand out
> - ⚠️ "Cultural heritage" has been done many times — hard to be innovative
> - ⚠️ Panel might not see a clear "problem-solution" fit
> - 💡 Would need a very specific, unique angle to win

---

### <a id="26204"></a>Problem Statement 26204

| **Problem Statement ID** | 26204 |
|---|---|
| **Problem Statement Title** | Student Innovation-A solution/idea that can boost the current situation of the tourism industries including hotels, travel and others. |
| **Organization** | AICTE |
| **Department** | AICTE, MIC-Student Innovation |
| **Category** | Software |
| **Theme** | Travel & Tourism |

**Description:**

Student Innovation-A solution/idea that can boost the current situation of the tourism industries including hotels, travel and others.

> **💡 Detailed Solution Approach:**
>
> Open-ended — tourism solutions. Some ideas:
> 1. **AI Trip Planner:** Input budget + interests + dates → AI generates personalized itinerary with hotels, transport, activities
> 2. **AR Heritage Overlay:** Point phone at a historical site → see historical reconstruction overlaid on real view
> 3. **Tourism Chatbot:** Multilingual chatbot for tourist queries about any Indian destination
>
> **Why this ranks #15:**
> - ⚠️ Same problem as 26197 — too vague, too broad
> - ⚠️ Tourism is oversaturated in hackathons
> - ⚠️ Hard to differentiate from existing apps (MakeMyTrip, etc.)
> - 💡 Would need a very novel angle

---

### <a id="26027"></a>Problem Statement 26027

| **Problem Statement ID** | 26027 |
|---|---|
| **Problem Statement Title** | Al-Powered Automatic Block Planning to Maximize Asset Availability for Train Operations on Indian Railways |
| **Organization** | Ministry of Railways |
| **Department** | Ministry of Railways |
| **Category** | Software |
| **Theme** | Transportation & Logistics |

**Description:**

Background: Railway maintenance for fixed infrastructure of Engineering, Traction Distribution, and Signal & Telecommunication departments is currently planned independently. Each department requests maintenance blocks/disconnections via the BDMS system. This planning process is decentralized and manual. This often leads to inefficient block utilization, poor coordination, and suboptimal scheduling,which may reduce asset availability and impact train operations. Detailed Description: Maintenance data-such as defects and overdue tasks—is maintained separately in systems like Track Management System (TMS), Signalling Maintenance & Management System (SMMS), and Traction Distribution Management System (TDMS). Meanwhile, the Control Office Application (COA) manages block corridor availability. Without integration and coordinated scheduling, maintenance blocks/disconnections are not optimally planned, resulting in asset downtime and reduced availability of fixed infrastructure for train operation.Your task is to develop an Automatic Block Planning system that integrates maintenance, defects and corridor data to generate optimized block schedules. The system should prioritize maintenance activities to minimize asset downtime and maximize the availability of critical infrastructure, ensuring uninterrupted train operations.

**Expected Solution:**

Participants should build an Al system that includes:

1. Integration of maintenance data (defects, overdue maintenance) from TMS, SMMS, and TDMS with corridor block and block availability as per the Train Time Table and the goods trains forecast from the Control Office.

2. Uses AI/ML algorithms to prioritize and schedule maintenance tasks based on criticality, urgency, and impact on asset availability.

3. Optimize block scheduling to maximize asset uptime by minimizing downtime and efficiently coordinating multi-department activities.

4. Provides block plans over multiple time horizons-weekly and monthly—to support both short-term and long-term maintenance.

The solution should transform current decentralized and manual block planning into a data-driven, coordinated process that maximizes asset availability, improves safety, and supports reliable train operations.

> **💡 Detailed Solution Approach:**
>
> **Core Architecture:** A **constraint optimization + scheduling system** for railway maintenance blocks.
>
> **How it works:**
> 1. Model the problem as a constraint satisfaction/optimization problem
> 2. Constraints: train timetable, corridor availability, maintenance urgency, department dependencies
> 3. Use OR-Tools, PuLP, or a genetic algorithm to optimize block allocation
> 4. Output: optimized weekly/monthly maintenance schedule
>
> **Why this ranks #16:**
> - ⚠️ **Deep domain knowledge required** — railway maintenance is extremely specialized
> - ⚠️ No access to real railway data (TMS, SMMS, TDMS are internal systems)
> - ⚠️ Need to understand railway operations to build anything meaningful
> - ⚠️ Optimization without real data = toy demo
> - 💡 Would need significant railway domain research first

---

### <a id="26051"></a>Problem Statement 26051

| **Problem Statement ID** | 26051 |
|---|---|
| **Problem Statement Title** | Software Based Model Development for Design of Area Specific Shelter for Thermal Comfort Maintenance |
| **Organization** | DRDO |
| **Department** | Department of Defence Production /IDEX |
| **Category** | Software |
| **Theme** | Miscellaneous |

**Description:**

• **Background:**

The ambient atmospheric condition affects the temperature inside the shelter and makes thermal management necessary for maintenance of temperature in the comfortable range. The existing shelters for any region are generally not designed as per the requirements of a particular region and hence not energy efficient thus demands external thermal comfort maintenance system. Area specific designed shelters looks smart and one time solution for thermal management as per the atmospheric condition of the region.

This model development project work is specifically conceptualised keeping in mind the tough climatic condition of High Altitude cold Region like Ladakh and can be used for studying the design requirements of other climatic region shelters as well.

• **Description:**

The Ladakh region is blessed with high solar energy irradiance (1900-2100 kwh/m2/year) along with long average sunshine duration of 7.9 hours with 300 plus average annual cloud free days. The temperatures inside the shelters found suitable during day hours even during the winter period due to trapping of thermal energy from solar radiation, but approach nearly the ambient atmospheric temperature after sunset. High thermal losses through the material of the shelter and openings contributed towards such low temperature inside shelters.

A detailed thermal analysis of the shelter including size, shape orientation etc. along with, study related to application of suitable materials and application of thermal mass storage material, composite multi-material etc. and effect of openings on outcome looks to be a potential solution for development of self-sufficient passive shelter for the region in terms of temperature maintenance.

A general model development in ANSYS software to thermally simulate the shelter for study of heat losses and capture of real time atmospheric ambient climatic condition data will prove to be helpful. The project is conceptualised for the development of general model in ANSYS software. The model should be user friendly and works on user defined values (real time data, material properties etc.) to simulate the cases along with comparative analysis with different materials under same ambient condition to predict the most efficient combination of materials, shape, and size etc. in terms of temperature maintenance.

The primary objective of the work/project is to minimize the energy utilisation for thermal comfort maintenance in particular and minimization of fossil fuel application in general by designing of area specific self-sustained standalone passive shelter at defined atmospheric climatic condition.

• **Expected Solution:**

Development of Software based model for predicating the suitable shelter design including suitable material, size, shape etc. with the objective of thermal comfort maintenance in passive shelter installed in different atmospheric conditions. This work involves simple feeding of collected data and material properties in developed model and outcome shows in terms of most efficient design with materials for thermal comfort maintenance in a particular region.

The Developed Model should be capable of giving/solving the following tasks:

1. Prediction of shelter inside temperature based on the user defined inputs.
2. Prediction of thermal energy generated from solar radiation.
3. Heat flow details as per the temperature difference between ambient and shelter temperature for a defined time period.

> **💡 Detailed Solution Approach:**
>
> **Core Architecture:** An **ANSYS thermal simulation model** — finite element analysis of shelter heat transfer.
>
> **Why this ranks #17:**
> - ⚠️ **Requires ANSYS expertise** — specialized engineering software
> - ⚠️ Thermal simulation requires physics/engineering background
> - ⚠️ Not a typical hackathon project — more of an engineering research project
> - ⚠️ Hard to demo as a "software product"
> - 💡 Only viable if team has mechanical/thermal engineering members with ANSYS experience

---

### <a id="26037"></a>Problem Statement 26037

| **Problem Statement ID** | 26037 |
|---|---|
| **Problem Statement Title** | Adaptive Path Planning and Collision Avoidance for Autonomous Vehicles on Unstructured Indian Roads |
| **Organization** | MathWorks |
| **Department** | MathWorks |
| **Category** | Software |
| **Theme** | Smart Vehicles |

**Description:**

**Background:**

Most autonomous driving systems are developed for roads with clear lane markings, standard signage, predictable traffic flow, and controlled intersections. Indian roads are often very different. Vehicles of many types share the same space, including cars, buses, trucks, auto-rickshaws, two-wheelers, bicycles, pedestrians, pushcarts, and animals. Drivers and pedestrians may change direction suddenly, merge without signalling, drive against traffic, or cross at unmarked locations. In many areas, road edges are unclear, potholes are common, and formal lane discipline is limited. These conditions make it difficult for traditional path planning methods that depend on structured road geometry and predictable motion. India has a large and diverse road network that includes village roads, crowded market areas, urban intersections, and highways. To support the safe deployment of autonomous vehicles in such environments, students must build planning systems that can adapt in real time to uncertainty, mixed traffic, and changing road conditions.

**Description:**

Design and simulate an adaptive path planning system for an autonomous vehicle that operates in unstructured Indian road conditions. The system should perceive the environment using a multi-sensor setup such as camera, LiDAR, and radar, and identify diverse road users and obstacles, including auto-rickshaws, pushcarts, pedestrians, and animals. It should predict the short-term motion of surrounding agents, including non-lane-based and irregular movement patterns, and generate a safe, collision-free path that can be replanned in real time. The solution should also handle practical driving situations such as missing lane markings, informal merging, sudden pedestrian movement, and unexpected obstacles on the road. Teams should validate their solution using at least five realistic Indian road scenarios, such as an unmarked village road, a busy urban intersection without signals, a highway merge involving slow-moving vehicles, a dense market area with mixed traffic, and a sudden cattle-crossing event. Teams are encouraged to use MathWorks tools such as RoadRunner for scenario design, Automated Driving Toolbox for sensor modeling and fusion, Navigation Toolbox and Stateflow for planning and decision logic, Vehicle Dynamics Blockset or a Simulink bicycle model for vehicle behavior, and Deep Learning Toolbox for detection and trajectory prediction.

**Expected Solution:**

The expected solution should include three main parts. First, teams should build a working simulation pipeline that integrates perception, prediction, path planning, decision logic, and vehicle motion in MATLAB and Simulink. Second, teams should create realistic driving scenarios that represent Indian road conditions, including at least two detailed RoadRunner scenes such as a village road and an urban intersection, and use them to test the vehicle across all five required scenarios. Third, teams should present results that show safe and reliable navigation, including collision-free performance, smooth path generation, and timely replanning during changing road conditions. The final submission should include the simulation model, the designed scenarios, performance results with metrics such as replanning latency, path smoothness, and scenario completion rate, a short technical report that explains the approach and design choices, and a demonstration video that shows the vehicle navigating the test scenarios. The solution should demonstrate closed-loop validation of autonomous driving behavior under realistic mixed-traffic conditions.

**Datasets:**
Teams may use built-in sensor and scenario datasets available in MathWorks Automated Driving Toolbox, RoadRunner sample scenes, synthetic scenarios created by the team, and publicly available traffic datasets relevant to Indian road conditions.
- Indian Driving Dataset (IDD): https://idd.insaan.iiit.ac.in/
- Mendeley traffic dataset

> **💡 Detailed Solution Approach:**
>
> **Core Architecture:** A **MATLAB/Simulink simulation pipeline** — perception → prediction → planning → vehicle dynamics.
>
> **Why this ranks #18 (last):**
> - ⚠️ **Requires MATLAB/Simulink licenses** — not freely available
> - ⚠️ Autonomous driving simulation is extremely complex
> - ⚠️ Need RoadRunner (specialized scenario design tool)
> - ⚠️ 5 required scenarios + metric reporting = massive workload
> - ⚠️ MathWorks-specific toolchain — very niche skill set
> - ⚠️ Almost impossible to build a convincing demo in 36 hours
> - 💡 Only viable for teams with prior MATLAB/autonomous driving experience AND active licenses

---

## 📊 Final Rankings Summary

| Rank | ID | Problem Statement | Feasibility | Wow Factor | Impact | Risk | Verdict |
|---|---|---|---|---|---|---|---|
| 🥇 | 26107 | BIS Standards Assistant | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐ | Low | **TOP PICK** |
| 🥈 | 26031 | Onion Quality Grading | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐ | Low | **STRONG** |
| 🥉 | 26090 | Artisan Market Linkage | ⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ | Low | **STRONG** |
| 4th | 26032 | Farmer Procurement | ⭐⭐⭐⭐⭐ | ⭐⭐⭐ | ⭐⭐⭐⭐ | Low | **SAFE** |
| 5th | 26092 | Scheme Matching | ⭐⭐⭐⭐ | ⭐⭐⭐⭐ | ⭐⭐⭐⭐ | Low | **SAFE** |
| 6th | 26132 | Farmer Market Linkages | ⭐⭐⭐⭐ | ⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ | Med | **GOOD** |
| 7th | 26062 | Polar Expedition | ⭐⭐⭐⭐ | ⭐⭐⭐ | ⭐⭐⭐ | Med | **DECENT** |
| 8th | 26135 | Skilling Outcomes | ⭐⭐⭐⭐ | ⭐⭐⭐ | ⭐⭐⭐⭐ | Med | **DECENT** |
| 9th | 26108 | Standards Recommender | ⭐⭐⭐⭐ | ⭐⭐⭐⭐ | ⭐⭐⭐⭐ | Low | **Good if combined w/ 26107** |
| 10th | 26061 | Polar Energy Mgmt | ⭐⭐⭐ | ⭐⭐⭐ | ⭐⭐⭐ | Med | **RISKY** |
| 11th | 26122 | Infrastructure Data | ⭐⭐⭐ | ⭐⭐⭐⭐ | ⭐⭐⭐⭐ | Med | **RISKY** |
| 12th | 26163 | Security Assessment | ⭐⭐⭐ | ⭐⭐⭐⭐ | ⭐⭐⭐ | High | **SPECIALIST ONLY** |
| 13th | 26002 | NER Logistics | ⭐⭐ | ⭐⭐⭐ | ⭐⭐⭐⭐ | High | **TOO BROAD** |
| 14th | 26197 | Cultural Heritage | ⭐⭐⭐ | ⭐⭐ | ⭐⭐ | High | **TOO VAGUE** |
| 15th | 26204 | Tourism Solution | ⭐⭐⭐ | ⭐⭐ | ⭐⭐ | High | **TOO VAGUE** |
| 16th | 26027 | Railway Block Planning | ⭐⭐ | ⭐⭐⭐ | ⭐⭐⭐⭐ | High | **DOMAIN HEAVY** |
| 17th | 26051 | DRDO Shelter Design | ⭐ | ⭐⭐ | ⭐⭐⭐ | Very High | **SPECIALIST ONLY** |
| 18th | 26037 | Autonomous Vehicles | ⭐ | ⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ | Very High | **NEEDS MATLAB LICENSES** |

---

## 🎯 Recommended Strategy

**Primary Pick:** 26107 (BIS Assistant) — highest feasibility + highest wow factor
**Backup Pick:** 26031 (Onion Grading) — visual demo + clear scope
**Wildcard Pick:** 26090 (Artisan Linkage) — strongest social impact narrative

If your team has cybersecurity skills, 26163 (Security Assessment) is a unique dark horse.
If your team has MATLAB experience, 26037 (Autonomous Vehicles) could be a massive differentiator.

---

*Last updated: August 2026*
