# Pitch Notes — Smart Demand Signals

**Total target time: 5 minutes** (3-min talk + 2-min demo, or as fits the slot).

Use these notes per slide. The lines marked **🎤 Say** are word-for-word talk track; the lines marked **🕒 Time / 👀 Show** are stage cues.

---

## Slide 1 — Cover

**🕒 Time:** 10 seconds.
**👀 Show:** Stand still, the title speaks for you.

**🎤 Say:**
> "Smart Demand Signals. Daily commercial alerts for Inibsa's six thousand dental clinics. I'm [name], from team [name]."

(Move to slide 2.)

---

## Slide 2 — The problem

**🕒 Time:** 30 seconds.
**👀 Show:** Point at the quote when you read it.

**🎤 Say:**
> "Inibsa sells dental supplies to roughly six thousand clinics across Spain. Every morning, the sales team faces the same question: *which clinics should we contact today, and why?*"

> "Today, that decision is mostly intuition plus scattered KPIs. Five years of sales history are sitting in spreadsheets — *unused*. We turn those five years into a daily ranked call list."

(Move to slide 3.)

---

## Slide 3 — Two products, two brains

**🕒 Time:** 30 seconds.
**👀 Show:** Point at the **left card** then the **right card**.

**🎤 Say:**
> "The brief is very explicit on this point: commodities and technical products need different logic — and we agreed."

> "**Commodities** — anaesthesia, biosecurity. Recurring purchases. We compare each clinic against its purchase potential."

> "**Technical products** — biomaterials. Sporadic, case-driven. We compare each clinic against *its own* historical pattern, with year-over-year comparison so we don't read August holidays as churn."

> "Two parallel logics, one alert table."

(Move to slide 4.)

---

## Slide 4 — Pipeline

**🕒 Time:** 20 seconds.
**👀 Show:** Trace the four boxes left to right with your finger.

**🎤 Say:**
> "Purchase history goes in. Signal detection runs the two logics. We emit a daily alert with score, reason, channel, and full traceability. The result is a commercial action — routed to a sales rep, telesales, or marketing automation."

> "One function. One date input. End-to-end output."

(Move to slide 5.)

---

## Slide 5 — Alert anatomy

**🕒 Time:** 30 seconds.
**👀 Show:** Point at the JSON block, then read the four annotations on the right.

**🎤 Say:**
> "Here's what one alert looks like. Client forty-thousand-four-thirty-nine in Zaragoza. The motive explains itself: *promiscuous client, capturing six percent of potential, realistic growth margin*."

> "Four prioritisation signals — exactly the four the brief asks for: economic impact, urgency, client potential, and conversion probability. Score equals impact times urgency times conversion probability."

> "Most importantly: every metric that fired this alert is in the trace. **No black box.** A sales rep clicks one alert and sees the raw numbers. So does a judge."

(Move to slide 6.)

---

## Slide 6 — Numbers

**🕒 Time:** 25 seconds.
**👀 Show:** Hold for one beat at each big number.

**🎤 Say:**
> "Generated for the latest data — twenty-ninth of December — *four thousand two hundred seventy-one* alerts. Of those, *one thousand three hundred* are high priority."

> "Total expected commercial impact: *eleven point six million euros.*"

> "Split across four categories: lost clients, loss risk, sales opportunities, and healthy clients. Routed to delegado, telesales, or marketing automation."

(Move to slide 7.)

---

## Slide 7 — Live demo

**🕒 Time:** 2 minutes (the heart of the pitch).
**👀 Show:** Switch to the Streamlit dashboard. Have it open at `http://localhost:8501`.

### Step 1 — Client view (45s)

**🎤 Say:**
> "I'll start with the **Client view**. The system pre-selects clients with active alerts."

(Pick a top client from the dropdown.)

> "Here's a real client. **Loss risk** — orange banner. The system says: *contact within seven days*. The motive: *loyal client gone silent — used to buy nine thousand euros a year, no purchase for one hundred eighty days.*"

(Point at the cycle status.)

> "Look at the cycle status: *Overdue — twenty-six percent past their normal cycle*. They're not just silent — they're abnormally silent for *this specific client*."

(Point at the purchase history chart.)

> "And here's the visible drop in the history."

### Step 2 — Monitoring + daily cadence (45s)

**🎤 Say:**
> "Switch to **Monitoring**. KPI strip at the top: lost clients, loss risk, opportunities, healthy."

(Drag the date picker back to 2024-06-30.)

> "Now here's the daily-cadence proof. Same code, *eighteen months earlier*. The alert table updates. Different clients in trouble. The system is idempotent — it works for any historical date."

(Drag back to 2025-12-29. Click Export.)

> "Filtered alerts can be downloaded as CSV, or exported as HubSpot Tasks JSON. The CRM integration path is built in."

### Step 3 — Learning loop (30s)

**🎤 Say:**
> "Final tab — the **Learning loop**. We've seeded one hundred twenty mocked outcomes — clearly labelled as mock — to show the feedback contract."

(Point at the conversion-by-type table.)

> "Capture-window alerts convert at thirty-three percent. Silent alerts at eleven percent. Below the table, the system *automatically suggests threshold adjustments* — for example, raising the silent threshold because conversion is too low."

> "When real outcomes flow in, the same logic tunes the system. No retraining. No black box."

(Move to slide 8.)

---

## Slide 8 — Architecture

**🕒 Time:** 20 seconds.
**👀 Show:** Trace the four layers bottom to top.

**🎤 Say:**
> "Four-layer architecture: data, analytical, activation, feedback. Each layer is independent — you can swap any one of them without touching the others."

> "**Standalone today** — Python module plus Streamlit. **CRM-ready** — HubSpot Tasks exporter ships in this PR. **Daily idempotent** — one function, one date input."

(Move to slide 9.)

---

## Slide 9 — Brief scorecard

**🕒 Time:** 20 seconds.
**👀 Show:** Run your eye down the eight checkmarks.

**🎤 Say:**
> "Eight of eight deliverables from the brief — shipped. Purchase prediction for commodities, churn risk for technical products, capture windows, interpretable alerts, prioritisation, daily operation, standalone-to-CRM evolution path, and a learning loop."

> "Plus the four prioritisation signals: impact, urgency, client value, conversion probability."

(Move to slide 10.)

---

## Slide 10 — What's next

**🕒 Time:** 20 seconds.

**🎤 Say:**
> "Phase two: wire alerts into Inibsa's CRM via the HubSpot exporter, replace mocked outcomes with real recordings."

> "Phase three: threshold auto-tuning when we have at least five hundred real outcomes, and a thirty-day pilot with a control group to measure actual lift."

> "The architecture supports all of this without rewrites."

(Move to slide 11.)

---

## Slide 11 — Thank you

**🕒 Time:** 5 seconds, then take questions.

**🎤 Say:**
> "Thank you. Happy to take questions."

(Stop talking. Wait.)

---

# Q&A — backup answers

These are the predictable questions. Memorise the first sentence of each answer.

### "Did you measure predictive accuracy?"
> "Honestly: no. We deliberately didn't, because measuring intervention effectiveness requires a control group — which is phase two. What we *can* defend is the logic: every alert is traceable, every threshold is documented, every multiplier in the score has a rationale."

### "Why these specific thresholds?"
> "They're heuristics, calibrated to the brief's segments. The Learning loop tab shows their conversion rates — when we have enough real outcomes, the threshold-tuning module will adjust them automatically. We computed the data-driven quartile alternatives and the heuristic ones come out close."

### "Won't this fire the same silent alert every day for the same client?"
> "No. When an outcome is recorded as won, lost, or false positive, that combination of client × family × type is snoozed for thirty days. See `snooze_recently_actioned()` in the code."

### "Is this Machine Learning?"
> "Deliberately not. The brief is explicit: *the key is not technical sophistication but analytical and commercial utility*. We use rule-based detection with a feedback loop that tunes thresholds. Easy for the commercial team to interpret, easy for IT to maintain. Once we have at least five hundred real outcomes, ML becomes a real option — but right now, training on simulated labels would be self-deception."

### "What about clients with no potential data?"
> "The brief flags that sixteen percent of `potencial_h` rows are zero or unknown. We segment those as `unknown_potential` rather than guessing. They get reviewed separately — no false-positive churn alerts on data we don't have."

### "Why does the August month matter?"
> "We measured the seasonal effect empirically — August drops to twenty-five to thirty-eight percent of the yearly average. Without seasonality awareness, the system would fire roughly fifteen hundred false-positive churn alerts every August. We use a year-over-year baseline plus a holiday flag — drop signals are suppressed during holiday periods unless year-over-year *also* shows a real decline."

### "How does this scale?"
> "The daily run takes about five seconds for six thousand clients. Linear in client count. The architecture is layered — adding a new country, a new product family, or a new alert type doesn't touch the other layers."

### "Can you handle Portugal too?"
> "The brief said Portugal data quality is lower so initial scope is Spain. The pipeline is country-agnostic. Adding Portugal is a data-source change, not a code change."

### "What if a sales rep doesn't agree with an alert?"
> "Two answers. First, every alert is auditable — they can drill in, see the raw numbers, and decide. Second, the feedback loop captures `dismissed` as `false_positive` with a reason — and that reason flows back to the threshold-tuning module."

---

# Stage-management cheat sheet

- **Have the dashboard open** before you start — `streamlit run src/dashboard.py`
- **Reset the date picker** to `2025-12-29` before the demo
- **Pre-select a client** with a strong narrative (high score, clear motive)
- **If the demo crashes**: switch to the slides — they tell the same story
- **If you go over time**: cut Slide 10 (What's next) — it's the most expendable
- **If you have spare time**: dwell on Slide 5 (Alert anatomy) — it's where the credibility lives
