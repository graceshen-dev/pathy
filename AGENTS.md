<!-- LOVABLE:BEGIN -->
> [!IMPORTANT]
> This project is connected to [Lovable](https://lovable.dev). Avoid rewriting
> published git history — force pushing, or rebasing/amending/squashing commits
> that are already pushed — as it rewrites history on Lovable's side and the
> user will likely lose their project history.
>
> Commits you push to the connected branch sync back to Lovable and show up in
> the editor, so keep the branch in a working state.

## What Lovable manages

Rules outside this block are the project's own. Change the pieces below in
Lovable, not by hand. With the [Lovable MCP](https://mcp.lovable.dev)
connected, `send_message` asks Lovable to do it; otherwise ask the user to
use the editor.

- **Database.** Do not add or edit `supabase/migrations/` or `drizzle/`.
  Ask Lovable to change the schema.
- **Generated files.** Do not edit a file whose header says it is automatically
  generated.
- **AI gateway.** Keep model calls on Lovable's gateway, and keep
  `LOVABLE_API_KEY` out of browser code.
- **Connectors.** Lovable provides native connectors. `list_connectors` shows
  which are enabled; `add_connector` only returns the dashboard link. When a
  connector is enabled, calls go through the connector gateway and need
  `LOVABLE_API_KEY`. When Lovable does not provide one, users can bring their
  own key and store it in Secrets.
- **Secrets.** Lovable manages them. Do not put secret values in the repo.
<!-- LOVABLE:END -->

- Keep the desktop prototype screens as separate TanStack routes with a shared app shell; this preserves consistent navigation and independent page metadata.
- Prototype actions are frontend-only and must explicitly disclose disconnected messaging, translation, and mentor-booking services rather than report successful delivery.
- Read existing user journey rows through the authenticated browser client; scope local exploration preferences by user ID and never invent application progress.
- Lazy-load Leaflet behind ClientOnly; campus coordinates and markers are independent of visual reference images so map interactions remain geographic.

- Derive application checklists and passport mentor matches from authenticated application rows; keep device-only completion overrides separate from saved application progress.
- Combine saved passport entries with user-scoped quiz completion; require three correct campus answers for new stamps and keep map exploration history separate from earned stamps.
- The forum uses existing authenticated browser data policies for posts, replies, and votes; never seed fictional community activity.

- Keep personal targets and saved task dates separate from researched official deadlines; scope sourced deadlines by university, program, entry term and applicant category, and never extrapolate missing dates.
- Keep the Ontario campus catalogue as the shared source for map markers, campus resolution and quiz generation so new universities work throughout the journey.
- Centralize verified account state and the sole auth subscriber in the root AccountProvider; journey data reloads from that state to avoid competing listeners and cross-account state.
- Keep campus and existing prototype routes public; account forms use Cloud Auth and the existing signup profile trigger, while all private data access remains RLS-scoped.
- Keep university profiles and attributed campus photo galleries keyed to the shared campus catalogue; this keeps selected-school information consistent without changing journey data or map behaviour.
- Derive new-application program options and validation from verified university profiles; this prevents cross-university selections without changing existing saved applications.
- Keep fictional persona contacts on reserved example domains and display them as labelled non-sending text; this avoids routing users to real people or implying messaging is connected.
- Accessibility settings live in a root AccessibilityProvider that applies html classes; saved locally and, when signed in, to the user's own accessibility_preferences row so they follow the account.
- SmartMatch ranking (weights, filters) lives in src/lib/smart-match.ts and AI steps in smart-match.functions.ts; embeddings are computed per request over real mentor profiles plus labelled example students, so no stored vector table is needed until real mentors exist.
