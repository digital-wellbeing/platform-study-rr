# Relationships Between Health and Logged Video Game Play Across Platforms

This repo is structured to match our programmatic registered report. 


## Scripts

The first script generates a series of 8 simulated data tables, overviewed in `codebook.xlsx`. Generating the synthetic data is only possible by **internal** users, but the code is available in `0_generateSyntheticData.qmd`. The remaining scripts can be run by **external** users.

These data tables are generated in the following scripts:

- In `0_generateSyntheticData.qmd`, we simulate a total of 8 data tables that will mimic the structure of the eventual
- In `1_preprocess.qmd`, we clean the data and calculate relevant derived variables (e.g., mean scores, play behavior metrics, and so on).

We then analyze these data in the following scripts:

- In `2_basicNeeds.qmd`, we present the analysis code for Study 1: the relationship between basic needs and video game play.
- In `3_sleep.qmd`, we present the analysis code for Study 2: the relationship between sleep and video game play.
- In `4_genres.qmd`, we present the analysis code for Study 3: the relationship between video game genres and video game play.
- In `9_screenshots.qmd`, we present work-in-progress optical character recognition code for extracting screen use data from iOS screenshots. 

## Hygiene files
- `.Renviron` defines the path to key internal data files and API credentials.
- `index.qmd` is the header file that stitches the other Quarto files together into book form. 

## Running

- For **external use** (non-lab members), run `quarto render --profile external` in the Rstudio terminal to render all of the quarto files except 0_generateSyntheticData.qmd, which requires internal credentials. This command uses the specifications in `_quarto-external.yml` to render the files in the correct order (indicated by their number), and output them to `outputs/`.

- For **internal use**, run `quarto render --profile internal` in the Rstudio terminal to render *all* quarto files. This command uses the specifications in `_quarto-internal.yml` to render the files in the correct order (indicated by their number), and output them to `docs/`. The files in `docs/` are hosted on GitHub pages here: [https://digital-wellbeing.github.io/platform-study-rr/](https://digital-wellbeing.github.io/platform-study-rr/).



