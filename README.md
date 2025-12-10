# STA522 Project 2: Paper Helicopter Flight Experiment

**Authors:** Zhihao Chen, Zixiao Tan

## Overview

This project investigates the factors affecting paper helicopter flight duration through a full factorial experimental design. We examine four factors to determine their individual and interactive effects on flight time.

## Research Questions

1. Which factors are most important for achieving longer flight duration?
2. Does the rotor length effect vary by leg width?
3. What is the ideal factor combination for maximum flight time?

## Experimental Design

### Factors Studied

| Factor | Low Level | High Level |
|--------|-----------|------------|
| Rotor Length | 7.5 cm | 8.5 cm |
| Leg Length | 7.5 cm | 12.0 cm |
| Leg Width | 3.2 cm | 5.0 cm |
| Leg Clip | No | Yes |

### Design

- **Type:** Full factorial design (2^4 = 16 treatment combinations)
- **Replications:** 5 flights per combination
- **Total Observations:** 80 flights
- **Outcome:** Flight time (seconds)

## Key Findings

### Q1: Most Important Factor

**Rotor length** is the most critical factor for flight duration:
- **Positive effect:** High rotor (+0.220s, p<0.001)
- **Negative effects:**
  - Paper clip (-0.315s, p<0.001)
  - High leg length (-0.159s, p<0.001)
  - High leg width (-0.152s, p<0.001)

### Q2: Interaction Effects

The rotor × leg width interaction is **not significant** (p>0.05), indicating that the rotor length effect does not vary by leg width. However, other significant interactions were found:
- rotor × leg length: -0.448 (p=0.006)
- rotor × clip: -0.490 (p=0.003)
- rotor × leg length × clip: +0.696 (p=0.003)

### Q3: Optimal Design

**Treatment 'a'** yields the longest flight duration:
- **Configuration:** High rotor (8.5cm), low leg length (7.5cm), low leg width (3.2cm), no clip
- **Expected flight time:** 2.47 seconds (95% CI: 2.31-2.63s)
- **Strategy:** Maximize the beneficial rotor effect while minimizing all detrimental factors

## Project Files

- `project2.Rmd` - R Markdown analysis file with full methodology and code
- `project2.pdf` - Compiled PDF report with results and visualizations
- `paperplane.csv` - Experimental flight time data
- `problem.pdf` - Project assignment description
- `Making a Paper Helicopter.pdf` - Helicopter construction guide

## Statistical Methods

- Full factorial ANOVA model with all main effects and interactions
- Model diagnostics to verify assumptions (normality, constant variance)
- Nested F-tests to compare models
- 95% confidence intervals for treatment effects

## Dependencies

```r
library(tidyverse)
library(dplyr)
library(ggplot2)
library(kableExtra)
```

## How to Reproduce

1. Open `project2.Rmd` in RStudio
2. Install required packages
3. Knit the document to generate the PDF report

## Results Summary

The experiment demonstrates that **longer rotor length significantly improves flight time**, while adding weight (clip) or increasing leg dimensions reduces performance. The optimal helicopter design achieves approximately 2.5 seconds of flight time by maximizing rotor length and minimizing all other factors.
