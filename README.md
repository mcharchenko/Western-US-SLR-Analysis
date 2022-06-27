# Western-US-SLR-Analysis
A research project analyzing 5 years of snowfall data at Western United States ski resorts to calculate the snow to liquid ratio for each snowfall event.

The snow to liquid ratio (SLR) can be used to describe multiple accumulated snow depth properties such as water content and snow crystal density. These properties can be applied to a wide range of winter operations from recreational skiers looking for fresh dry powder or to how different snow layers bond to each other and its impacts on avalanche dangers for backcountry recreationalists.

By analyzing this simple ratio at sites across the major mountain ranges in the Western US, we can provide a numerical representation of snow properties between different regions. In doing so, we can create snow ratio climate norms and illustrate how climate impacts snow properties throughout the mountains of the Western US. 

## About This Repository:
This repo contains 5 .csv files of winter season snowfall data between October 1st 2015 to April 30th 2020 from the Global Historical Climatology Network (GHCN-D) at 6 western US ski resorts. These sites are split into 3 geographical regions, the coastal region (Mt. Hood OR and Tahoe City CA), the Intermountain West (Alta UT and Jackson WY), and the Continental region (Steamboat Springs CO and Vail CO).

The main jupyter notebook then imports these CSV's into Pandas dataframes where the data is pre-processed for analysis by removing days where no snow was observed, remove days with missing data, converting temperatures to celsius, and calculating the average daily temperatures. 

The observational data used rarely has the equipment to observe specific weather conditions such as whether precipitation is falling as rain, snow, or a mixture of rain/snow/ice pellets, and is often located in areas with sparse ground observations. Due to this, snowfall events where the average temperature was above 0 °C were not included in the scope of analysis and therefore dropped from the dataframes to limit data to events that one could resonably determine fell only as snowfall.

The snow to liquid ratio (SLR) is then calculated for all of the remaining data by dividing the observed daily snowfall depth accumulation by the observed daily liquid water depth. 

The original scope of this project was to challenge the common claim by ski resorts that their best powder days occur on the days where they have recieved the heaviest snowfall. So the analysis was limited to snowfall events above the mean snowfall for the region in order to focus on the heavier snowfall events. 

The subsetted data was then plotted using a scatter plot, and a simple linear regression was then calculated and plotted to visualized the trend of the snow ratio with heavier snowfall events.

While the initial goal was just to use this data to determine whether the common ski resort claim that their heaviest snows are their best for skiers, I realized that the results of the calculations also had impacts on avalanche risk, weather forecasting guidance, and how snow properties may shift in a changing climate. 

Future goals include adding more observational sites and additional years of data to the study along with potentially creating a basic predicitive model of how snow ratios and in turn snow properties will shift as our climate changes.
