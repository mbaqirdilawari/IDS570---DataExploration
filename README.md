# IDS 570 Data Exploration: Political Economy Corpus (Structured Option)

Exploratory analysis of a corpus of 23 political economy texts for IDS 570 (Text as Data), Duke University.

## What the analysis does

1. **Step 0: Cleaning.** Normalizes the long S (ſ), removes words containing the illegible-character marker (●), and checks for Early Modern spellings.
2. **Approach 1: TF-IDF.** Builds a document-feature matrix and extracts the 15 most distinctive terms for each document.
3. **Approach 2: Pearson correlation.** Computes pairwise correlations between all documents and visualizes them as a heatmap.
4. **Approach 3: Syntactic complexity.** Parses two texts (A06785 and A07594_Circle) with udpipe and compares sentence length, clauses, subordination, coordination and complex nominals.
5. **Synthesis.** Brings the three approaches together.

## Files

- `data_exploration.qmd`: all code and written analysis
- `data_exploration.html`: the rendered report
- `outputs/`: tables (CSV) and the heatmap (PNG) produced by the code

## How to run

1. Place the 23 corpus text files (from the course Canvas page, "Text Files" folder) in a folder called `Files/` next to `data_exploration.qmd`.
2. Install the packages: `install.packages(c("tidyverse", "quanteda", "quanteda.textstats", "tidytext", "udpipe", "knitr"))`
3. Create an `outputs/` folder, then render `data_exploration.qmd` in RStudio.

The udpipe English model downloads automatically on the first run. Parsing the two texts takes several minutes the first time. The result is then saved to `outputs/udpipe_annotations.rds` and reused.

