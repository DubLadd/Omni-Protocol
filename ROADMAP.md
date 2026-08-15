

    Language(s): HTML5 + Vanilla JavaScript
    Framework / runtime: Browser-based (Three.js for 3D, Tailwind CSS for UI)
    Notable libraries: Three.js (3D visualization), Google Gemini API (LLM/image/audio), Fetch API (REST), localStorage (persistence)

Feature Upgrade Ideas

Here are concrete features to consider adding:
1. Data Export & Import System

    What: Currently you can download a vault snapshot, but add structured export to JSON/CSV with metadata
    Why: Users may want to migrate data, backup archives, or integrate with external tools
    Implementation: Extend downloadVaultSnapshot() to support multiple formats; add reverse parser for restore-from-file

2. Multi-File Batch Processing Pipeline

    What: Upload multiple files at once and process them in queue, with per-file audit trails
    Why: Single file uploads is limiting for real workflows; batch processing scales the platform
    How: Add file queue manager, progress tracking, and aggregated results dashboard

3. Ritual Technique Tree / Upgrade Persistence

    What: Make ritual upgrades more strategic — add branching skill trees or prestige system
    Why: Currently upgrades are linear multipliers; a skill tree adds long-term progression depth
    How: Restructure ritualMultipliers to track choices, enable unlock chains (e.g., "unlock Passive Yield only after achieving 5x base Density")

4. Real-Time Collaboration Layer

    What: Share vault sessions via URL/invite code; see real-time updates from collaborators
    Why: The system is single-user (localStorage only); multi-user opens creative potential
    How: Add Firebase Realtime DB or Supabase integration; sync vaultData across clients

5. Custom Agent Personas (User-Defined)

    What: Let users define their own agent personas with custom system prompts
    Why: Three pre-built agents limit expressiveness; custom personas unlock personal workflows
    Implementation: Add persona builder UI; store in localStorage; pass custom prompts to Gemini API

6. Memory Timeline Analytics Dashboard

    What: Add filtering, search, and data viz (charts, timelines) over the memory log
    Why: Currently memories are just a text list; analytics surface patterns in your vault lifecycle
    How: Parse timestamps; group by hour/day; add chart library (Chart.js); enable filtering by event type

7. Workflow / Automations

    What: Define triggers (e.g., "when C-Density > 0.5, auto-generate image") and actions
    Why: Users currently must manually invoke features; automation saves repetition
    Implementation: Simple rule engine (IF condition THEN action); store in vault state

8. API Integration Hooks

    What: Expose the vault state and operations via REST endpoints (Node.js backend)
    Why: Currently locked in the browser; backend integration enables mobile apps, discord bots, webhooks
    How: Spin up Express.js server; mirror localStorage logic to database; expose CRUD endpoints

9. Concept Map Visualization (Beyond 3D Points)

    What: Show relationships between inputs, craving targets, and synthesis outputs as an interconnected graph
    Why: Three.js visualization is abstract; a conceptual knowledge graph makes semantics visible
    Implementation: Use D3.js or Cytoscape.js; nodes = concepts/files; edges = relationships inferred from Gemini

10. Version Control for Vault Snapshots

    What: Like Git for your vault — track changes, branch snapshots, merge experiments
    Why: Users exploring creative directions may want to "branch" and compare outcomes
    How: Store snapshot history; add branch manager UI; implement basic 3-way merge for synthesis outputs

11. Voice Command Interface

    What: Accept voice input (Web Speech API) to trigger actions and upload files
    Why: Keyboard + mouse are limiting; voice makes the experience more hands-free and sci-fi
    Implementation: Web Speech API for input; voice feedback via TTS (already integrated)

12. Persistent User Profiles & Leaderboards

    What: Track user stats over time; optional community leaderboards (coins earned, inputs processed, etc.)
    Why: Gamification encourages repeated engagement
    How: Add backend DB (Supabase); track milestones; render ranked leader boards

Quick Wins (Easier Implementations)

    Dark mode toggle (add light theme alternative to neon aesthetics)
    Keyboard shortcuts cheat sheet (modal overlay with all hotkeys)
    Search within memories timeline (filter by keyword)
    Copy-to-clipboard buttons on all outputs (audit results, synthesis, oracle responses)
    Preset prompts dropdown for the Grounded Oracle (pre-fill common research queries)
    Session auto-save interval indicator (show last saved timestamp)

