# Tutorial #2: Making sense of City of Sydney walking count data

Clean, map, and analyse multi-year pedestrian counts for the City of Sydney — Colab-ready with public data links. Build site maps, time-series, and a COVID-recovery view (vs 2019), then identify 2025’s busiest and slowest-to-recover locations.

**Open in Colab:** https://colab.research.google.com/drive/1pMhHGEYmZdGNTJeYglhlnn0YcuHOoKOk?usp=sharing  
[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1pMhHGEYmZdGNTJeYglhlnn0YcuHOoKOk?usp=sharing)

## What this notebook does
- Loads **Walking_count_sites.csv** and **Walking_count_surveys.csv** (public links included).
- Harmonises fields (e.g., `SiteID`, `Year`) and joins surveys to site metadata.
- Maps all sites (Folium) with circle **size+colour** = latest-year counts (no clustering).
- Plots **per-site** time-series (Plotly), keeping seasons/day-type separate (no seasonal summing).
- Computes **yearly mean & median** across all sites/seasons and visualises recovery vs **2019**.
- Ranks **Top/Bottom 10** busiest (2025) and **fastest/slowest** recovery vs 2019.
- Builds **side-by-side maps**: left = 2025 volume; right = % recovery vs 2019.

<img width="1195" alt="sydney-walking-tutorial-screenshot" src="https://substackcdn.com/image/fetch/$s_!poxE!,w_1456,c_limit,f_webp,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2cab9879-b839-4c74-b585-af1de83180d3_2782x1612.png" />

## Quick start (Colab)
1. Click the **Open in Colab** link or badge above.
2. Run the first install cell (only needed on a fresh runtime).
3. The notebook downloads the two CSVs from Google Drive automatically; you can swap in your own files/paths.

## Files
- `Tutorial_2_Making_sense_of_City_of_Sydney_walking_count_data.ipynb` — main notebook  

## Data
The notebook reads two CSVs via public links:
- **Walking_count_sites.csv** — site locations & attributes  
- **Walking_count_surveys.csv** — survey records by site, year, season, and day type  

Original datasets are available on the **[City of Sydney Open Data Hub](https://www.cityofsydney.nsw.gov.au/public-health-safety-programs/walking-counts)**.  
