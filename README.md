# UK Election Data Analysis

## Overview
This project analyzes UK general election data from 2019 and 2024, creating visualizations to explore patterns in voting results and candidate demographics. The analysis includes constituency-level results, party performance comparisons, and gender distribution of candidates and elected MPs.

## Data
The analysis uses two primary datasets:
- `2019.csv`: Contains results from the 2019 UK general election
- `2024.csv`: Contains results from the 2024 UK general election

Data sources:
- 2024 election data: [UK Parliament Commons Library, Briefing Paper CBP-10009](https://commonslibrary.parliament.uk/research-briefings/cbp-10009/)
- 2019 election data: [UK Parliament Commons Library, Briefing Paper CBP-8749](https://commonslibrary.parliament.uk/research-briefings/cbp-8749/)

Both datasets include information about:
- Constituencies (names, regions, types)
- Candidates (names, gender, party affiliation)
- Voting results (votes received, vote share, change from previous election)
- MP status (sitting MP, former MP)

## Features
The code provides several analyses and visualizations:

### 1. Party Performance Analysis
- Seat totals by party for the 2024 election
- Changes in seats compared to the 2019 election
- Visual representation with color-coded horizontal bar charts

### 2. Gender Distribution Analysis
- Overall gender distribution of all candidates
- Gender distribution by party (top 6 parties)
- Gender distribution of elected MPs
- Comparison of gender distribution between 2019 and 2024 elections

### 3. Electoral Map Visualizations
- Hexagonal map showing constituency winners (equal area representation)
- Geographical map of election results

## Files
- `uk_election_map_generator.py`: Generates electoral maps (hexagonal and geographical)
- `uk_election_analysis.py`: Processes and analyzes election data, creates visualizations

## Requirements
- Python 3.x
- pandas
- numpy
- matplotlib
- seaborn
- geopandas (for geographical maps)

## Usage
1. Place the data files in the appropriate directory:
   ```
   /content/drive/MyDrive/2019.csv
   /content/drive/MyDrive/2024.csv
   ```

2. Run the analysis script:
   ```python
   python uk_election_analysis.py
   ```

3. Generate electoral maps:
   ```python
   python uk_election_map_generator.py
   ```

## Data Preprocessing
The analysis includes several preprocessing steps:
- Handling missing values
- Combining "Labour" and "Labour Co-operative" parties
- Identifying constituency winners
- Calculating seat changes between elections
- Grouping smaller parties as "Other" for visualization clarity

## Visualizations
The code generates several visualizations:
- Party seat totals and changes (horizontal bar charts)
- Candidate gender distribution (pie charts)
- Gender distribution by party (stacked bar charts)
- Electoral maps showing constituency winners

## Notes
- The code handles the "Labour" and "Labour Co-operative" parties as a single entity since they operate as an electoral alliance
- Smaller parties are grouped as "Other" in some visualizations for clarity
- The electoral maps require additional geographic data files not included in this repository
