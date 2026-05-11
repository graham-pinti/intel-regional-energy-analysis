# Intel Data Center Site Selection: U.S. Regional Energy Analysis

**[View Interactive Dashboard on Tableau Public]([https://public.tableau.com/app/profile/graham.pinti/viz/G_PintiIntelRegionalEnergyAnalysisDashboardPublic/Dashboard?publish=yes])**

Built for Intel's Sustainability Team as part of the Global Career Accelerator 
Data Science Track at the University of Vermont. Intel is planning a new data 
center and needs to select the optimal U.S. region based on three core energy 
requirements: reliable supply, affordability, and around-the-clock renewable 
availability. This project works through those requirements systematically, 
starting with 13 candidate regions and narrowing to a single data-driven 
recommendation.

> **Data Source:** U.S. Energy Information Administration (EIA) | 
> Period: December 2021 – January 2023 | Two datasets: energy_dataset 
> and energy_data_by_source covering 13 U.S. regions.

## The Analytical Story

Choosing a data center location is not a single question. It is a filtering 
process. Each requirement eliminates candidates until only the strongest 
option remains.

**Filter 1: Who actually produces enough energy?**
Not every region generates more power than it consumes. Regions that import 
energy are dependent on outside suppliers, which introduces price volatility 
and supply risk. Of 13 regions analyzed, only 5 operate as net energy 
producers: Mid-Atlantic, Northwest, Southwest, Central, and Southeast, in 
descending order of surplus. The remaining 8 regions are net importers and 
were eliminated from consideration.

**Filter 2: Who relies on renewable energy?**
Intel has sustainability commitments that require a meaningful renewable energy 
presence at its facilities. Of the 5 net producing regions, two stood out as 
leaders in renewable energy percentage: Northwest at 44% and Central at 38%. 
Both qualify on supply reliability and sustainability criteria simultaneously, 
making them the two serious contenders.

**Filter 3: Is the renewable source stable around the clock?**
A data center runs 24 hours a day, 7 days a week. Wind and solar generation 
are time-dependent, peaking at certain hours and dropping at others. Analysis 
of California wind generation confirms this pattern, with percent difference 
above zero only between 12PM and 10PM, peaking at 3PM. Hydropower generates 
continuously regardless of time of day or weather. The Central region's 
renewable profile is dominated by wind. The Northwest's is dominated by 
hydropower and pumped storage, which maintains consistently high output 
across all 24 hours. For a facility that cannot tolerate generation gaps, 
this distinction is decisive.

**The Recommendation**
The Northwest is the only region that simultaneously leads in energy surplus, 
renewable percentage, and around-the-clock source stability. The data does 
not just support this recommendation. It points to it through a systematic 
elimination of every other candidate.

## Areas of Analysis

- Net energy production surplus or deficit across all 13 U.S. regions
- Supply and demand stability over time with dynamic period filtering
- Renewable energy percentage by region and dominant source composition
- Intraday generation patterns and hourly variability by energy source
- Energy source breakdown by region using tree map visualization

## Dashboard Structure

Built in Tableau with 7 analytical views and one interactive summary dashboard:

- **Summary Dashboard** — Interactive view combining Net Production, Renewable 
Energy Percentage, and Energy Source by Region with dropdown controls
- **Net Production** — Sorted bar chart of net energy surplus or deficit 
by region across all 13 regions, identifying the 5 viable candidate regions
- **Renewable Energy** — Sorted bar chart of renewable energy as a percentage 
of total generation by region, narrowing candidates to Northwest and Central
- **Utility Power Source Breakdown** — Tree map of energy source composition 
by region and balancing authority, revealing what those renewables actually are
- **Renewable Generation by Hour of Day** — Intraday comparison of CAL vs. NW 
renewable output across all 24 hours, confirming Northwest's around-the-clock 
stability
- **Supply and Demand by Region** — Dual axis line chart of demand vs. net 
generation over time with dynamic day/week/month period parameter and 
regional dropdown filter
- **Energy Source by Region** — Multi-source line chart colored by energy 
type with regional and period filters
- **Hourly Difference in Generation** — Line chart of percent difference in 
energy generation from the previous hour, filtered to California wind energy

## Site Recommendation: Northwest Region

Based on the full analysis, the Northwest region is the recommended location 
for Intel's next data center for three converging reasons.

First, the Northwest is one of five net energy producing regions, ensuring a 
reliable surplus that supports stable pricing and reduces the risk of shortfalls 
during peak demand periods.

Second, the Northwest leads all thirteen regions in renewable energy percentage, 
with hydropower and pumped storage as its dominant source. Unlike solar or wind, 
hydropower generates consistently across all hours of the day, making it 
particularly well-suited to the around-the-clock energy demands of a data center. 
This directly supports Intel's sustainability commitments without sacrificing 
reliability.

Third, supply and demand patterns in the Northwest show stable and predictable 
generation across the analyzed period, minimizing operational risk associated 
with energy price volatility or supply interruptions.

Among all regions analyzed, the Northwest is the only one that simultaneously 
leads in energy surplus, renewable percentage, source stability, and intraday 
consistency, making it the strongest candidate for a facility of this scale 
and strategic importance.

## Key Terms

- **Net Production** — Net Generation minus Demand. Positive values indicate 
a surplus; negative values indicate a deficit
- **Renewable Energy** — Defined in this analysis as wind, solar, and 
hydropower and pumped storage combined
- **Percent Difference** — Change in energy generation compared to the 
previous hour, used to identify intraday generation trends
- **Region Abbreviations:** NW (Northwest), CENT (Central), CAL (California), 
TEX (Texas), NY (New York), MIDW (Midwest), SW (Southwest), TEN (Tennessee), 
NE (Northeast), SE (Southeast), MIDA (Mid-Atlantic), CAR (Central America Region)

## Tools Used

Tableau Desktop — calculated fields, dual axis charts, tree maps, parameters, 
dynamic filters, interactive dashboard with actions

## Data Source

U.S. Energy Information Administration (EIA) — Regional hourly energy 
generation and demand data, December 2021 – January 2023
