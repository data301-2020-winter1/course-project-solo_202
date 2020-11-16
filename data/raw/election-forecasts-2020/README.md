---
files:
 - https://projects.fivethirtyeight.com/2020-general-data/presidential_national_toplines_2020.csv
 - https://projects.fivethirtyeight.com/2020-general-data/presidential_state_toplines_2020.csv
 - https://projects.fivethirtyeight.com/2020-general-data/presidential_polls_2020.csv
 - https://projects.fivethirtyeight.com/2020-general-data/presidential_poll_averages_2020.csv
 - https://projects.fivethirtyeight.com/2020-general-data/presidential_ev_probabilities_2020.csv
 - https://projects.fivethirtyeight.com/2020-general-data/presidential_scenario_analysis_2020.csv
 - https://projects.fivethirtyeight.com/2020-general-data/presidential_forecast_steps.csv
 - https://projects.fivethirtyeight.com/2020-general-data/economic_index.csv
 - https://projects.fivethirtyeight.com/2020-general-data/electoral_college_vs_popvote.csv
 - https://projects.fivethirtyeight.com/2020-general-data/senate_national_toplines_2020.csv
 - https://projects.fivethirtyeight.com/2020-general-data/senate_state_toplines_2020.csv
 - https://projects.fivethirtyeight.com/2020-general-data/house_national_toplines_2020.csv
 - https://projects.fivethirtyeight.com/2020-general-data/house_district_toplines_2020.csv
 - https://projects.fivethirtyeight.com/2020-general-data/senate_fundamentals.csv
 - https://projects.fivethirtyeight.com/2020-general-data/house_fundamentals.csv
 - https://projects.fivethirtyeight.com/2020-general-data/senate_seat_distribution.csv
 - https://projects.fivethirtyeight.com/2020-general-data/house_seat_distribution.csv
 - https://projects.fivethirtyeight.com/2020-general-data/senate_steps.csv
 - https://projects.fivethirtyeight.com/2020-general-data/house_steps.csv
 - https://projects.fivethirtyeight.com/2020-general-data/joint_probabilities.csv
---

# election-forecasts-2020

This file contains links to the data behind our [2020 General Election Forecast](https://projects.fivethirtyeight.com/2020-election-forecast/).


## Presidential Forecast
`presidential_state_toplines_2020.csv` contains the final state-level toplines on each day. This sheet contains the following additional columns:

Column | Description
-------|------------
`state` | Name of the state
`tipping` | Tipping-point chance, the chance the state will deliver the decisive vote in the Electoral College
`vpi` | Voter power index, the relative likelihood that an individual voter in the state will determine the Electoral College winner
`winstate_inc` | Chance the incumbent will win the state
`winstate_chal` | Chance the challenger will win the state
`winstate_3rd` | Chance the third-party candidate will win the state
`voteshare_inc`, `voteshare_inc_lo`, `voteshare_inc_hi` | Forecasted vote share for the incumbent, including the upper and lower bounds of an 80% confidence interval
`voteshare_chal`, `voteshare_chal_lo`, `voteshare_chal_hi` | Forecasted vote share for the challenger, including the upper and lower bounds of an 80% confidence interval
`voteshare_3rd`, `voteshare_3rd_lo`, `voteshare_3rd_hi` | Forecasted vote share for the third-party candidate, including the upper and lower bounds of an 80% confidence interval
`voteshare_other`, `voteshare_other_lo`, `voteshare_other_hi` | Forecasted vote share for other candidates, including the upper and lower bounds of an 80% confidence interval
`margin`, `margin_lo`, `margin_hi` | Forecasted margin for the incumbent, including the upper and lower bounds of an 80% confidence interval
`win_EC_if_win_state_inc` | Chance that the incumbent will win the Electoral College if they win this state
`win_EC_if_win_state_chal` | Chance that the challenger will win the Electoral College if they win this state
`win_state_if_win_EC_inc` | Chance that the incumbent will win this state if they win the Electoral College
`win_state_if_win_EC_chal` | Chance that the challenger will win this state if they win the Electoral College
`state_turnout`, `state_turnout_hi`, `state_turnout_lo` | Forecasted state-level voter turnout based on past turnout, estimates of population growth, polls about whether voters are more or less enthusiastic about the election than usual and other factors in each state. Includes the upper and lower bounds of an 80% confidence interval. Turnout estimates are only available on model runs after Sept. 5, 2020.



`presidential_poll_averages_2020.csv` contains the polling averages for each day. Additional poll and poling average data can be found in our [polls dataset](https://github.com/fivethirtyeight/data/tree/master/polls). This sheet contains the following additional columns:

Column | Description
-------|------------
pct_estimate | Polling average for the candidate listed in `candidate_name` on `modeldate`
pct_trend_adjusted | Trendline adjusted polling average for the candidate listed in `candidate_name` on `modeldate`


`economic_index.csv` contains economic indicators that serve as inputs to the forecast. For more information on these indicators, see [this post](https://fivethirtyeight.com/features/measuring-the-effect-of-the-economy-on-elections/). The economic indexes were collected from the [Federal Reserve Bank Of St. Louis]( https://fred.stlouisfed.org/series/DSPIC96) and the stock prices data from [Yahoo Finance](https://finance.yahoo.com/). This sheet contains the following additional columns:

Column | Description
-------|------------
`indicator` | Name of the economic indicator
`category` | What that indicator helps measure
`current_zscore` | Number of standard deviations from the previous 2-year average for the current value of the indicator
`projected_zscore` | Number of standard deviations from the previous 2-year average for the projected value of the indicator on Election Day
`projected_hi` | Upper bound of an 80% confidence interval for `projected_zscore`
`projected_lo` | Lower bound of an 80% confidence interval for `projected_zscore`