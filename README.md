# SurfsUp_Challenge

## Overview
The purpose is to use SQLite and SQLAlchemy to pull the data from the hawaii.sql file. Then to use that data to find the monthly weather summaries for December and June, and compare them to see which one would be the best month to sell ice cream.

## Results
* The mean for June is at 74.94F compared to December's which average temperature was 71.04F. So June was 3.9F hotter than Decemeber.
* The count is higher in June at 1700 while December had 1517
* Standard Deviation for both June and December is around 3 so that tells us there is little fluctuation in the results

![June_Temps](https://user-images.githubusercontent.com/108701073/187243730-08bbef6c-dd2f-4f8e-84b6-fe95d6a4cd7d.png)

![December_Temps](https://user-images.githubusercontent.com/108701073/187243699-e5b86bfc-b9ac-4cdd-b832-abad11e86458.png)

## Summary
From the results we can see that there isn't that much of a difference with June and December in temperature. So ice cream could be sold all year round, but June would most likely have slightly better results as it is a little bit hotter than December so more people would buy Ice cream in June. Another value that we could extract from the data to try and improve our results and understanding is the humidity. We can use the following queries to look

Jun = session.query(Measurement.date,Measurement.prcp,).filter(extract('month', Measurement.date) == 6).all()

Dec = session.query(Measurement.date,Measurement.prcp,).filter(extract('month', Measurement.date) == 12).all()
