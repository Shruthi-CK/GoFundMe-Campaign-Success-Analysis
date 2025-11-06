# GoFundMe-Campaign-Success-Analysis

This project analyzes 1,000 GoFundMe "Animal" category campaigns to identify the visual and temporal factors that drive fundraising success.

### Part 1: Data Collection

* **Task A:** A Python scraper (using Selenium and BeautifulSoup) was built to gather 1,000 campaign links, collecting data on the amount raised, campaign duration, and text descriptions.
* **Task B:** The primary image from each campaign was processed using the Google Vision API to extract descriptive content labels (e.g., "Dog," "Cat," "Shelter").

### Part 2: Predictive Modeling

* **Task C:** A binary target variable was engineered to classify campaigns as "high-earning" (1) or "low-earning" (0) based on the median amount raised ($689.50).
* **Task D:** Multiple logistic regression models were trained to predict this target. The analysis compared the predictive power of image labels, text descriptions, and campaign duration. The model combining **text descriptions and duration** achieved the highest accuracy (70.5%), proving that campaign length is a critical predictor.

### Part 3: Topic Modeling & Insights

* **Task E:** Latent Dirichlet Allocation (LDA) topic modeling was performed on the image labels to identify 7 distinct visual themes (e.g., "Dogs," "Cats," "Shelter Scenes," "Facial Expressions").
* The topic weights were compared between the highest and lowest fundraising quartiles.
* **Task F:** The analysis revealed that campaigns featuring **dogs** (+10.0% difference) and **positive facial expressions** (+1.5%) were significantly more common in the top quartile. Campaigns featuring **cats** (–8.3%) were more common in the bottom quartile. Actionable insights are provided for non-profits to optimize their visual strategy.
