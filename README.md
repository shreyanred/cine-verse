# CineVerse 🎬✨
> *"Your next great movie is waiting."*

A world-class, premium movie discovery and recommendation platform blending the depth of **Letterboxd**, the data credibility of **IMDb & Metacritic**, the user experience of **Netflix**, and the visual artistry of modern cinematic portfolios.

---

## 🌟 Key Features

1. **Full-Screen Cinematic Hero Banner**:
   - Continuous Ken Burns parallax zoom motion on high-res backdrops.
   - Smooth auto-advancing carousel with progress indicators.
   - High-definition official YouTube trailer embeds.
   - Instant "Watch Trailer", "Explore Movie", and "Add to Watchlist" actions.

2. **Top 10 Movies in the World (Transparent Bayesian Canon)**:
   - Evaluated using the **CineVerse Bayesian Consensus Algorithm (CBCA-v2)**.
   - Blends verified Rotten Tomatoes Tomatometer, Metacritic Metascores, and IMDb audience volume.
   - Transparent "How is this ranked?" modal explaining sample reliability shrinkage factors ($m = 50,000$, $C = 7.15$).
   - Dramatic 1–10 typography with horizontal scrolling carousel.

3. **Intelligent Movie Recommendation Engine**:
   - **Option A (Natural Language Semantic Input)**: Enter descriptive prompts like *"I want a mind-bending sci-fi movie with a dark atmosphere"* and receive matched results with customized **"Why this was recommended"** explanations.
   - **Option B (Multi-Criteria Studio)**: Filter by mood, genre, and narrative pacing.
   - **Option C ("Recommend Something Like This")**: Select any film (e.g. *Interstellar*, *Parasite*, *Blade Runner 2049*) to receive spiritually connected masterpieces.

4. **"What are you in the mood for?" (Mood-Based Discovery)**:
   - 12+ glowing interactive mood cards (Mind-Bending, Make Me Think, Adrenaline Surge, Make Me Cry, Romance, Dread & Terror, etc.).
   - Dynamic slide-out cinema drawer previewing tailored films.

5. **Artistic Genre Spectrum**:
   - 16 visual genre cards with movie count badges, high-res backdrops, and instant filtering.

6. **"You Probably Haven't Seen These" (Hidden Gems)**:
   - Celebrates films with outstanding critical consensus ($> 8.0$) but lower mainstream blockbusting (*Past Lives*, *Coherence*, *Aftersun*, *Incendies*, *Anatomy of a Fall*, *Memories of Murder*).

7. **International Cinema Universe**:
   - Dedicated hubs for South Korea (Hallyu), Japan (Anime & Kurosawa), India (Tollywood & Bollywood), France, and Spain.

8. **Deep Movie Detail Pages (`/movie/[id]`)**:
   - Full-bleed cinematic backdrops with vignette overlays.
   - Multi-source score cards (IMDb, Rotten Tomatoes, Metacritic, CBCA).
   - Visual sentiment analysis ratio bar (Positive / Neutral / Negative) with common praise and critical notes.
   - Cast gallery with character names, verified critic quotes, and streaming providers.

9. **Your Movie Universe (`/watchlist`)**:
   - Client-side storage for Watchlist, Watched history, Favorites, and 1–10 star ratings.
   - Dynamic **"Recommended for Your Universe"** computed in real time from your taste preferences.

10. **Side-by-Side Movie Comparison Matrix (`/compare`)**:
    - Direct head-to-head comparison of ratings, runtime, worldwide box office, sentiment, and themes.

11. **Instant Global Search Modal (`⌘K` / `Ctrl+K`)**:
    - Real-time autocomplete matching titles, directors, actors, genres, and keywords with keyboard navigation.

12. **Procedural Web Audio Haptics**:
    - Synthesizes subtle cinematic clicks, whooshes, and celebratory shimmers via Web Audio API without external audio assets. Master mute toggle included.

---

## 🛠️ Technology Stack

- **Framework**: Next.js 16 (App Router) + React 19
- **Language**: TypeScript
- **Styling**: Tailwind CSS 4 with custom cinematic glassmorphism and glows
- **Icons**: Lucide React
- **Audio**: Web Audio API Procedural Synthesizer
- **State**: Reactive LocalStorage Stores with cross-tab and event synchronization

---

## 🚀 Getting Started

### 1. Prerequisites
- Node.js 18+ or Node.js 24+
- npm 10+

### 2. Installation
```bash
# Navigate to project directory
cd cineverse

# Install dependencies
npm install --legacy-peer-deps
```

### 3. Environment Variables
Copy `.env.example` to `.env.local`:
```bash
cp .env.example .env.local
```

### 4. Running Locally
```bash
npm run dev
```
Open [http://localhost:3000](http://localhost:3000) in your browser.

### 5. Production Build
```bash
npm run build
npm run start
```

---

## 📊 Ranking Methodology (CBCA-v2)

To avoid fabricated critic scores, CineVerse employs empirical Bayesian weighted smoothing:

$$\text{Weighted Score} = \left(\frac{v}{v + m}\right) \times R + \left(\frac{m}{v + m}\right) \times C$$

Where:
- **$v$**: Number of verified user reviews
- **$m$**: Minimum review confidence threshold ($50,000$)
- **$R$**: Normalized blended score of critics ($45\%$) and audience ($55\%$)
- **$C$**: Global cinematic benchmark mean ($7.15$)

Attribution: Verified reviews aggregated from IMDb, Metacritic, and Rotten Tomatoes.
