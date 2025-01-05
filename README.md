# UBC MineCraft Player Engagement Analysis

## Introduction

This project aims to analyze player datasets from a UBC MineCraft server to identify the kinds of players most likely to contribute a large amount of data. This information will help the research team target these players in their recruiting efforts. We selected the first question posed by the project lead, Frank Wood:

**“Which ‘kinds’ of players are most likely to contribute a large amount of data?”**

By addressing this question, we aim to assist the research team in finding players who will provide meaningful data for future analyses.

## Datasets

We utilized two datasets collected from the MineCraft server:

### `players.csv`

- Contains information about 196 unique players.
- This dataset includes demographic data and the total hours each player contributed.

| Variable         | Description                                                                 |
|------------------|-----------------------------------------------------------------------------|
| experience       | Player's experience level: beginner, amateur, regular, pro, or veteran. (Qualitative) |
| subscribe        | Whether the player subscribed to email updates. (Qualitative)               |
| hashedEmail      | Encrypted email address of the player. (Qualitative)                        |
| played_hours     | Total number of hours played by the player. (Quantitative)                  |
| name             | Player's name. Not used in analysis. (Qualitative)                         |
| gender           | Player's gender. (Qualitative)                                              |
| age              | Player's age. (Quantitative)                                                |
| individualId     | Not relevant to the analysis. (Qualitative)                                 |
| organizationName | Not relevant to the analysis. (Qualitative)                                 |

### `sessions.csv`

- Contains 1535 observations of individual player sessions.

| Variable            | Description                                                          |
|---------------------|----------------------------------------------------------------------|
| hashedEmail         | Encrypted email address of the player. (Qualitative)                 |
| start_time          | Start time of the session. (Quantitative)                            |
| end_time            | End time of the session. (Quantitative)                              |
| original_start_time | Original start time in UNIX format. Not used in the analysis. (Quantitative) |
| original_end_time   | Original end time in UNIX format. Not used in the analysis. (Quantitative) |

## Challenges

- **Players with zero hours**: A significant portion of the dataset consists of players who contributed zero hours. This made data visualization more challenging as it resulted in sparse plots.
- **Unnecessary variables**: Several variables were irrelevant to the analysis and were removed during data wrangling.

## Methodology

The response variable of interest is `played_hours`, representing the total hours played by each player. The explanatory variables we used to predict player engagement include `experience`, `gender`, and `age`. The goal is to identify correlations between these explanatory variables and the hours contributed by each player.

We cleaned and preprocessed both datasets, removing unnecessary columns and handling time zone differences in the session data. After wrangling, we conducted our analysis and developed insights about the players most likely to contribute the most data.

## Conclusion

Our analysis provides actionable insights into the kinds of players that contribute the most data, allowing the research team to better target their recruiting efforts for future studies.

## Installation and Setup

1. Clone the repository:

```bash
git clone https://github.com/your-username/your-repository.git
```

2. Install the required packages:

```bash
pip install -r requirements.txt
```

3. Run the analysis notebook:

```bash
jupyter notebook analysis.ipynb
```

## Results

For detailed results and analysis, please refer to the [final report](./minecraft_player_engagement_analysis.ipynb).

## License

This project is licensed under the MIT License - see the [LICENSE](./LICENSE) file for details.
