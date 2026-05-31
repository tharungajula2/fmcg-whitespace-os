# FMCG Whitespace OS — SOURCE OF TRUTH (Pistachio Blueprint)
**Maturity State:** Strategic Portfolio Asset / Strategy Concept Prototype  
**Version:** 2.0 (Professional Pivot)  
**Last Codebase Verification:** 2026-05-31  

---

## A. Brand Positioning & Product Philosophy

The **FMCG Whitespace OS** (historically referenced during early development as "PAUSE") is a premium, systems-minded portfolio asset designed to showcase advanced product management capabilities in the consumer goods space. It models the disciplined execution of introducing disruptive, high-retention products into legacy FMCG markets.

### 1. The Core Strategic Thesis
Legacy FMCG players are structurally slow to adapt to changing consumer preferences. FMCG Whitespace OS demonstrates how newer, repositioned brands can capture market share by standing on the street, observing unfiltered behavioral cues, and identifying critical gaps in everyday nutrition and habits.

### 2. Core Pillars of the Brand Study
*   **Whitespaces Everywhere:** Spotting overlooked consumer formats (e.g., merging premium indulgence with everyday routine health).
*   **Functional Indulgence:** Moving away from standard, dry "fitness" marketing. Indulgence is a mass driver; health is a quiet default value. We build high-appeal sensory formats that silently deliver functional benefits.
*   **The Math of Taste (Optimization):** Treating "Better-for-you" foods as a rigorous optimization problem. We identify and strip out guilt-heavy ingredients (like excess sugar and high fats) and replace them with high-tech alternatives, adjusting dimensions (like biscuit thickness or liquid viscosity) to protect the crucial "Love and Like" taste bracket.
*   **Damage Control Approach:** Meeting consumers where they are. We reduce the physiological toll of modern eating behaviors (e.g., portion control, lactase-treated digestibility) rather than demanding an unrealistic, total lifestyle change.
*   **Unit Economics First:** Strategy is irrelevant if the customer-lifetime-value to customer-acquisition-cost (LTV:CAC) loop fails in the price-sensitive, quick-commerce-dominated Indian retail landscape.

---

## B. Design System & Aesthetics ("Performance Editorial")

The interface is styled around a customized, premium visual concept known as the **Pistachio Accent System**. It uses vanilla CSS variables in tandem with Tailwind CSS v4's compiler layer to project a serene, high-agency editorial voice (combining classic serif elegance with clean, performance-minded typography).

### 1. Custom Color Tokens (`app/globals.css`)
```css
:root {
  --background: #F5ECD7; /* Vanilla Cream — from Café Latte bottle */
  --foreground: #2B1A15; /* Espresso Ink — Grounded and authoritative */
  
  /* Accent System — Functional & Performance-focused */
  --pistachio: #4B633C; /* Darkened for better readability and authority */
  --pistachio-strong: #3A4D2E; /* Heavy Performance Green */
  --pistachio-soft: rgba(75, 99, 60, 0.4);
  --pistachio-subtle: rgba(75, 99, 60, 0.14);
  
  /* Neutral Grounding */
  --border-warm: #CFC3B0; 
  --graphite: #E8DCC8; /* Warm Sand — card surfaces */
  
  /* Product Accents — Sourced for artwork/flavor representation */
  --accent-choco: #8B4513;
  --accent-pista: #93C572;
  --accent-vanilla: #F3E5AB;
  --accent-coffee: #6F4E37;
  --accent-bar: #4A2B29;
  --accent-cocoa: #8A5A3B;

  /* Semantic Aliases */
  --accent: var(--pistachio);
  --accent-soft: var(--pistachio-soft);
  --accent-subtle: var(--pistachio-subtle);
  --muted-gold: var(--foreground);
}
```

### 2. Modern Typography Systems
*   **Serif Headings:** Cormorant Garamond (`var(--font-cormorant)`) — provides a classic, editorial feel for title layers (`h1, h2, h3, h4`).
*   **Sans-Serif Body:** Geist Sans (`var(--font-geist-sans)`) — clean, ultra-readable metrics optimized for quantitative breakdowns.

### 3. Premium Atmospheric Custom Classes
*   `glass-card`: Transparent container layer using `backdrop-filter: blur(16px)` with high hover responsive transitions.
*   `film-surface`: Soft vertical gradients transitioning smoothly to the vanilla background overlay.
*   `haze-overlay`: Radial backdrop element (`filter: blur(80px)`) creating a modern, diffused branding aura.
*   `vignette-atmosphere`: Radial masks mimicking a cinematic vignette look for background wrapper boundaries.
*   `sheen-effect`: Subtle gradient glow animation sliding across interactive buttons and cards upon hover.
*   `animate-float` / `animate-float-slow`: Pure CSS float animations translating elements vertically and rotating them slightly to mimic light, suspended bottles or items.

---

## C. System Requirements & Dependency Versions

The application is built on modern React 19 frameworks integrated into Next.js 16. It leverages PostCSS processing for custom Tailwind integration.

### 1. Project Dependencies (`package.json`)
```json
{
  "name": "fmcg-whitespace-os",
  "version": "0.1.0",
  "private": true,
  "scripts": {
    "dev": "next dev",
    "build": "next build",
    "start": "next start",
    "lint": "eslint"
  },
  "dependencies": {
    "gsap": "^3.14.2",
    "next": "16.2.3",
    "react": "19.2.4",
    "react-dom": "19.2.4"
  },
  "devDependencies": {
    "@tailwindcss/postcss": "^4",
    "@types/node": "^20",
    "@types/react": "^19",
    "@types/react-dom": "^19",
    "eslint": "^9",
    "eslint-config-next": "16.2.3",
    "tailwindcss": "^4",
    "typescript": "^5"
  }
}
```

### 2. Path Aliases (`tsconfig.json`)
Explicit TypeScript resolution matches `@/*` mapping directly to the root `./*` directory (e.g. `@/app/types` resolves to `./app/types`).

---

## D. Architecture & Directory Mapping

```
fmcg-whitespace-os/
├── app/
│   ├── components/               # Module-wise components partitioned by layout zones
│   │   ├── channels/             # Channel mapping cards and visual grids
│   │   ├── growth/               # Occasion loops and retention diagrams
│   │   ├── hero/                 # Ambient home hero sections and cinematic headers
│   │   ├── labs/                 # Flavor and formulation interactive slots
│   │   ├── layout/               # Shared global components (Header, Navigation)
│   │   ├── research/             # Modular interactive workbook chapter components
│   │   │   ├── EditorialCallout.tsx
│   │   │   ├── EditorialChapter.tsx
│   │   │   ├── EditorialTable.tsx
│   │   │   ├── FlavorLab.tsx
│   │   │   ├── ImageSlot.tsx
│   │   │   ├── PasswordGate.tsx   # Secured gating UI component (bypassed in current build)
│   │   │   ├── QCIntelligence.tsx
│   │   │   ├── StickyNotesChapter.tsx
│   │   │   ├── WorkbookChapter.tsx
│   │   │   └── WorkbookTableOfContents.tsx
│   │   └── ui/                   # High-fidelity custom form inputs and button systems
│   ├── data/                     # Centralized Static Data registries (The Single Sources of Truth)
│   │   ├── growth.ts             # Consumer growth messaging frames
│   │   ├── navigation.ts         # Navigation routes schema and footer targets
│   │   ├── occasions.ts          # Daily routine attachment occasions data
│   │   ├── outreach.ts           # Outreach targets and tactical initiatives
│   │   ├── products.ts           # Product details, strategic parameters, and risk profiles
│   │   ├── research-wip-data.ts  # Master copy database containing Chapters 00 to 09
│   │   ├── site-content.ts       # Hero details, vision statements, and outreach messaging
│   │   └── summer-concepts.ts    # Custom product concepts for trial and seasonality
│   ├── types/
│   │   └── index.ts              # Global TypeScript structural models
│   ├── globals.css               # HSL color variables, theme configurations, custom CSS animations
│   ├── how-i-can-help/
│   │   └── page.tsx              # Growth Strategy memo interface (/how-i-can-help)
│   ├── layout.tsx                # Master page wrapper loading Geist and Cormorant fonts
│   ├── page.tsx                  # Landing entrance featuring background cinematic video (/home)
│   ├── products/
│   │   └── page.tsx              # Comprehensive Product Lab / Strategy details (/products)
│   └── research-wip/
│       ├── page.tsx              # Master study index layer (Disables Web Indexing)
│       └── ResearchWipClient.tsx # Client orchestrator resolving workbook chapters dynamically
├── public/
│   ├── images/                   # High-res transparent product illustrations
│   └── videos/                   # Cinematic premium placeholder video layers
├── shelf/                        # Backups and content sheets
│   └── RESEARCH_WIP_MASTER_CONTENT.md # Critical raw copy database of research workbook chapters
├── next.config.ts                # Serves redirections, security settings, and environment aliases
├── tsconfig.json                 # Path resolutions and ES compiler options
└── package.json                  # Precise stack version lock
```

---

## E. Core Data Schema

The data structures of the FMCG Whitespace OS are programmatically typed to ensure consistent representation across the portfolio pages and components.

### 1. Product Interface (`app/types/index.ts`)
Tracks the parameters used to analyze and position each product concept.
```typescript
export interface Product {
  id: string;
  slug: string;
  name: string;
  format: 'Coffee' | 'Bar' | 'Drink' | 'Supplement';
  heroDescriptor: string;
  operatorDescription: string;
  primaryOccasion: string;
  accentColor: string;
  imagePath: string;
  category: string;
  
  // Strategic Intelligence
  strategicRole: string;
  repeatLogic: string;
  channelFit: string[];
  operatorNote: string;
  themeColor: string;
  
  // Thesis Journey Overlays
  portfolioClassification: 'Hero' | 'Repeat' | 'Wedge' | 'Support' | 'Indulgence';
  riskLevel: 'Low' | 'Moderate' | 'High';
  expansionCaution: string;
  cannibalizationRisk: string;
  strategicWeight: number;
}
```

### 2. Occasion Interface
Associates occasions with direct triggers and consumer behaviors.
```typescript
export interface Occasion {
  id: string;
  title: string;
  humanDescription: string;
  behavioralState: string;
  winningFormat: string;
  messageThatWorks: string;
  repeatTrigger: string;
  channelEdge: string;
  riskFriction: string;
  themeColor: string;
  bestFitProductIds: string[];
}
```

### 3. Workbook Chapter Structure
Models content blocks to resolve different layouts inside the workspace.
```typescript
export interface WorkbookChapter {
  id: string;
  title: string;
  eyebrow: string;
  summary: string;
  type?: 'study' | 'editorial' | 'sticky-notes' | 'qc-intelligence' | 'flavor-lab';
  blocks?: WorkbookBlock[];         // Standard structured study card layout
  sections?: EditorialSection[];     // Magazine-style editorial columns
  stickyNotes?: StickyNote[];        // Unfiltered signals boards
  imagePlaceholder?: {
    label: string;
    description: string;
    imagePath?: string;
  };
}

export interface WorkbookBlock {
  id: string;
  type: 'prompt' | 'question' | 'hypothesis' | 'validation' | 'risk';
  title: string;
  body: string;
}

export interface StickyNote {
  id: string;
  title: string;
  body: string;
  status: 'OPEN' | 'CLOSED';
}
```

---

## F. Permanent Next.js Server-Side Redirects

To prevent broken links across older versions of the portfolio, the Next.js router explicitly maps legacy paths to their active equivalents.

All redirects are configured with `permanent: true` (HTTP 301) inside `next.config.ts`:

| Source Path | Destination Path |
| :--- | :--- |
| `/strategy` | `/how-i-can-help` |
| `/economics` | `/how-i-can-help` |
| `/channels` | `/products` |
| `/growth` | `/products` |
| `/occasions` | `/products` |
| `/labs/packaging` | `/how-i-can-help` |
| `/labs/flavor` | `/products` |
| `/labs/manufacturing` | `/how-i-can-help` |
| `/labs/r-and-d` | `/how-i-can-help` |
| `/labs/expansion` | `/how-i-can-help` |
| `/products/:slug` | `/products` |

---

## G. Centralized Databases & Strategic Profiles

### 1. Active Portfolio SKU Registry (`app/data/products.ts`)
The product catalog consists of 5 strategic beverage prototypes, each serving a unique commercial function:

*   **Rich Cold Coffee (Daily Ritual Anchor)**
    *   *Strategic Role:* High-frequency, low-barrier anchor designed to attach protein to the existing daily caffeine ritual.
    *   *Indulgence Moat:* Looks and tastes like a premium coffee-house product, hiding nutritional content.
    *   *Occasion:* Anytime craving.
    *   *Classification:* `Hero` | *Risk:* Low.
*   **Rosy Falooda (Cultural Nostalgia Wedge)**
    *   *Strategic Role:* Nostalgia-coded, high-viscosity formulation that taps into emotional memory loops with zero guilt.
    *   *Indulgence Moat:* Unmatched regional dessert-coded familiarity.
    *   *Occasion:* Evening indulgence.
    *   *Classification:* `Wedge` | *Risk:* Low.
*   **Mango Tango (Seasonal Volume Driver)**
    *   *Strategic Role:* Mass trial builder that leverages India's highest-volume summer flavor profile.
    *   *Indulgence Moat:* Natural pulp sensation bypassing artificial notes.
    *   *Occasion:* Summer afternoon.
    *   *Classification:* `Hero` | *Risk:* Moderate (highly seasonal).
*   **Thandai Chill (Heritage Premium Extension)**
    *   *Strategic Role:* Premium traditional drink integrating high-grade saffron, almonds, and traditional spices.
    *   *Indulgence Moat:* High cultural credibility bridging tradition with modern nutritional goals.
    *   *Occasion:* Festive season or evening wind-down.
    *   *Classification:* `Support` | *Risk:* Low.
*   **Coco Chill (Premium Urban Refresh)**
    *   *Strategic Role:* Lighter, hydrative, recovery-focused refreshing lane targeted at premium urban consumers.
    *   *Indulgence Moat:* Sophisticated look, low sweetness, clean texture.
    *   *Occasion:* Post-workout or afternoon reset.
    *   *Classification:* `Indulgence` | *Risk:* Low.

---

## H. Dynamic Strategic Workbook & Gating Logic

The **Research WIP** space (`/research-wip`) acts as an interactive study mapping food science, unit economics, supply chains, and consumer profiles.

### 1. Modular Chapters Structure (`app/data/research-wip-data.ts`)
*   **Chapter 00-sticky-notes (`type: 'sticky-notes'`):** 4 raw, open insights detailing product design vs fitness branding, occasion attachment, and quick commerce dynamics.
*   **Chapter 01-growth-intelligence (`type: 'qc-intelligence'`):** Interactive dashboards rendering quick commerce channel analysis and search volume dynamics.
*   **Chapter 02-product-lab (`type: 'flavor-lab'`):** Formulation lab matrix showcasing ingredient selection, viscosity, and moisture metrics.
*   **Chapter 03-visionary-essence (`type: 'editorial'`):** Detailed mapping of "The Core Thesis" (price expectations, food science, and identifying whitespaces).
*   **Chapter 04-supply-chain (`type: 'editorial'`):** Deep dive into essential amino acids, PDCAAS vs DIAAS metrics, and ultra-filtered milk technology. Includes detailed raw manufacturing processes and retort sterilizing waterflows.
*   **Chapter 05-consumer-reality (`type: 'editorial'`):** Structural data on Indian protein intake, trust verification systems, and the South Indian genetic moat (lactose-free formulations addressing a 66% intolerance profile).
*   **Chapter 06-unit-economics (`type: 'editorial'`):** The full financial model of D2C vs Quick Commerce margin cascades:
    *   *Gross Metrics:* MRP **Rs 110**, Net Selling Price **Rs 88**, COGS **Rs 40-48** (36-44% of MRP), CM2 margin after shipping **14-27%**, with break-even calculated at **4 repeat purchases** based on a **22% repeat rate**.
    *   *Comparison Benchmarks:* Epigamia (Rs 141), Yogabar (Rs 131), Phab (Rs 125) vs Amul's value floor (Rs 50 for 20g protein).
*   **Chapter 07-competitive-identity (`type: 'editorial'`):** Positioning architecture modeling Indian health food across 7 distinct brand tiers.
*   **Chapter 08-risk-mapping (`type: 'editorial'`):** Audit of taste-repeat deficiencies, ASCI/FSSAI regulatory claims, and product damage thresholds.
*   **Chapter 09-strategic-unresolveds (`type: 'editorial'`):** Interactive strategic catalog containing open questions across operations, consumer behavior, and brand trust.

### 2. Interactive Note-Taking System
Users can jot down notes on each module. Notes are persisted on the client's device using standard browser mechanics inside the `ResearchWipClient` container:
*   Initial render loads saved text strings: `localStorage.getItem('research_wip_notes')`.
*   Note edits fire state updates, persisting data to disk asynchronously via `localStorage.setItem('research_wip_notes', ...)`.

### 3. Password Gating (Inactive Framework Component)
The workspace features a styled security gate component at `app/components/research/PasswordGate.tsx` which:
*   Takes an `onUnlock` handler to validate input.
*   Is configured with a hardcoded passcode: `pause26`.
*   Displays error states with dynamic feedback animations (shake effects, 2-second timeout resets) upon failure.
*   *Note:* The main wrapper `ResearchWipClient.tsx` currently bypasses the gate, rendering the workbook modules directly to ensure recruiters can view the content without barrier.

---

## I. Zero-to-One Developer Rebuild Checklist

Follow these step-by-step instructions to rebuild the FMCG Whitespace OS project exactly as it is configured today.

### Step 1: Bootstrap the Project Base
Initialize a clean Next.js application using standard npx script protocols:
```powershell
npx -y create-next-app@latest fmcg-whitespace-os --ts --src-dir=false --app --eslint --import-alias="@/*" --use-npm
```
*Note: Make sure to navigate inside the generated folder and confirm that your file system structure matches `/app` routes directly instead of routing through a `/src` parent directory.*

### Step 2: Configure System Dependencies
Update your `package.json` to lock down core framework versions:
```json
"dependencies": {
  "gsap": "^3.14.2",
  "next": "16.2.3",
  "react": "19.2.4",
  "react-dom": "19.2.4"
}
```
Install the necessary package tree:
```powershell
npm install
```

### Step 3: Set Up Tailwind CSS v4 & PostCSS Configurations
1.  Verify that your PostCSS config file (`postcss.config.mjs`) loads `@tailwindcss/postcss`:
    ```javascript
    export default {
      plugins: {
        '@tailwindcss/postcss': {},
      },
    };
    ```
2.  Set up the `@import "tailwindcss";` compiler header inside `app/globals.css`, followed immediately by your custom colors, custom fonts, `@theme inline` aliases, and premium design system CSS styles.

### Step 4: Map Server Routing & Permanent Redirects
Copy the audited redirect routes map into `next.config.ts` to ensure compatibility across client paths:
```typescript
import type { NextConfig } from "next";

const nextConfig: NextConfig = {
  async redirects() {
    return [
      { source: '/strategy', destination: '/how-i-can-help', permanent: true },
      { source: '/economics', destination: '/how-i-can-help', permanent: true },
      { source: '/channels', destination: '/products', permanent: true },
      { source: '/growth', destination: '/products', permanent: true },
      { source: '/occasions', destination: '/products', permanent: true },
      { source: '/labs/packaging', destination: '/how-i-can-help', permanent: true },
      { source: '/labs/flavor', destination: '/products', permanent: true },
      { source: '/labs/manufacturing', destination: '/how-i-can-help', permanent: true },
      { source: '/labs/r-and-d', destination: '/how-i-can-help', permanent: true },
      { source: '/labs/expansion', destination: '/how-i-can-help', permanent: true },
      { source: '/products/:slug', destination: '/products', permanent: true },
    ];
  },
};

export default nextConfig;
```

### Step 5: Initialize the Centralized Data Layers
Create database files under `app/data/` exactly corresponding to the data formats, including `products.ts`, `occasions.ts`, `summer-concepts.ts`, `outreach.ts`, and the comprehensive chapters manifest `research-wip-data.ts`.

### Step 6: Assemble the Routing Pages
1.  **Home (`/`):** Set up a responsive entry point with cinematic background masking effects inside `app/page.tsx`.
2.  **Product Lab (`/products`):** Implement the strategic product detail cards mapped to active static SKUs under `app/products/page.tsx`.
3.  **Growth Memo (`/how-i-can-help`):** Configure occasion grids and PM initiatives maps inside `app/how-i-can-help/page.tsx`.
4.  **Strategic Workbook (`/research-wip`):** Build a no-index search wrapper page inside `app/research-wip/page.tsx`, and orchestrate modular chapter views (sticky-notes, qc-intelligence, flavor-lab, editorial, study) via the `ResearchWipClient` framework.

### Step 7: Build & Audit Verify
Verify typescript compliance and build execution:
```powershell
npm run build
```
Start the local server environment:
```powershell
npm run dev
```
Navigate to `http://localhost:3000` to verify interactive transitions, note storage functionality, and active server redirects.
