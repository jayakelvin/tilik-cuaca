# TilikCuaca

**Weather in context, through data.**

TilikCuaca is a collection of compact, reproducible meteorological assessments built around real weather events.

The idea is simple:

> **One meteorological question → minimum necessary public data → 1–3 figures → concise interpretation → reproducible Python workflow.**

Rather than documenting every aspect of an event, each assessment focuses on one question that can be answered clearly and scientifically using observations, forecasts, reanalysis, satellite, radar, or climate data.

## Why TilikCuaca?

*Tilik* is an Indonesian word meaning to observe, examine, or look into something.

TilikCuaca therefore reflects the purpose of this project: examining weather carefully using data and placing it in the appropriate meteorological or climatological context.

## What kinds of questions?

Examples include:

- How unusual is the rainfall occurring now?
- Is a heat event actually extreme for this location and season?
- Was a prolonged rainy period unusual because of its duration, accumulation, or both?
- Did a forecast capture an approaching windstorm?
- How has a tropical cyclone evolved relative to forecasts?
- How unusual is the current atmospheric circulation?
- Is an ongoing drought meteorologically exceptional?
- How does a recent event compare with the historical record?
- How might a relevant threshold change under future climate conditions?

The event itself is not necessarily the main product.

The objective is to demonstrate a method that can be reused for another location, period, or event.

## Principles

Every TilikCuaca assessment should be:

**Focused**  
One primary meteorological question.

**Compact**  
Normally no more than 1–3 final figures.

**Reproducible**  
The analysis should be reproducible with Python and documented public data sources.

**Scientifically defensible**  
Observations, forecasts, reanalysis, model output, derived quantities, and interpretations should be clearly distinguished.

**Transparent about limitations**  
The analysis should not support conclusions beyond what the data and method can demonstrate.

**Reusable**  
Where practical, locations, dates, thresholds, and other parameters should be easy to modify.

A null result is also a valid result. An event does not need to be record-breaking or exceptional to be scientifically interesting.

## Assessments

| ID | Assessment | Question | Status |
|---|---|---|---|
| 001 | Tokyo rainy streak | Was Tokyo's prolonged rainy period unusual because of persistence, rainfall accumulation, or both? | In progress |

Each assessment has its own directory under [`assessments/`](assessments/).

## Repository structure

```text
tilik-cuaca/
├── assessments/
│   └── 001_tokyo_rain_streak/
├── src/
│   └── tilikcuaca/
├── requirements.txt
└── README.md
```

Code initially remains within individual assessments.

Functions are moved into `src/tilikcuaca/` only when they become genuinely reusable across multiple assessments.

## Data

TilikCuaca prioritizes authoritative and openly accessible sources, including national meteorological agencies and established international Earth-observation and climate-data services.

Potential sources include:

- DWD
- JMA
- BMKG
- BoM
- MetService
- PAGASA
- ECMWF Open Data
- ERA5 / ERA5-Land
- Copernicus services
- EUMETSAT
- GPM IMERG
- Sentinel

Each assessment documents the exact dataset, variable, source, period, processing steps, and relevant limitations.

Large source datasets are generally not stored in this repository.

## Reproducibility

Each completed assessment should contain enough information to answer:

1. What data were used?
2. Where did the data come from?
3. What variables and periods were analysed?
4. What calculations were performed?
5. What assumptions or thresholds were used?
6. What are the important limitations?
7. How can the figures be regenerated?

## TilikCuaca vs. Earth in Extremes

TilikCuaca is designed for focused, reusable assessments.

More comprehensive event investigations involving multiple scientific questions, datasets, processes, or extensive interpretation belong in the separate **Earth in Extremes** project.

A useful rule:

> If answering the original question repeatedly requires another dataset, another mechanism, and another figure, the investigation may have grown beyond TilikCuaca.

## License

Code in this repository is released under the MIT License unless otherwise stated.

Individual datasets remain subject to the terms and licences of their respective providers.