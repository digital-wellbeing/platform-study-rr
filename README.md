# Relationships Between Health and Logged Video Game Play Across Platforms

This repo is structured to match our programmatic registered report. 

An overview of the 8 different data tables and the variables within them can be found in `codebook.xlsx`. 

These data tables are generated in the following scripts:

- In `0_generateSyntheticData.qmd`, we simulate a total of 8 data tables that will mimic the structure of the eventual
- In `1_preprocess.qmd`, we clean the data and calculate relevant derived variables (e.g., mean scores, play behavior metrics, and so on).

We then analyze these data in the following scripts:

- In `2_basicNeeds.qmd`, we present the analysis code for Study 1: the relationship between basic needs and video game play.
- In `3_sleep.qmd`, we present the analysis code for Study 2: the relationship between sleep and video game play.
- In `4_genres.qmd`, we present the analysis code for Study 3: the relationship between video game genres and video game play.
- In `9_screenshots.qmd`, we present work-in-progress optical character recognition code for extracting screen use data from iOS screenshots. 

## Running

- For internal use, running `quarto render` in the Rstudio terminal will run all of the (completed) quarto files. This command uses the specifications in `_quarto.yml` to render the files in the correct order (indicated by their number), and output them to `_output/`.

- For external use, !!TODO!!
