# Pathy

Mentorship for first-generation students heading to Ontario universities.

## Tech Stack

- **Framework:** TanStack Start (React 19, TypeScript), Vite 7
- **Styling:** Tailwind CSS v4, shadcn/ui components
- **Backend:** Lovable Cloud (Postgres database, authentication, row-level security)
- **AI:** Lovable AI Gateway (language model for intent extraction and conversation starters, text embeddings for semantic matching)
- **Maps:** Leaflet
- **Testing:** Vitest

## Purpose and Mission

Many first-generation students don't have someone at home who has been through university applications. Pathy connects them with university students who have walked the same path.

**Mission:** to remove barriers to higher education by making meaningful mentorship accessible to every student, whatever connections they already have. AI helps students find the right people; it does not replace them.

## Key Features

- **Find a Mentor (SmartMatch):** students describe what they're looking for in their own words. A hybrid engine combines AI intent extraction, semantic similarity and weighted ranking (university, program, language, topics) to recommend the top three mentors. Each match explains why it was chosen and suggests conversation starters. Students can also browse mentors manually.
- **Home dashboard:** shows how many mentors you've connected with and your top mentor recommendations.
- **Explore:** an interactive map of Ontario's 23 universities. Pat the fox travels between the campuses you visit. Each campus has a photo gallery, a profile, what it's known for, standout programs and student mentor cards.
- **Passport:** a digital passport book. Answer a quick two-step check-in for a campus to earn its stamp in the university's colours.
- **My Applications:** add applications with only the programs each university offers, and get checklists tied to official deadlines.
- **Forum:** community posts, replies and votes.
- **Reminders:** upcoming deadlines in one place.
- **Accounts:** email and Google sign-in, with password recovery.
- **Accessibility (AODA / IASR aligned):** text resizing, light and dark mode, read-aloud and dictation, high contrast, easy-read font, reading guide, reduced motion, larger buttons and focus mode. Settings are saved to the user's account.

## Getting Started

```sh
npm install
npm run dev
```
