# Shared Space App — Roadmap

**Deadline:** Working gift build by 20 December 2026. Final buffer until 31 December 2026.

## Phase 1 — Product Definition | 18 Aug–31 Aug
- Finalize temporary app name and private-space concept.
- Define the two-person user flow: Sign up → Create Space → Invite → Join.
- Lock MVP scope and move non-essential features to Later.
- Define content types and statuses.
- Create screen inventory and navigation.
- Decide visual system from saved references.

**Deliverable:** Product brief + MVP feature list + screen map.

## Phase 2 — UX/UI | 1 Sep–20 Sep
- Design Splash, Login, Create/Join Space, Invite.
- Design Home with For You and shared categories.
- Design Photos, Note Card composer, Our Notes.
- Design Restaurants list/detail/rating.
- Design Movies & Series list/detail/rating.
- Design Memories timeline.
- Design Share-to-App save sheet.
- Create reusable components: cards, chips, buttons, bottom nav, empty states.

**Deliverable:** Complete clickable Figma prototype for MVP.

## Phase 3 — Flutter Foundation | 21 Sep–5 Oct
- Install Flutter and configure VS Code.
- Create GitHub Flutter project.
- Set folder architecture and theme tokens.
- Build navigation shell and reusable UI components.
- Connect Firebase project.
- Add Authentication.

**Deliverable:** App launches, login works, navigation works.

## Phase 4 — Shared Space & Data | 6 Oct–20 Oct
- Firestore users and spaces collections.
- Create Space and invite code/link.
- Join Space flow.
- Member permissions restricted to the two invited users.
- Activity feed data model.
- Real-time sync between two accounts.

**Deliverable:** Two real accounts can share one private space.

## Phase 5 — Core Content | 21 Oct–10 Nov
- Photos upload and gallery.
- Notes/Messages cards and reactions.
- Open Later date lock.
- Restaurants + status + ratings.
- Movies/Series + status + ratings.
- Memories timeline based on completed items.

**Deliverable:** Main gift experience is usable end-to-end.

## Phase 6 — Share Links | 11 Nov–22 Nov
- Android Share Intent.
- iOS Share Extension.
- Receive shared URL into app.
- Extract URL metadata where possible.
- Classify into Restaurant / Music / Movie / Wishlist / Saved Link.
- Manual category fallback.
- Notify the second person after save.

**Deliverable:** Share → App → saved card works.

## Phase 7 — Notifications & Polish | 23 Nov–6 Dec
- Firebase Cloud Messaging.
- New content notifications.
- Open Later notifications.
- Empty/loading/error states.
- Animations and haptics.
- Image compression and upload reliability.

**Deliverable:** Stable beta build.

## Phase 8 — Gift Experience | 7 Dec–20 Dec
- Final app name and icon.
- Personalized welcome card.
- Seed first photos, messages, restaurants or memories.
- Final typography and visual polish.
- Test on both actual phones.
- Fix critical bugs.

**Deliverable:** Gift-ready version by 20 Dec.

## Buffer | 21 Dec–31 Dec
Only bug fixes, backup, install/distribution, and final content. No major new features.

## MVP Priority
P0: Auth, private Space, invite, Home, Photos, Notes, Restaurants, Movies, Memories, notifications.
P1: Share Links, Open Later, reactions.
P2: Music, Clothes/Wishlist, audio notes, advanced animations.
