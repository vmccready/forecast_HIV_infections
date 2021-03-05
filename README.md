# forecast_HIV_infections
Regression Models to forecast HIV infections



To start, we plotted each numerical column against HIV incidence. We wanted to see if there were any indicators that were obviously not linear relationships that we could remove off the bat. We also removed an outlier from the HIV incidence column that was severely skewing our data. Due to IV drug use, there was a huge outbreak in Scott County, Indiana. The value of HIV incidence here was 767. We added two columns that were insurance information to our main dataframe. 

<img src = "https://github.com/vmccready/forecast_HIV_infections/blob/main/images/linear-relation1.png" width="600" height="450" > 

This is a portion of our columns. With these visualizations we decided to remove the columns num_SSPS, Med_AMAT_fac, and AMAT_fac. We can see that AMAT_fac has a couple vertical lines, and there is no linear relationship here. 

