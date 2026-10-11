# College ROI Analysis

## Author

Howard Wei ([@HowardWei123](https://github.com/HowardWei123))

## Description

College ROI Analysis utilizes the U.S. Department of Education's College Scoreboard data to understand the relationship between attending college, student debt, and post-graduation earnings. This project will look at outcomes across all institution types to see whether the price of education actually leads to higher earnings. Students on financial aid or grants will also be examined for graduation rates and earnings to see how well colleges are serving low-income students. Since many schools may omit values due to privacy, we can study these schools and draw conclusions from their omitted data. Finally, an interactive dashboard will allow users to explore different visualizations of the data.
## Outline and Plan

### Interface

The interactive dashboard interface will be built in Python using the Streamlit framework and Plotly library. The dashboard will include filters to update visualizations in real-time.

### Data Collection and Storage

Data will be accessed through the official College Scorecard API (`api.data.gov/ed/collegescorecard`), with backup data contained in the "Most Recent Institution-Level Data" CSV from [collegescorecard.ed.gov/data](https://collegescorecard.ed.gov/data/). The free API key will be stored in `.env` and only used when running the data collection script to retrieve raw data. After cleaning and processing, the data will be stored in gitignored CSV files, and a separate MD file will document every step to make the data reproducible.

### Data Analysis and Visualization

Descriptive statistics will be derived from the clean data for cost, debt, degree completion time, and earnings, all while inspecting distributions and outliers relative to institution types. Inferential analysis will require a one-way ANOVA and a regression model to compare and contrast outcomes. A Chi-square test would also be needed to determine what data is omitted relative to institution types. An interactive scatter plot, bar plot, and U.S. map will be generated for the main panel, with users having the option to create more visualizations if they want to. If time allows, a machine learning extension that predicts earnings based on different incomes and institution types will be implemented.

## License

Released under the MIT License. See [LICENSE](LICENSE).
