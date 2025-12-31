TABLEAU DASHBOARD & DATA STORYTELLING – ANALYZING AUTO MPG TRENDS -
(Regression analysis to study how engine factors like horsepower, weight, cylinders, etc affect MPG using the Auto MPG dataset. Includes report, visuals, and Tableau dashboard.)

In this project, I used Tableau to explore and visualize key patterns in the Auto MPG dataset. I created interactive dashboards that highlight relationships between engine characteristics and fuel efficiency, enabling users to intuitively explore data trends and insights. 

<img width="1218" height="984" alt="image" src="https://github.com/user-attachments/assets/97c59aa1-d714-448b-9081-be559999f1e0" />


Let's have a step by step look at my analysis using Tableau -

1) Define the goal
I analyzed how engine-related factors (horsepower, weight, displacement, cylinders, model year, origin) impact MPG (fuel efficiency).

2) Load the dataset in R
Imported the Auto MPG dataset (398 rows, 9 columns) into R / RStudio for analysis.

3) Clean the data (important step)
The horsepower column had missing values shown as “?”.
I converted horsepower to numeric and replaced missing values using the median (to reduce the effect of outliers).

4) Explore the data in R (EDA)
Created quick visuals and summary statistics to understand patterns:

MPG vs Horsepower (negative relationship)
<img width="1298" height="891" alt="image" src="https://github.com/user-attachments/assets/fa7bf058-2f61-4186-a9f1-d12a2508d772" />

MPG vs Weight (strong negative relationship)
<img width="1362" height="918" alt="image" src="https://github.com/user-attachments/assets/2663b83b-f986-48d5-b12d-48cf90310f30" />

MPG by Cylinders (fewer cylinders → higher MPG)
<img width="1334" height="889" alt="image" src="https://github.com/user-attachments/assets/7e71a333-1430-476b-b221-2128eedfb173" />

5) Build regression models in R
Simple linear regression: MPG predicted using horsepower.
Multiple linear regression: MPG predicted using multiple features (cylinders, displacement, horsepower, weight, acceleration, model year, origin).

Residual Plot using R studio
<img width="1368" height="921" alt="image" src="https://github.com/user-attachments/assets/08587e51-e1d2-4e3a-b48a-7a34a4ba037e" />

Histogram of Residuals using R studio
<img width="1378" height="930" alt="image" src="https://github.com/user-attachments/assets/f8341135-3a83-43ec-b5a0-5f08abec372c" />

6) Validate the model
Split data into training (300 rows) and testing (98 rows).
Evaluated performance using RMSE and MAE to check prediction accuracy on new/unseen data.

7) Export cleaned data for Tableau
After cleaning in R, I prepared/exported the dataset so Tableau could read it smoothly (clean numeric horsepower, consistent fields).

8) Build Tableau visualizations
In Tableau, I created clear visuals to communicate the relationships:

Scatter Plot: MPG vs Horsepower
This plot shows a negative correlation between engine horsepower and miles per gallon (MPG). As horsepower increases, MPG tends to decrease. This trend suggests that vehicles with more powerful engines are generally less fuel-efficient. This is intuitive, as stronger engines often consume more fuel to deliver higher performance.
<img width="774" height="939" alt="image" src="https://github.com/user-attachments/assets/3566bb19-1a0a-42e5-b98a-1ef8f92365bb" />

Scatter Plot: MPG vs Weight
The second plot reveals a strong negative correlation between a vehicle’s weight and its fuel efficiency. Heavier cars typically consume more fuel, leading to lower MPG. The relationship is more pronounced compared to horsepower, emphasizing the impact of vehicle mass on fuel consumption.
<img width="772" height="914" alt="image" src="https://github.com/user-attachments/assets/7630d99e-560c-4562-ae39-3090dad317a9" />

Scatter Plot: MPG vs Displacement
The third scatter plot also suggests a negative relationship between engine displacement and MPG. Displacement refers to the total volume of all engine cylinders, and larger displacement typically means higher fuel consumption. This plot indicates that cars with larger engines tend to have lower fuel efficiency.
<img width="786" height="927" alt="image" src="https://github.com/user-attachments/assets/5285d0cb-37dd-42e4-a62d-28fe9ef60e20" />

Scatter Plot: MPG vs Model Year
Unlike the others, this plot shows a positive correlation between model year and MPG. Newer cars tend to be more fuel-efficient, which aligns with industry trends toward better technology, stricter fuel standards, and increased consumer demand for efficiency. The gradual increase over time confirms that MPG has improved over the years.
<img width="770" height="914" alt="image" src="https://github.com/user-attachments/assets/61fe0787-44ca-454d-b0da-f7686ebb4e22" />

Hence, our visualizations reveal that horsepower, weight, and displacement are negatively correlated with MPG, while newer model years tend to have higher MPG. These insights confirm that lighter, less powerful, and newer cars are generally more fuel-efficient.

9) Create a Tableau dashboard (final deliverable)
Combined the visualizations into an interactive dashboard so viewers can understand the key drivers of MPG at a glance.

DASHBOARD - Analyzing Automobile Engine Impact on MPG 
<img width="1218" height="984" alt="image" src="https://github.com/user-attachments/assets/28608bfa-ce6f-4012-a603-84df87da3450" />


10) Final insights (what Tableau helped communicate)
Weight and horsepower are the strongest negative predictors of MPG.
Newer model years and non-US origins (Europe/Japan) tend to have better MPG.

***********************************************************************************************************

**CONCLUSION -**
Successfully built and validated linear regression models to predict MPG.
Multiple regression provides better explanatory power than simple regression.
Key drivers of MPG: Low weight, low horsepower, recent model years, non-US origin.
Limitations: Some residuals indicate potential outliers; model could be enhanced with nonlinear methods.
Visual: Image of a fuel-efficient car or a checkmark icon.

**RECOMMENDATION -**
Manufacturers: Focus on reducing vehicle weight and optimizing horsepower.
Consumers: Prioritize cars from Japan/Europe or newer models for better MPG.
Future Work: Explore nonlinear models, additional features, or larger datasets.
