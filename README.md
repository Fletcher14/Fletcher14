## Emmanuel Fletcher (Manny)

Paramedic. I build the software I wish the job had.

Three years of watching clinical information fail to travel — between the dispatch system and the
ambulance, between the ambulance and the hospital, between the hospital and the next crew —
turned into a fairly specific interest in why health systems that should talk to each other
don't.

Everything below is built around that one question.

---

### Health data continuity

Three systems that should exchange information and largely don't. Each project is one
link in the chain.

**1 · The handoff — [epic-done-right](https://github.com/Fletcher14/epic-done-right)**
An EMS-to-hospital bridge in FHIR R4. Allergies, safety flags and medications move from
a pre-hospital record into a chart, with SMART on FHIR backend-services auth and a return
path for the completed report. Tested against a real HAPI server, not just its own mock —
which is where the interesting bugs came from.

**2 · The identity problem — [continuity-layer](https://github.com/Fletcher14/continuity-layer)**
Many sources in, one patient record out, and nothing merged. A miniature master patient
index: two systems sharing no identifiers, no schema and no date format, resolved into one
canonical record with per-fact provenance — while anything unconfirmable goes to a review
queue instead of being guessed at.

A false merge writes one person's allergies into another person's chart and cannot be
undone. Every rule in it is biased by that.

**3 · The return path — [patient-lookup-portal](https://github.com/Fletcher14/patient-lookup-portal)** · *in progress*
The direction that barely exists in practice: hospital outcome data back to the clinician
who ran the call. You work a stroke, you do everything right, and you never find out
whether they got tPA. Commercial products serve the *agency* — quality improvement,
registry submission. Almost nothing serves the medic.

A lookup portal where a paramedic sees the outcome of their own calls, and only their own.
Scoped before any code, and the access rules are built and tested first: who counts as being
on the call, which hospital visit belongs to it, and which diagnoses are never shown.

---

### How I work

**[IDL-FSD](https://github.com/Fletcher14/IDL-FSD)** — a running investigation log from an
autonomous-driving perception project. Documentation only; the simulator itself is
proprietary. Chapter titles include *"the fix that wasn't, and the limit it exposed"* and
*"the forward-detection blind spot"*, which is a fair summary of what the log is for. If
you want to know how I debug rather than what I've shipped, read that one.

**[homelab](https://github.com/Fletcher14/homelab)** — a single box running 28 containers
that backs itself up, watches itself, and tells me when it breaks. Written up as decisions
and failures rather than a configuration dump — including the honeypot that had never
caught anything and was paging me daily regardless.

---

### Not public

**FirstResponse** — EMS routing built by someone who has driven the routes.
**CVFR-P** — a computer-vision project.

Both are proprietary and stay that way. Happy to talk through either.

---

### Currently

Working toward a move into health IT. Studying for RHCSA. Reachable at the address on my
profile.

*Some of this was built with heavy use of AI tooling. I can walk you through any line of
it, including the parts where I had to argue with it.*
