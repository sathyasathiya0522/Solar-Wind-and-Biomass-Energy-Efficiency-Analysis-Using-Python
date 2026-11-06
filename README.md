Solar, Wind and Biomass Energy Efficiency Analysis Using Python
Project Overview
This project analyses renewable-energy records for Solar, Wind and
Biomass using Python. It compares output efficiency, installation
cost, annual maintenance cost and dataset-supplied optimized output
across seven locations in India.

The project follows a data analytics workflow covering data inspection,
cleaning, feature engineering, exploratory data analysis (EDA),
statistical analysis and visualization.
Project Objectives
- Compare output efficiency across Solar, Wind and Biomass.
- Examine installation and annual maintenance costs.
- Compare dataset-supplied optimized output across energy sources.
- Explore efficiency differences across locations.
- Examine relationships between numerical variables.
- Create clear visualizations and derive data-supported insights.
Dataset Information
  Item                                Details
  Dataset                             Non-Conventional Energy Sources Optimizer

  Source                              Hugging Face Datasets

  Dataset page                        Non-Conventional Energy Sources
Optimizer

  Domain                              Renewable Energy

  Original size                       100,000 rows × 11 columns

  Final size                          100,000 rows × 15 columns

  Energy sources                      Solar, Wind, Biomass

  Locations                           Andhra Pradesh, Gujarat, Karnataka, Maharashtra, Rajasthan, Tamil Nadu, Telangana

  File format                         CSV
Environment                         Google Colab
Tools and Technologies
- Python -- programming and analysis
- Pandas -- data loading, cleaning, grouping and analysis
- NumPy -- numerical operations
- Matplotlib -- chart creation
- Seaborn -- statistical visualizations
- Google Colab -- notebook development and execution
Dataset Attributes
The original dataset contains these 11 attributes:

  Attribute                     Description
  source_type                 Renewable energy source: Solar, Wind or Biomass
location                    Location represented in the record
avg_temperature_c           Average temperature in °C
wind_speed_mps              Wind speed in metres per second
solar_radiation_kwh_m2      Solar radiation in kWh/m²
humidity_percent            Humidity percentage
altitude_m                  Altitude in metres
installation_cost_usd       Installation cost in USD
maintenance_cost_usd_year   Annual maintenance cost in USD
output_efficiency_percent   Output efficiency percentage
optimized_output_kw         Dataset-supplied optimized output in kW
Project Workflow
1. Data loading
2. Initial data inspection and EDA
3. Data cleaning and type validation
4. Feature engineering
5. Final EDA
6. Statistical analysis
7. Univariate analysis
8. Bivariate analysis
9. Multivariate analysis
10. Findings and conclusion
Data Cleaning and Preparation
The notebook checks dataset dimensions, data types, missing values,
duplicate records, descriptive statistics and category values.
- Missing values found: 0
- Duplicate rows found: 0
- No rows were removed for missing or duplicate values.
- source_type and location were converted to categorical data
  types.
- Numeric columns were validated and converted to numeric types where
  required.
Feature Engineering
Four additional features were created:
  Feature                             Formula / Purpose
  total_first_year_cost_usd         Installation cost + annual
maintenance cost

  optimized_output_per_1000_usd     Optimized output ÷ installation
cost × 1,000

  efficiency_band                   Project-defined groups: Low (≤60%),
Medium (>60% to 75%), High (>75%)
location_source                   Combined location and energy source
Final dataset: 100,000 rows × 15 columns, with 0 missing values and
0 duplicate rows.
Statistical Analysis
The project uses: - Mean, median and mode - Variance and standard
deviation - Skewness and kurtosis - Pearson correlation - IQR-based
outlier checking
Output Efficiency Summary
  Energy Source     Mean (%)   Median (%)   Mode (%)
  Biomass              67.47        67.43      89.00
Solar                67.53        67.71      45.78
Wind                 67.60        67.54      87.49
Key Statistical Findings
- Wind has the highest mean output efficiency at 67.60%, followed
  by Solar at 67.53% and Biomass at 67.47%.
- Standard deviations are similar: Biomass 15.88, Solar 15.92
  and Wind 15.84.
- Installation cost and output efficiency have a Pearson correlation
  of approximately -0.004, indicating almost no linear
  relationship in this dataset.
- Optimized output and optimized output per USD 1,000 have a positive
  correlation of approximately 0.71.
Exploratory Data Analysis and Visualizations
Univariate Analysis
1. Output Efficiency Comparison Across Energy Sources -- Boxplot
   Compares the distribution, median and mean output efficiency of the
   three energy sources.
2. Distribution of Average Temperature -- Histogram
   Examines the distribution of average temperature values.
3. Percentage Distribution of Records by Energy Source
   Compares the proportion of Solar, Wind and Biomass records.
4. Average Installation Cost by Energy Source
   Compares the average installation cost across the three sources.
Bivariate Analysis
5. Installation Cost vs Output Efficiency -- Hexbin Plot
   Explores the relationship between installation cost and output
   efficiency.
6. Mean vs Median Output Efficiency by Energy Source -- Lollipop
   Chart
   Compares mean and median efficiency for each source.
7. Correlation Heatmap of Numerical Features
   Summarizes the direction and strength of correlations among
   numerical variables.
Multivariate Analysis
8. Average Output Efficiency by Location and Energy Source --
   Heatmap
   Compares efficiency across seven locations and three energy sources.
9. Average Optimized Output by Energy Source -- Bar Chart
   Compares the dataset-supplied optimized output across the three
   sources.
10. Average Output Efficiency and First-Year Cost by Energy Source --
    Comparison Charts
    Compares average efficiency and first-year cost together.
Key Findings
- Average output efficiency is very similar across Solar, Wind and
  Biomass in this dataset.
- Wind has the highest average efficiency, but the difference from
  Solar and Biomass is small.
- Average installation and first-year costs are also close, with
  Biomass recording the highest average cost.
- Efficiency varies across locations and energy sources.
- Installation cost has almost no linear correlation with output
  efficiency in the supplied records.
- The dataset supports exploratory comparison; it does not by itself
  establish real-world technology superiority.
Business Insights
- Compare efficiency, installation cost and annual maintenance cost
  together rather than selecting a source using one metric.
- Use location-level results as an initial screening step, followed by
  local resource and engineering assessments.
- Validate the definition and units of optimized output before
  treating it as an estimate of actual electricity generation.
- Consider project lifetime, financing, tariffs, reliability and
  measured energy yield before making investment decisions.
Limitations
- The dataset does not contain a date or year field; therefore,
  time-series trend analysis is not included.
- optimized_output_kw is treated as a dataset-supplied optimized
  measure and is not independently verified actual generation.
- Correlation indicates association, not causation.
- Efficiency-band thresholds are project-defined for analysis and are
  not official industry standards.
- The results describe the supplied dataset and should not be treated
  as a complete technical feasibility or investment recommendation.
- No predictive machine-learning model is included in this project.
Conclusion
This project uses Python to inspect, clean, transform and analyse
renewable-energy data. Statistical summaries and visualizations compare
Solar, Wind and Biomass across efficiency, cost, optimized output and
location. The three sources show very similar average output efficiency
in the dataset. These findings provide an exploratory comparison and can
support further investigation with verified technical and financial
information.
How to Run the Project
1. Download or clone this repository.
2. Open Solar_Wind_Biomass_Energy_Analysis.ipynb in Google Colab or
   Jupyter Notebook.
3. Ensure the dataset CSV file is available at the path used in the
   notebook, or update the file path.
4. Run the notebook cells in order.
5. Review the generated tables, statistical results and visualizations.
Repository Structure
Solar-Wind-Biomass-Energy-Analysis/
│
├── Solar_Wind_Biomass_Energy_Analysis.ipynb
├── SORCE FILE.csv
├── Solar_Wind_Biomass_Energy_Efficiency_Project_Documentation.pdf
└── README.md
Author
Subramaniyam R
Data Analytics Project
Python | Pandas | NumPy | Matplotlib | Seaborn | Google Colab
