Heat Risk and System Capacity
A Practical, Computable Public-Data Framework
The Core Idea

Heat disasters are rarely about the single hottest temperature of the day.

They occur when system capacity fails — when people, buildings, and infrastructure can no longer shed accumulated heat.

The key driver is cumulative heat load with recovery:

How hot it gets

How humid it is

How long it lasts

Whether nights cool enough for bodies and systems to reset

A city’s effective heat stress is not one number.

It is a location-specific heat burden (Tw*) shaped by:

Climate baseline

Housing conditions

Air-conditioning access

Grid reliability

Population vulnerability

This framework turns that insight into simple, transparent metrics that anyone can compute from basic weather data.

Core Inputs
1. Local Baselines

Every location requires its own thresholds.

Daytime baseline

Examples:

30–32 °C in humid climates

34–36 °C in arid regions

Nighttime recovery baseline

Typically:

24–26 °C minimum temperature

Adjusted for:

Housing quality

AC prevalence

Urban heat-island effects

2. Multi-Day Weather Sequences

Inputs include:

Hourly or 3-hourly temperature

Humidity

These can be:

Historical events (Chicago 1995, Europe 2003)

Synthetic warming scenarios (+2–3 °C)

3. Optional System Context

Additional indicators improve realism:

Grid strain (% of peak load)

Vulnerable population factors

Age

Health status

Socioeconomic conditions

AC access

Key Computed Metrics (Tw* Family)

These metrics make the conceptual model operational.

1. Cumulative Heat Load (CHL)
What it captures

Total heat absorbed above the daytime baseline.

Definition

Degree-hours above threshold, humidity-weighted:

CHL = Σ [ w_humid × max( T_eff − T_base_day, 0 ) ]

Where T_eff may be:

Apparent temperature

Wet-bulb temperature

A simple temperature-humidity proxy

Interpretation

CHL explains why heatwaves can become deadly even when daily peaks seem moderate — because heat accumulates over time.

2. Hot Night Excess (HNe) — Recovery Deficit
What it captures

Whether nights allow physiological and infrastructure recovery.

Definition

Degree-hours above nighttime baseline during the sleep window (20:00–08:00):

HNe = Σ max( T_night − T_base_night, 0 )

Key insight

Warm nights are the strongest predictor of hospitalizations and mortality.

Variants include:

Severe HNe threshold: 28 °C

Continuous metric replacing binary “tropical night” indicators

3. Compound Day-Night Strain Indicator
What it captures

The most dangerous pattern — when heat never lets up.

Components:

Consecutive high-CHL days

Consecutive high-HNe nights

Length of compound streaks

Optional modifiers:

Grid strain

Vulnerability factors

Conceptual form:

Risk Index ∝ f( CHL, HNe, streak length, system margins )

No universal formula — calibration is location-specific.

The Risk Curve: Stable → Straining → Failure

Heat risk rises nonlinearly as system capacity is exceeded.

Stable (Absorbing)

Systems operate within limits.

Indicators:

Low or resetting CHL

Minimal HNe

No compound streaks

Normal grid demand

Straining (Capacity Crossover)

Recovery windows shrink.

Indicators:

Rising multi-day CHL

Elevated HNe for 2+ nights

Emerging compound streaks

Grid stress signals

This stage drove most mortality in Chicago 1995 and Europe 2003.

Failure (Cascade)

Self-reinforcing breakdown occurs.

Indicators:

Very high CHL + HNe

Long compound streaks

Grid outages

Emergency services overwhelmed

At this stage, one additional hot night can dramatically increase harm.

Why Risk Escalates Nonlinearly

Three compounding mechanisms:

1. Probability compounding

Multi-day heatwaves increase faster than single-day extremes.

2. Load accumulation

Heat storage grows daily when recovery fails.

3. Vulnerability amplification

Compound heat exposure raises mortality risk significantly, especially for elderly and low-income populations.

Output Visualizations

The framework emphasizes making invisible dynamics visible.

Timeline View

Shows:

Daily max/min temperature

Humidity or wet-bulb overlay

Rising CHL curve

Nighttime HNe bars

Risk State Progression

Color-coded system states:

Green — Stable

Amber — Straining

Red — Failure

Nonlinear Risk Gauge

Displays escalation based on:

Consecutive hot nights

Compound streak length

Grid strain

Vulnerability factors

Example Scenarios
Chicago 1995

Moderate daytime heat but extreme nighttime warmth.

Recovery failure dominated risk.

Europe 2003

Long duration with high CHL and persistent hot nights.

Risk multiplier climbed continuously.

Synthetic +2–3 °C Warming

Demonstrates how small baseline warming:

Accelerates CHL growth

Eliminates recovery windows earlier

Triggers failure states sooner

Why This Framework Matters

Peak temperature alone misses the mechanisms that cause harm.

This approach focuses on what actually breaks:

Heat accumulation (CHL)

Recovery failure (HNe)

Compound persistence

System capacity margins

What This Framework Is (and Is Not)
It IS:

A transparent public-data model

A systems-risk framework

A literacy tool for understanding heat risk

It is NOT:

A weather forecast model

A physiological simulation

A replacement for operational heat indices

The Big Insight

Heat disasters are not defined by how hot it gets.

They are defined by how long systems fail to cool.

System margin toggles connect weather to infrastructure and people, not just thermometers.

The framework avoids WBGT pitfalls by centering duration, recovery, and capacity—the things that actually break first.# Heat-Risk-as-Capacity-Failure-A-Computable-Public-Data-Framework
