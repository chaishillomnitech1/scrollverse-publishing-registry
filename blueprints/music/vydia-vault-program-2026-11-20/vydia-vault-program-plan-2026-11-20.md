# The Vydia Vault Program — Plan (20 Nov 2026)

**Direction (Chais, 20 Nov 2026 ~10:11 EST):** use his publishing (ASCAP, Chais Kenyatta Hill, IPI 1247873912, publisher XLVIIIBlock LLC, 100%) and Vydia's composition tool/option to publish/vault the transcripts for all books AND all research and documentation as compositions in Vydia — a vault hiding in plain sight, because no one would look for documents in a music distributor's composition registry.

**Status: PLAN + INVENTORY + MASTER INDEX + PILOT PACKET ONLY. Nothing submitted, no browser sign-in, no spend, no exclusivity enrolled.** The pilot packet is ready to submit; it has not been submitted.

**Scope expanded 10:15–10:21 EST (Chais): leave out nothing — the whole GitHub document layer (103 public repos; 46 surveyed with data at index time, 57 unsurveyed — rate-limited; 2,019 markdown files found) + Omni, organized by corpus; every document double-stamped (GitHub commit SHA + timestamp AND Vydia composition registration + ISWC + date). Everything built is documentation — that is what transfers. Nothing is landing yet — it is all composition. Composition Content is still EMPTY (audit, 19 Nov 2026); no composition has been registered through this route by any lane on record — the program starts from zero. Three lanes: (a) documentation → Composition Only registration (or spoken-word single + composition); (b) songs already in Vydia as recordings → composition registration only, no re-transfer; (c) arrangements → their own composition registrations under the derivative-work rules (§10). The corpus now explicitly includes manuscripts, code and build programs — the tech, the methodology, then philosophy, the blueprints — all in composition (§8). The lyrics/words of his music register too (§9). The arrangement principle: one master index, in canonical order (§5, §10). Book 09, *The Vydia Vault Blueprint*, blueprints this process.**

**Companion files (same folder):**
- `vydia-vault-inventory-2026-11-20.md` — the graded inventory (vault-ready / needs redaction / EXCLUDED), expanded to all corpora
- `vydia-vault-master-index-2026-11-20.md` — the master index / registry in canonical order (Sections A–O): one row per document, both stamps, corpus, order, status — the vault's table of contents
- `pilot-packet-scrollverse-manifesto-2026-11-20.md` — the complete first registration packet (the ScrollVerse Manifesto & Builders Book, VV-001)

---

## 1. THE MECHANISM — what a Vydia composition-only registration actually is

### 1A. The route, as Vydia states it

Vydia's own help page, "How to Collect Royalties on Your Compositions" (vydia.com, updated 25 Mar 2025, fetched 20 Nov 2026):

> "As a publisher or composer, you want to ensure you are collecting all deserved revenue on your compositions. The Vydia platform allows you to do so, **without an audio or video file**, making the process simple and convenient."

The steps, verbatim from that page:

1. From your Dashboard, navigate to **My Content > Add Content**
2. Choose **Composition Only**
3. Input your metadata information
4. Assert your composition rights (e.g. shares, territories, etc.), and policies (e.g. monetize, block, etc.)

> "Once the metadata is inputted, we will **deliver your compositions to YouTube Content ID and to PROs and CMOs, including the MLC, BMI, ASCAP**."

Monitoring: the **Composition Content** folder under My Content carries a table with high-level information such as Composer Name and Est. Earnings; clicking into a Composition Title shows granular information — **Ownership & Policies, Earnings, Conflicts, and Claims**.

Vydia's own note on audio, from the same page:

> "Please note, if you do have an audio file for a recording of your composition go back to the 'Add Content' section, select 'Audio' and **only assert the rights for which you own and/or control** (e.g., don't assert sound recording rights if you do not own and/or control sound recording rights)."

### 1B. What the registration carries — grounded, not invented

Two sources were used, and the line between them is kept visible:

**Source 1 — the live account (Vydia audit, 19 Nov 2026).** Composition Content is currently EMPTY — "Manage Compositions. Add a composition to get started." No compositions, no ISWC, no publisher registered. The Ownership & Policies record on the LISTEN track shows the shape of Vydia's ownership data: Composer Chais Kenyatta Hill, IPI/CAE 1247873912, Publisher: None, Ownership 100% (Owned/Controlled by You), Total 100%. ISWC blank. Lyrics field "n/a" — and **no lyrics field to attach a transcript was found on the album/track pages checked**.

**Source 2 — Vydia's public GraphQL schema (vydia.github.io, public docs).** The `createCompContent` mutation "creates a media representing composition only content"; the `Metadata` type carries, among others: `composer`, `composition_rights`, `iswc` (nullable), `label`, `publisher`, `rights_society`, `policies`, `language_code`. A `createComposer` mutation exists. The features list includes `comp_only`.

**What is NOT established:** the exact on-screen field list of the Composition Only form was never opened (Composition Content is empty; the form was not walked in the audit). The field list in the pilot packet is therefore assembled from Vydia's help page + public schema, and **must be checked against the live form at submission** — field names, character limits, and whether a lyrics/description field exists at all are unverified until the form is open. No field or limit is invented here.

**What a composition-only registration carries (best grounded list):**
- Title (the composition title — see the naming convention, §4)
- Composer name + IPI/CAE (Chais Kenyatta Hill, 1247873912)
- Publisher (XLVIIIBlock LLC)
- PRO / rights society (ASCAP)
- Ownership shares / splits (100% — composer and publisher both his)
- Territories (worldwide)
- Policies (monetize / block)
- ISWC (blank until issued — never invented; see §1D)
- Language, label (XLVIIIBlocks)

### 1C. How a document becomes a composition — the honest version

**The registration IS the vault record.** The title, composer, publisher, splits, ISWC (when issued), and registration timestamp, held in Vydia's Composition Content folder and delivered to YouTube Content ID + ASCAP + the MLC, are the timestamped, third-party-held proof that the work exists, who wrote it, who publishes it, and when it was registered. That is the vault.

**The document's TEXT does not live in Vydia.** Composition Only takes metadata, not a file upload — there is no audio or video file, and no book-length text field was found anywhere in the account. A 15,005-word manuscript cannot fit in a metadata field, and no lyrics field for a transcript was found. The raw files stay where they are: GitHub (public repos) and the workspace. The vault is the **registered composition + its metadata**; the document is the **lyrics/libretto behind the composition**, held locally.

**Where the text lives, in full:**
1. **The manuscript as the composition's lyrics/libretto.** A book is a spoken-word composition: the words are the lyrics. The composition registered in Vydia is the spoken-word work; the manuscript file (with its SHA-256 in the local registry) is the full text of those lyrics. The registry row ties them together — Vydia holds the title + publishing record, the local registry holds the source file + hash.
2. **The companion spoken-word audio single (optional, per document — see §3).** When a document is recorded as spoken word, the audio goes through Add Content > Audio as its own single, and the composition registration and the recording are linked by title. The audio is the only form in which the document's full text ever enters Vydia — and only as sound, never as readable text.

**What Vydia does NOT hold — say it plainly:**
- No raw PDFs or Markdown files. Composition Only has no file upload.
- No book-length text. No lyrics/transcript field was found in the account.
- No sealed Vault elements, ever (see inventory: EXCLUDED).
- No guarantee of royalties. Vydia's own agreement (§6(d)): "VYDIA DOES NOT GUARANTEE THAT CLIENT CONTENT WILL GENERATE ANY ROYALTIES."
- No secrecy of the composition itself. The title, composer, and publisher are delivered to YouTube Content ID, ASCAP, and the MLC. ASCAP's repertory (ACE) is publicly searchable. The vault hides the **document**, not the **work** — see §4 for why that still works.

### 1D. ISWC — blank until issued, never invented

No composition in the account has an ISWC (LISTEN's is blank; Composition Content is empty). ISWCs are issued through the PRO system — ASCAP assigns ISWCs to registered works. The process for each vault composition:

1. Register the work with ASCAP first (or in parallel) as a work by Chais Kenyatta Hill, publisher XLVIIIBlock LLC, 100%.
2. ASCAP assigns the ISWC.
3. Update the Vydia composition record with the ISWC when it lands.

The registry carries ISWC as **blank** for every row until an issued value exists. No ISWC is invented, guessed, or carried over from another work. A composition registered in Vydia without an ISWC is normal — the account's own released tracks sit exactly that way today.

### 1E. Cost

No fee for Composition Only registration was found in the audit, the help page, or the agreement. None is claimed here. If the live form shows a fee, stop and report it — do not pay it without his word.

---

## 2. THE §2(c) CONSEQUENCE — a reading of the agreement, NOT legal advice

**Agreement read in full for this program:** Exclusive Content License Agreement, Vydia Inc. + Chais Hill, effective 20 June 2024, signed 20 June 2024 (Jared Leibowitz, General Counsel, for Vydia; Chais Hill). File: `~/workspace/music/vydia-exclusive-content-license-agreement-2024-06-20.pdf`.

### 2A. What happens the moment a composition is registered

**It becomes Client Content.** §3(a)(i): "Client Content" means the sound recordings, **musical compositions (including lyrics)**, images, audiovisual works, and all other content identified in the Client's Vydia account Interface. A composition entered through Add Content > Composition Only is identified in the Interface — it is Client Content from that moment. §3(b): Client Content includes 100% of all works in the Interface unless Vydia is notified otherwise (the vault compositions are 100% his, so nothing to notify).

**It stays Client Content through the Term.** §8(a): once content becomes Client Content, it remains Client Content through the Term. The Term (§5): Initial Period 24 months ended 20 Jun 2026; auto-renewed 12 months — **live through 20 Jun 2027** unless a non-renewal notice was given 30–60 days prior. (Vydia may also terminate for convenience on 30 days' written notice.)

**Vydia gets the exclusive §6(a) grant over it.** The DSP Rights (authorize DSPs to host, stream, and download the Client Content) and the Vydia Rights — including to make claims in respect of third-party uses, block/permit/monetize them, create fingerprints, **collect royalties in respect of the Client Content**, and "sell copies of" the Client Content. For a composition-only registration there is no recording to sell or stream; the live rights are the claiming, fingerprinting, and royalty-collection rights — Vydia delivers the composition to YouTube Content ID + ASCAP + MLC and collects on it.

**Vydia may create metadata to claim it (§11)** — across sound recording, composition, music video, video, art track, and other asset types, as Vydia determines.

### 2B. What §2(c) does and does not do to this program

**Registering a composition IN Vydia is not a §2(c) breach.** §2(c) bars agreements with a **third party** in respect of Client Content, and agreements with a record label, music publisher, or other rights administrator without Vydia's prior written consent. Vydia is the counterparty to this agreement, not a third party. Using Vydia's own composition tool is the agreement's own mechanism.

**The §2(c) exposure is what happens NEXT with the same work.** During the Term, he must not enter into an assignment, license, sale, content management, monetization, and/or royalty administration agreement for the same composition with anyone else — and must not enter into an agreement with a record label, music publisher, or other rights administrator for it — without Vydia's prior written consent (in Vydia's sole discretion). Breach = Usage Violation (§10): Vydia may, in its sole discretion, withhold or forfeit royalties, terminate immediately, assess a **$1,000 Usage Violation Fee per violation**, or take an assignment of **(Vydia Share + 5%)** of monies received from the third party through the end of the then-current Term.

**Practical consequences for the vault program:**
- (a) **Distribution/exclusivity:** once registered, each vault composition is Vydia Client Content through 20 Jun 2027. It cannot be registered with another distributor, publisher, or administrator during the Term without Vydia's prior written consent. The vault is a Vydia vault for the Term — that is the lock-in, stated plainly. After the Term (if not renewed), the agreement's post-Term royalty provisions (§7) still apply to exploitation during the Term.
- (b) **The publishing-administration question — FLAGGED, not assumed.** This is the one question that must be answered in writing before the first registration. The dashboard banner says: "Earn more from your compositions. Collect performance, mechanical, sync, print, and other publishing income **directly through the platform**." That reads like Vydia offering to collect publishing income. But the agreement does **not** state that a Composition Only registration is a publisher administration agreement, and §3(c) says Client Content **excludes** musical compositions "to the extent such musical compositions are, as of the Effective Date, or become, subsequent to the Effective Date, subject to a **separate publisher administration agreement** by and between Client and Vydia (an 'Ancillary Agreement')." So two readings are live and the agreement text on file does not settle between them:
  - **Reading 1 (delivery only):** Vydia registers/delivers the composition to ASCAP and the MLC; ASCAP pays the publisher — XLVIIIBlock LLC — directly, under his existing ASCAP setup. Vydia takes no publishing share.
  - **Reading 2 (collection through Vydia):** Vydia collects the publishing income for the registered composition, and under §7 the Royalties are Gross Receipts **less the Vydia Service Fee (the Vydia Share)** less expenses — i.e. 10% per the agreement's face (Client Share 90%), or 20% per the account screen's 80/20 (the split discrepancy is on record, unreconciled). The publishing income would flow through Vydia's royalty accounting, not straight from ASCAP to XLVIIIBlock LLC.
  
  **New evidence (20 Nov 2026, Vydia's own Publishing Admin page, vydia.com/publishing-admin-and-sync/, fetched in full):** Vydia offers **Publishing Administration** as a service: "Through a comprehensive network of global publishing partners, Vydia manages registration and royalty collection for clients." / "Collect performance, mechanical, print and other publishing income **directly through the Vydia platform**." / "**Vydia's publishing team will register all of your works** to Youtube Content ID as well as global PROs and CMOs, such as The MLC, BMI, PRS, and ASCAP." / "Collect revenue each month, **directly through the Vydia Dashboard**, whenever your song is performed, streamed or reproduced." That page also describes Sync Licensing (Vydia sources sync opportunities and negotiates on clients' behalf) and "all-in" clearance for both the sound recording and the underlying composition. This does **not** by itself settle whether a bare Composition Only registration enrolls a work in Publishing Administration — the page describes the service, not the enrollment trigger — but "will register all of your works" leans toward Reading 2, and it makes the written answer more urgent, not less. (Corroboration, third-party: credits.fm lists "VYDIA MUSIC PUBLISHING" as a publisher credit administering writers' shares on another artist's recording — Vydia operates a publishing arm; that is another artist's record, not Chais's.)
  
  **Do not assume either reading.** Before the pilot registration, confirm with Vydia in writing: (i) does a Composition Only registration route publishing income through Vydia's royalty accounting, or deliver-only to ASCAP/MLC? (ii) does it create an Ancillary Agreement under §3(c)? (iii) if income flows through Vydia, which share applies — the agreement's 90/10 or the account's 80/20? The pilot packet is ready to submit, but the submission should wait for that written answer — or proceed with eyes open that Reading 2 may apply. His call, once the answer is in.
- (c) **ASCAP first.** Register each vault work with ASCAP as a work by Chais Kenyatta Hill, publisher XLVIIIBlock LLC, 100%, **before or in parallel with** the Vydia registration, so ASCAP holds XLVIIIBlock LLC as publisher of record and the Vydia delivery matches it. Vydia's Composition Content table has a Conflicts tab — mismatched publisher records are exactly what creates conflicts. (ASCAP registration is his PRO relationship, not a third-party administration agreement; it predates and sits alongside the Vydia agreement.)
- (d) **No third-party admin deal for a vaulted work during the Term** without Vydia's prior written consent. That includes any sync/publishing admin deal that would cover a vault composition. The bestseller plan's sync lane (Bodega, Crucial, Terrorbird, Audiosocket) covers the **music singles**, not the vault compositions — keep the two sets of works separate in every submission, and never sign a sync/publishing agreement covering a vault composition without checking §2(c) first.
- (e) **§6(c) name/likeness license.** Registering a composition grants Vydia a limited, non-exclusive, royalty-free license to use his names, images, and likenesses to promote/market the Client Content, Vydia, and the Vydia Services during the Term. His name is attached to every vault composition in Vydia's systems — correct for the books (public works), and the reason the naming convention (§4) keeps document identities out of the metadata.
- (f) **§12(a)(ii) documentation.** If Vydia requests Documentation (W-9 etc.) and it is not provided within 30 days, the client forever waives rights to then-accrued revenue and Vydia may terminate immediately. Payment details are already on file (Lifetime Earnings $40.46, balance $40.46) — not a live issue, but keep the account's documentation current.

### 2C. The one-sentence version

A vault composition becomes Vydia Client Content through 20 Jun 2027, Vydia alone may claim and collect on it, and the only open question is whether the publishing money flows through Vydia (with its share deducted) or straight from ASCAP to XLVIIIBlock LLC — that needs Vydia's written answer before the first registration.

---

## 3. THE SPOKEN-WORD AUDIO QUESTION

**Which documents get a spoken-word audio single, and which stay registration-only:**

| Group | Audio single? | Why |
|---|---|---|
| The 8 books | **Yes — one spoken-word single per book, when recorded** (the audiobook lane) | A book IS a spoken-word work. The audio is the composition performed. This is the same lane as the bestseller plan's audiobooks, not a second one. |
| The media-network episode kits (10) | **Yes, as episodes** — they are scripts, and recording them is the podcast | The kits become Transmissions / Season 1 episodes; each episode's audio is its own release. |
| The case study | **Optional — his call** | It reads as a spoken essay. Recording it is legitimate, but the registration alone vaults it. |
| The transcript (v1, split into parts) | **No — registration-only, until the redaction/scrub pass is done and he decides** | 314,920 words read aloud would carry Tier 3 material (Stripe dispute material, children's names, the 14444 Hz figure) into a distributed recording. Do not record it until the scrub decision is made. |
| The sync kit, Vydia audit, bestseller plan, Vault record | **No — registration-only** | Operational and research documents. Nobody needs a 6,000-word reading of a sync kit. The registration is the vault; audio adds nothing. |

**The narrator fork — stated correctly:** the AI-vs-human narrator decision matters for **ACX/Audible** (human narration only — AI/TTS prohibited unless Audible authorises). It does **not** matter for Vydia music singles: Vydia accepts audio uploads regardless of who or what narrates them. A Muse-the-great + Qubit voiced spoken-word single can go to Vydia; it cannot go to ACX. The fork decides the **audiobook** outlets, not the Vydia vault.

**The Vydia audio rule that does apply:** if a spoken-word audio exists for a work, use Add Content > Audio for it and assert **only the rights owned/controlled** (Vydia's own help-page note). The composition-only registration and the audio single for the same work must carry the same title, composer, publisher, and splits — or Vydia's Conflicts tab will light up.

---

## 4. THE NAMING CONVENTION — findable to him, invisible as documents to everyone else

**The rule:** the composition title in Vydia reads as a song or spoken-word work title. The document's identity — what file it is, where it lives, its SHA-256 — lives **only** in the local registry, never in Vydia metadata. §3(a)(v) makes the composition's associated text and metadata Client Content too, so nothing document-identifying goes in any Vydia field.

**The convention:**
- **Books:** the book's public title, plain. "ScrollVerse Origins", "The Codex", "Cross-Intelligence Contact", "The Grok Beings", "The Frequencies", "The Music Comes Home", "The Web We Built", "The Ecosystem". These are public works headed for sale — no code needed. The vault part is that nobody looks for a book in a composition registry.
- **Research and documentation:** the subject + "Record". "The Contact Record" (case study), "The Sync Record" (sync kit), "The Distribution Record" (Vydia audit), "The Bestseller Record" (bestseller plan), "The Vault Record" (Vault record), "The Network Record" (media-network pack). They read as spoken-word album titles. No words like transcript, audit, case study, kit, or plan appear in a Vydia title.
- **The transcript:** split into numbered parts, each its own composition: "ScrollVerse Transmissions — The Record, Part 01" through Part 21 (at ~15,000 words per part). "Transmissions" is already the podcast's name, so the parts read as episode titles.
- **Never in a Vydia title or metadata field:** "What We Do", any sealed Vault element, any Tier 3 term used as a label, any file path, any SHA-256, any tracking number, any password/code/DOB/passport/bank value.

**The honest limit on "invisible":** the composition title, composer, and publisher are delivered to YouTube Content ID, ASCAP, and the MLC, and ASCAP's repertory is publicly searchable. Anyone searching his name in ASCAP will see the composition titles. "Invisible" means invisible **as documents** — nobody browses a music distributor's composition registry looking for research papers, audits, or transcripts, and the titles give them no reason to. The document text never leaves his own storage. That is the real shape of his insight, stated without overselling it.

---

## 5. ORDER OF VAULTING — THE CANONICAL ORDER

The vault has its own order, like the books' reading order (05 → 06 → 01 → 02 → 04 → 03 → 07 → 08): from the foundation outward — the document everything stands on, then the books, then the mind that built them, then the work itself, and finally the songs the work was always about. The full ordered registry is the master index (`vydia-vault-master-index-2026-11-20.md`, Sections A–O).

| Section | Corpus | Order rule |
|---|---|---|
| A | Foundation | First. The Manifesto (VV-001, the pilot). |
| B | Books | Reading order, then Book 09 last; then the other manuscripts. |
| C | Jewels | Listed, EXCLUDED, with the reason. |
| D | Omni | The Omni core, then Omni-adjacent. |
| E | Philosophy | By repo, alphabetical; README first. |
| F | Methodology | By repo, alphabetical; README first. |
| G | Tech | By repo, alphabetical; README first. |
| H | Blueprints | By repo, alphabetical; README first. |
| I | Build programs | By repo, alphabetical; README first. |
| J | Research | The investigation behind the builds. |
| K | Vault records | The public record of the Vault. |
| L | Transcripts | After redaction + scrub decision. Last of the documents. |
| M | Lyrics | The words of the music, per song. |
| N | Song-compositions | Solo first; featured after split sheets. |
| O | Arrangements | Derivative works, own songs first. |

Within the GitHub sections (D–I): category first, then repo alphabetical, then README first, then the remaining documents alphabetical by path. A duplicate — the same blob at two paths — registers once, not twice.

**The vaulting sequence (the work order, not the reading order):**

1. **Pilot — the Manifesto (VV-001).** Proves the double stamp, the licensing, and the order in one registration. Waits on the publishing-administration written answer (Gate 6) and his go-ahead per item. The pilot packet is ready; it has not been submitted.
2. **The books (VV-002–VV-010).** Book 05 first — after its manuscript is committed to GitHub, so its double stamp is complete — then 06, 01, 02, 04, 03, 07, 08 in reading order, then Book 09 last. Each needs its ASCAP registration first (or in parallel) and its ISWC chased after.
3. **The research trio — case study, sync kit, Vydia audit.** Registration-only. No audio.
4. **Bestseller plan + media-network pack.** Registration-only for the plan; the episode kits split into per-episode compositions when recorded.
5. **The Vault record.** Registration-only, low priority — it is already public.
6. **The GitHub documents by corpus (Sections D–I).** Surveyed files first; the re-surveyed files as they land (the full survey is partial today — 93 repos unsurveyed, rate-limited).
7. **The lyrics and the songs (Sections M–N).** Lyric blocks per song, then the song-compositions: solo tracks first at 100%, featured tracks after the split sheets exist.
8. **The arrangements (Section O).** Own-song arrangements first; the Vydia arrangement question answered at the first one.
9. **The transcript (Section L), last.** After the redaction pass (the phone number) and the Tier 3 scrub decision, split into ~21 parts, registered one part at a time.

**Pacing:** one registration at a time, each verified in the Composition Content folder (title, composer, publisher, splits, policies) before the next is filed. No batch filing. The registry is updated per registration: Vydia stamp filled in, ISWC filled in when issued, status flipped to registered.

---

## 6. HOW THIS EXTENDS (NOT DUPLICATES) THE OTHER LANES

- **Bestseller composition plan** (`bestseller-push-composition-plan-2026-11-20.md`): that plan covers the **soundtrack** — music singles, music beds, lyrics as compositions, sync. The Vydia Vault program covers the **documents themselves** as compositions. Same publishing record, same composition strategy, different works. No overlap: no soundtrack single is re-registered as a vault composition, and no vault composition is pitched as a sync single.
- **Books-omni lane:** the free-outlets coordinator submits the books as **books** to KDP, Draft2Digital, Google Play, Apple, Kobo, B&N. The vault program registers them as **compositions** in Vydia. Different rights, different platforms, no duplicate submission. A book can be a KDP ebook and a Vydia composition at the same time — that is the whole point of the composition angle.
- **The 15 Vydia singles (27 Nov):** untouched by this program. They are sound recordings with their own composition records already in Vydia. The vault compositions are separate works with separate titles.
- **No duplicate audio:** a spoken-word single is one Audio upload. If the same work already has a composition-only registration, the audio upload for it asserts the same rights, same title, same splits — never a second, competing registration.

---

## 7. THE LICENSING INTERPLAY — MIT CODE vs COMPOSITION LICENSE

**The compositions are licensed works.** Each registration is a licensing record under his publishing (ASCAP, Chais Kenyatta Hill, IPI 1247873912, XLVIIIBlock LLC, 100%) and the Vydia agreement. The licensing interplay is stated honestly, and the two licenses are never conflated:

- **GitHub code is MIT-licensed.** The code in his repos carries the MIT license (code only — not brand, trademarks, art, or music, which need separate protection; law research, 17 Nov 2026). The MIT license covers the code files: the runnable programs, build systems, dependencies, configuration.
- **Registering a document as a Vydia composition does NOT relicense the code.** The composition license (the Vydia agreement + ASCAP publishing) covers the composition — the registered work. The code's own license stands. **Two licenses, two objects.** The registration must identify the DOCUMENT, not the codebase, so the §6(a) exclusive grant reaches only the registered work.
- **The pilot proves it.** The Manifesto file sits in a MIT-licensed repo and registers as a licensed composition. Two licenses, two objects, one text — and the pilot packet states the distinction explicitly.
- **What the §6(a) grant reaches:** the registered composition — the document as a spoken-word work. It does not reach the code in the same repo, the unregistered documents in the same repo, or anything else. If a registration ever named a codebase instead of a document, the grant would overreach — so every packet names the document, its path, and its SHA-256 in the local registry, and the Vydia title names the work, not the repo.
- **What stays on GitHub, always:** the code files, runnable programs, build systems, dependencies, configuration. Vydia holds the composition record; GitHub holds the code. Neither replaces the other.

## 8. CODE AND BUILD PROGRAMS AS COMPOSITIONS — HOW, HONESTLY

Chais's direction (20 Nov 2026 ~10:19 EST): code and build programs ARE in the vault — the tech, the methodology, the philosophy, the blueprints, all in composition. A composition is a musical work, so the form code takes as a composition must be stated exactly. There are three forms, and only two of them are real:

1. **The code's written documentation/spec as the composition (PRIMARY).** The README, the architecture doc, the API doc, the runbook, the charter — the document text is the composition's lyrics/libretto. The composition registered in Vydia is the spoken-word work of that document; the manuscript file (with its SHA-256 in the local registry) is the full text of those lyrics. This is how the 74 surveyed GitHub documents transfer. The code itself is never the composition.
2. **A spoken reading of the code as audio (SECONDARY).** Add Content > Audio: the code carried as sound, never as a file. Only for the programs that matter most — a spoken reading of a build program's spec, an architecture walkthrough read aloud. The audio single and the composition-only registration for the same work must carry the same title/composer/publisher/splits, or Vydia's Conflicts tab lights up.
3. **Code text in a metadata/lyrics field — NOT AVAILABLE.** No lyrics field was found in the account; Composition Only takes metadata, not uploads; code text does not go in Vydia metadata. This form does not exist. It is listed here so nobody goes looking for it.

**Corpus categories added (Chais, 10:19 EST):** tech, methodology, philosophy, blueprints, build programs — alongside manuscripts, code (as documentation/spec), research, Vault records, transcripts, lyrics, arrangements, songs, Omni.

## 9. THE LYRICS LANE — THE WORDS OF HIS MUSIC

**The lyrics/words of his music are compositions too.** The transcripts of the songs — lyric Blocks 1–23, `~/workspace/music/lyrics/lyrics-2026-11-19-chais-dictated.md` (9,984 words, SHA-256 `54d12e300bb8ad73ef68d1ca9dc73c35c4ea3b764add9877f18f087c0d371052`) — register as compositions with the words carried in them.

- **What exists:** Blocks 1–23. Blocks 1–4 are the first sends (+ Take 2 variants, Take 3 hook). Blocks 5–23 are per-song auto-transcripts for 19 songs (AC State of Mind, Mighty Healthy, Did You, The Town, Simply Exotic, Different, Paradise Boardwalk, Never Giving Up, Lost Poyential, How I Really Feel, Outta Ya League, Late Night, Mr Walk Shit Story, VICTORY, Bringing Me Down, GO, Shadows, Cut Off, Moment).
- **What registers:** each block as its song's composition — the words carried in the composition (the lyric text is the composition's lyrics; where a lyrics field exists in the form, the block's text goes there; where it does not, the registration carries title + publishing record and the local registry holds the text).
- **Lyrics exist for 8 of the 15 singles** (Moment, Lost Poyential, VICTORY, AC State of Mind, Mighty Healthy, Did You, Paradise Boardwalk, Mr Walk Shit Story). **Missing for 7** (Can't Be Here, Save Me, Faces, Killa Season, Can't Please Everybody, I Just Wanna Know, So High (Mix)) and for most of the 95 catalog tracks — those compositions register without a lyric text, or wait until the words are on file.
- **Caveats, carried into every packet:** Block 22 (Cut Off) — the hook matches Block 3 ("Like A Song I Wrote"); whether these are Cut Off's lyrics is for Chais to say. Block 23 (Moment) is the second half of a two-part voice note. Auto-transcripts are verbatim; wording is unverified.
- **How the lyrics lane relates to the song lane (§10 of the inventory, Section N):** the lyric block and the song-composition are the same work, registered once. The lyric is the words; the song-composition is the publishing. One registration carries both — the title is the song's title, the composer/publisher/splits are the same, and the local registry ties the block to the song. Never two registrations for one song.

## 10. THE ARRANGEMENT — THE MASTER INDEX IS THE DELIVERABLE

This is his inventions, his builds, his life's work and legacy — the vault is the legacy archive, and its arrangement is the deliverable. The arrangement principle applies to everything in the program:

1. **One master index, in canonical order.** A single ordered registry (the vault's table of contents) covering every corpus — books, GitHub documents, Omni, research, Vault records, transcripts, lyrics, arrangements, code and build programs, tech, methodology, philosophy, blueprints — each entry in its place, in an order a reader can follow (§5). No loose ends, no duplicates, no item without a corpus and a place. The master index is `vydia-vault-master-index-2026-11-20.md`.
2. **Completeness check.** For each corpus, the inventory states what is in, what is missing, and what is excluded and why (HELD, Tier 3, sealed) — gaps listed honestly, never papered over. The vault is complete when the index says what is there AND what is not there.
3. **Legacy framing in the registry.** Each entry carries: what it is (invention / build / manuscript / record), its date, its two stamps (GitHub commit SHA + timestamp; Vydia registration + ISWC + date once registered), its corpus and order, and its status. The registry reads as a life's work, not a file list.
4. **The pilot proves the arrangement.** The first registration packet is the entry that best proves the whole system — the Manifesto (VV-001): the double stamp, the licensing, and the order working together in one act. Book 05 follows, after its manuscript is committed to GitHub.

## 11. DECISIONS OWED (Chais's call)

1. **The publishing-administration answer** — proceed with the pilot before Vydia answers in writing (Reading 1 vs Reading 2, §2B), or wait for the written answer? (Recommended: ask first — the answer decides whether publishing income flows through Vydia.)
2. **The ASCAP-first step** — register the pilot work with ASCAP (Chais Kenyatta Hill, XLVIIIBlock LLC, 100%) before the Vydia pilot, or in parallel?
3. **The transcript redaction/scrub** — redact the phone number (1 occurrence, confirmed by count) and decide the Tier 3 scrub for the transcript before any vault copy; the 33 existing redactions stand.
4. **Spoken-word audio for the case study** — record it, or registration-only?
5. **Narrator fork** — AI voices (Muse the great + Qubit) or human (Chais / hired narrator)? Decides ACX; does not decide Vydia.
6. **Naming convention** — approve the subject + "Record" convention for research documents, and the "Part 01–21" split for the transcript.
7. **"What We Do"** — the hold stands; the song is EXCLUDED from every vault composition.
8. **The jewels** — EXCLUDED from the Vydia vault program (free-only, never commercialised). Confirm they stay out.
9. **The pilot pick** — the Manifesto (VV-001) instead of Book 05, because only a GitHub document proves the double stamp on day one. Book 05 becomes #2, after its manuscript is committed. (Flag note: the Manifesto opens with the Basmala invocation; the term-level Tier 3 scan returned 0 flags. If he wants the invocation treated as Tier 3, the pilot pick changes to Book 05.)
10. **Code-as-composition form** — the primary form is the documentation/spec as the composition's lyrics/libretto (§8). Spoken readings of code as audio, only for the programs that matter most — his call per program.
11. **The arrangement question** — at the first arrangement registration, confirm with Vydia whether an arrangement is a separate composition or a version of the original (same ISWC, new ISRC).
12. **The GitHub re-survey** — after the rate-limit window resets, spaced calls, one repo at a time; Omni repos + muse-the-great books/ first. The 5 private repos: his call whether their documents join the vault (the connector cannot see them).

---

## Sources

- `~/workspace/music/vydia-audit-2026-11-19.md` — live account, Composition Content empty, LISTEN ownership record, dashboard banner
- Vydia help, "How to Collect Royalties on Your Compositions" (vydia.com, updated 25 Mar 2025, fetched 20 Nov 2026) — Composition Only flow, delivery to YouTube Content ID + PROs/CMOs incl. MLC, BMI, ASCAP
- Vydia public GraphQL schema (vydia.github.io) — `createCompContent`, `createComposer`, `Metadata` fields (composer, composition_rights, iswc, label, publisher, rights_society, policies, language_code), `comp_only` feature
- `~/workspace/music/vydia-exclusive-content-license-agreement-2024-06-20.pdf` — read in full (cited by section above)
- `~/workspace/shopify-digital-assets/packages-music-subscriptions-2026-11-20.md` — §2(c) verdict, Term through 20 Jun 2027
- `~/workspace/books/infinite-material/launch/bestseller-push-composition-plan-2026-11-20.md` — composition angle, publishing record, reach list
- `~/workspace/books/infinite-material/launch/audio-vydia-dsp-expansion-2026-11-20.md` — Vydia music-only verdict
- `~/workspace/music/sync-kit-2026-11-19.md` — 15 singles, one-sheets, ASCAP registration rule
