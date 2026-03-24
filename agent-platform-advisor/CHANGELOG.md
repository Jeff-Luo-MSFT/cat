# Changelog

All notable changes to the Agent Platform Advisor are documented here.

## [Unreleased] — apa-v2 branch

### Added
- **Implementation Guide** (step 5 of wizard) — per-platform pre-development and post-development checklists loaded from `apa.yaml`
- **Agent Structure Planning** (step 4 of wizard) — interactive component cards with checkboxes and notes fields; structure data defined in `apa.yaml`
- SVG icon system using Lucide stroke icons (`getIcon()` helper); replaces all emoji icons in structure data
- `structures` and `implementation` sections in `apa.yaml` for all four platforms
- Platform-specific structure titles rendered dynamically from YAML

### Changed
- "AI Foundry" renamed to "Microsoft Foundry" throughout
- M365 Copilot excluded from custom agent path recommendations (prescreen fast-track now routes correctly)
- Progress bar updated to 5 steps: Welcome → Assessment → Recommendation → Structure → Implementation

### Fixed (design review)
- `.center` changed from `display:block` to `display:flex` — button `gap` spacing now renders correctly (FINDING-001)
- Progress bar gained `flex-wrap:wrap` to prevent overflow on mobile viewports (FINDING-002)
- Implementation checklist `list-style:disc` removed — eliminates double bullets when checkboxes are present (FINDING-003)
- Structure and Implementation section titles reduced from 48px to 28px to match app hierarchy (FINDING-004)
- Added `:focus-visible` keyboard focus rings to `.btn` and `.option-card` (FINDING-005)
- Textarea placeholder text shortened (FINDING-006)
- Welcome screen sparkle icon replaced with Fluent SVG; robot emoji removed (FINDING-007)
- CSS variable system rebuilt and aligned with DESIGN.md tokens (FINDING-001–006, prior review)

---

## v1 — Initial Release (March 2026)

- YAML-driven 8-question assessment with weighted scoring engine
- Hard rules and tiebreaker logic for platform selection
- Recommendation screen with primary/secondary platform cards, fit badges, and key factors
- Pre-screen fast-track for M365 Copilot built-in experiences
- Refactored to external `assets/apa.css` and `assets/apa.js`
- OG meta tags, Clarity analytics, favicon
