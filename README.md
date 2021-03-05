# forecast_HIV_infections
Regression Models to forecast HIV infections



To start, we plotted each numerical column against HIV incidence. We wanted to see if there were any indicators that were obviously not linear relationships that we could remove off the bat. We also removed an outlier from the HIV incidence column that was severely skewing our data. Due to IV drug use, there was a huge outbreak in Scott County, Indiana. The value of HIV incidence here was 767. We added two columns that were insurance information to our main dataframe. 

<img src = "https://github.com/vmccready/forecast_HIV_infections/blob/main/images/linear-relation1.png" width="600" height="450" > 

This is a portion of our columns. With these visualizations we decided to remove the columns num_SSPS, Med_AMAT_fac, and AMAT_fac. We can see that AMAT_fac has a couple vertical lines, and there is no linear relationship here. 

<img src = "https://github.com/vmccready/forecast_HIV_infections/blob/main/images/residuals.png" width = "600" height = "450"> 

After making a residual plot, we saw that as the predicted y value went up, our error increased. This didn't seem like a
good model so we decided to look at the log relationship between our remaining columns and HIV incidence.
Using cross validation, we had 10 different folds. 
Our MSE's were [36.07326178167476, 54.39551418062765, 43.632470317828556, 50.25402972285556, 33.05529189092128, 55.30357581323924, 43.704994077342, 37.2715979330248, 24.630613510839833, 76.55200315756804]
with an average of 45.38238000396442 

<img src = "https://github.com/vmccready/forecast_HIV_infections/blob/main/images/log-relation.png" width = "600" height = "450" > 


This visualization revealed that a lot of the columns we had origianlly kept did not have linear relations. We dropped a majority of our columns and decided to keep the following columns: 
HIVdiag, diagpreva, drugdeathrate, population, plHIV, drugdep, adultmen, msm12mth, msm5yr, bup_phys, STATEABBREVIATION
HIVprevalence, drugdeathrate, drugdeaths, unemployment_rate, poverty_rate, Uninsured Males, household_income (edited) 






