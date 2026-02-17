Heat Risk and System Capacity
A Practical, Computable Framework
1. The Core Idea
Heat disasters are rarely about the hottest temperature of the day. They’re about capacity failure: when people, buildings, and infrastructure can no longer shed accumulated heat.

The key driver is cumulative heat load with recovery—how hot, how humid, for how long, and whether nights cool enough for bodies and systems to reset. A city’s effective heat stress isn’t a single number; it’s a location‑specific Tw\* shaped by climate, housing, AC access, grid strength, and population vulnerability.

This framework turns that insight into simple, transparent metrics that anyone can compute from basic weather data.

2. Core Inputs
2.1 Local baseline / zone
Every location needs its own thresholds:

Daytime baseline (e.g., 30–32°C in humid tropics, 34–36°C in arid zones)

Nighttime recovery baseline (typically 24–26°C, adjusted for housing + AC prevalence)

2.2 Multi‑day weather sequences
Hourly or 3‑hourly temperature + humidity

Can be:

Historical (Chicago 1995, Europe 2003)

Synthetic (e.g., +2–3°C warming applied to past events)

2.3 Optional system context
Grid strain proxy (% of peak load)

Vulnerable population factor (age, health, SES, AC access)

3. Key Computed Metrics (Tw\* Family)
These are the “fast‑turnaround” metrics that make the conceptual model operational.

3.1 Cumulative Heat Load (CHL)
What it captures: How much heat the system has absorbed above its local baseline.

Definition: Degree‑hours (or degree‑days) above a daytime baseline, humidity‑weighted.

CHL
=
∑
hours
𝑤
humid
⋅
max
⁡
(
𝑇
eff
−
𝑇
base,day
,
0
)
Where 
𝑇
eff
 can be:

Apparent temperature

Wet‑bulb

A simple T + RH function

Interpretation:  
CHL shows why “not that hot yet” heatwaves still kill—because the load keeps building.

3.2 Hot Night Excess (HNe) / Recovery Deficit
What it captures: Whether nights allow recovery. This is the strongest predictor of hospitalizations.

Definition: °C·h above a nighttime threshold during the sleep window (20:00–08:00).

HNe
=
∑
20:00–08:00
max
⁡
(
𝑇
night
−
𝑇
base,night
,
0
)
Variants:

Severe HNe: threshold at 28°C

Strongly associated with elderly and low‑SES hospitalization spikes

Binary “tropical night” → replaced by a continuous, more predictive metric

Interpretation:  
Warm nights are the hinge between “straining” and “failure.”

3.3 Compound Day–Night Strain Indicator
What it captures: The most dangerous pattern—when heat never lets up.

Components:

Consecutive hot days (CHL above threshold)

Consecutive hot nights (HNe above threshold)

Compound streaks (both exceeded for N cycles)

System margin toggles: grid strain, vulnerable population factor

Composite form (conceptual):

RiskIndex
∝
𝑓
(
CHL
,
HNe
,
streak length
,
grid strain
,
vulnerability
)
No universal formula—each city calibrates to its own history.

4. The Risk Curve: Stable → Straining → Failure
Heat risk rises nonlinearly. These states overlap and shift by location.

4.1 Stable / Absorbing
Systems operate within design limits.

Metric signature:

CHL low or resetting daily

HNe near zero

No compound streaks

Grid demand normal

4.2 Straining / Capacity Crossover
Demand begins to exceed capacity; recovery windows shrink.

Metric signature:

CHL rising for multiple days

HNe elevated for 2+ nights (e.g., min temp >25°C)

Compound streaks forming

Grid strain flags

Hospital admissions rising

This is where Chicago 1995 and Europe 2003 spent most of their deadly period.

4.3 Failure / Cascade
Failures reinforce each other; local systems cannot self‑correct.

Metric signature:

Very high CHL + HNe

Long compound streaks

Grid at/beyond capacity, outages

EMS/hospitals overwhelmed

Here the curve steepens: one more hot night can double the harm.

5. Nonlinear Escalation (Risk Multiplier)
Why the curve bends upward:

Compounding probabilities:  
Multi‑day heatwaves increase faster than single‑day extremes as the climate warms.

Compounding load:  
CHL and HNe accumulate; each day adds to a stock.

Compounding vulnerability:  
Studies show compound day–night heat yields higher mortality odds (OR 1.1–1.3+), especially for elderly and low‑SES groups.

The framework expresses this as a risk multiplier that jumps sharply once thresholds are crossed.

6. Output Visualizations
These make the invisible dynamics visible.

6.1 Timeline Plot
Daily max/min

Humidity or Tw overlay

CHL as a rising curve

HNe as nighttime bars

Shows how load builds even when daytime peaks look modest.

6.2 Risk State Progression
A color band or panel showing:

Green → Stable

Amber → Straining

Red → Failure

Driven by CHL, HNe, and compound streaks.

6.3 Nonlinear Escalation Gauge
A dial showing the risk multiplier responding to:

Consecutive hot nights

Compound streaks

Grid strain

Vulnerability factor

This is the “jumpiness” made visual.

7. Demo Scenarios
Chicago 1995
Moderate daytime peaks

Extremely warm nights

HNe dominates

Shows how recovery failure drives mortality

Europe 2003
Long duration

High CHL

Long compound streaks

Risk multiplier climbs relentlessly

Synthetic +2–3°C warming
Apply uniform warming to past events

CHL and HNe rise faster

Straining → Failure transitions occur earlier and more often

8. README Framing (Drop‑In)
Beyond Peak Temperature: Why Recovery Windows and System Margins Matter More

Peak temperature alone misses the mechanisms that kill.

CHL shows load accumulation.

HNe shows recovery failure, the strongest predictor of harm.

Compound day–night metrics capture the highest‑risk patterns.

System margin toggles connect weather to infrastructure and people, not just thermometers.

The framework avoids WBGT pitfalls by centering duration, recovery, and capacity—the things that actually break first.# Heat-Risk-as-Capacity-Failure-A-Computable-Public-Data-Framework
