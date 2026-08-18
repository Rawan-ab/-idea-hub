# Social Save Library — Roadmap

## Phase 1 — Product Definition
- Define supported share sources for MVP.
- Define categories and item status model.
- Define metadata fields: URL, source, title, description, thumbnail, created date, category, favorite, seen/done, archived.
- Define Inbox behavior and manual reclassification.
- Create screen inventory and navigation.

**Deliverable:** Product brief + data model + MVP scope.

## Phase 2 — UX/UI
- Design onboarding/login.
- Design Home / Inbox.
- Design Collections / Categories.
- Design Saved Item card and detail view.
- Design search, filters, favorites, archive.
- Design Share-to-App confirmation sheet.
- Design empty/error/loading states.

**Deliverable:** Clickable Figma prototype.

## Phase 3 — Flutter Foundation
- Create Flutter project.
- Set architecture and theme.
- Build navigation and reusable cards.
- Connect Supabase.
- Add authentication and user profile.

**Deliverable:** App shell + login + local save flow.

## Phase 4 — Share Intake
- Android Share Intent.
- iOS Share Extension.
- Receive URL from external apps.
- Normalize URLs and detect source platform.
- Save raw link even if metadata extraction fails.

**Deliverable:** Share → app → saved item works reliably.

## Phase 5 — Metadata & Backend
- Create FastAPI service.
- Fetch safe metadata such as title, Open Graph image, description and hostname where available.
- Add fallback behavior for restricted social platforms.
- Store metadata in Supabase/PostgreSQL.

**Deliverable:** Saved cards contain useful preview data when available.

## Phase 6 — Organization
- Auto category rules based on hostname, title and metadata.
- Inbox for uncertain items.
- Manual category change.
- Search and filters.
- Favorites, Seen/Done, Archive and Delete.

**Deliverable:** Complete usable organizer.

## Phase 7 — Platform Testing
- Test TikTok links.
- Test Instagram links.
- Test X links.
- Test YouTube, websites, Google Maps and shopping links.
- Handle duplicate URLs and broken/deleted content.

**Deliverable:** Stable beta.

## Phase 8 — Later Enhancements
- AI classification.
- Natural-language search.
- Custom Collections.
- Similar-item suggestions.
- Smart duplicate detection.
- Deeper official API integrations where platforms permit.

## MVP Priority
P0: Share intake, raw link storage, Inbox, categories, search, open original link.
P1: Metadata previews, Favorites, Seen/Done, Archive.
P2: AI classification, natural search, advanced Collections.
