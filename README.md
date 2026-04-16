# Data-Scientist-Assignment
Weather forecasts are systematically biased. A forecast model might consistently over-predict wind speed in valleys and under-predict it on ridgelines. The task of the project is to build a model that learns and corrects this bias.

**Step 1:** Pick 10 locations across different terrain types (coastal, mountain, plains, desert, tropical). We have picked 2 locations for each terrain, because selection in this manner maintains the symmetry which eases to reach to conclusion with more accuracy.

**Step 2:**  Fetch hourly data for each location: wind speed (m/s) and wind direction from both APIs, for the period 1 January 2025 to 31 December 2025.

**Step 3:** Split the data: January through October for training. November and December are your held-out test set.

**Step 4:** We have used gradient boosting approach for building a correction model. Because of it's ability to capture complex non-linear relationships between forecast errors and input features such as terrain type, time, and wind direction, and weather systems are inherently non-linear. So, simpler models like linear regression may fail. Whereas complex models like neural networks requires large computation.

**Step 5:** The correction model reduced RMSE from 1.12 to 0.82, indicating improved prediction accuracy.  The bias and MAE also decreased, confirming consistent improvement across predictions.

<ins>**ANALYSIS**</ins><br>
The forecast bias shows clear dependence on terrain type. For example, desert regions(-0.4) exhibit higher bias compared to plains(0.3)<br>
The forecast bias varies with time of day and season. Hourly analysis shows different bias patterns during daytime(negative bias) and nighttime(positive bias)
