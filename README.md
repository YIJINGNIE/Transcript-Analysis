# Transcript-Analysis
A data analysis of my community college transcript (2024–2026)
# Whatcom Community College Transcript Analysis

A data analysis of my community college transcript (2024–2026): rebuilding and
verifying my official GPA with Python, then visualizing my academic record.

## Background

As a transfer student heading into the Informatics / Data Science track at the
University of Washington, I used my own transcript as my first end-to-end data
project — practicing the full workflow a data analyst uses every day: load raw
data, clean it, engineer features, group and aggregate, join tables, and
visualize the result.

## Data

- **Source:** my official transcript, Autumn 2024 – Summer 2026 (8 terms)
- **Size:** 21 courses, 10 columns (Year, Season, Course_code, Grade,
  Attempted, Points, Repeated, …)
- **Official cumulative GPA:** 3.946

## Analysis

1. **Load & inspect** — read the CSV; check shape, columns, and data types
2. **Clean** — handle missing values, standardize text, build derived columns
3. **GPA calculation** — recompute cumulative and per-term GPA using a *weighted*
   average (quality points ÷ attempted credits)
4. **Join & aggregate** — merge a department lookup table; compute GPA and course
   counts by department
5. **Visualize** — a GPA trend line, plus a by-department dashboard (GPA and
   course count side by side)

## Key Findings

- Recomputed cumulative GPA = **3.946**, matching the official transcript exactly
- All 8 terms reconciled against the official record
- Lowest term was 2025 Winter (**3.667**) — one B in English Composition
- By department: most are 4.0; **English** is 3.5 (that one B), while
  **Mathematics** has both the most courses (4) and a 4.0 — the most consistent

## What I Practiced

- **Weighted vs. simple average** — GPA must be weighted by credits; a plain
  `.mean()` only *looks* right when every course has equal credits
- **Left joins to preserve data** — keep every course when adding department
  names, instead of silently dropping unmatched rows
- **Sanity-checking every number** against the official transcript

## Tools

Python · pandas · NumPy · matplotlib · Google Colab
