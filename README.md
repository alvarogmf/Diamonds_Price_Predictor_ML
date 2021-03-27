# Diamonds Price Predictor 
## _“Remember diamonds are created under pressure so hold on, it be your time to shine soon.”_ - Sope Agbelusi

<p align="left"><img src="https://cdn-images-1.medium.com/max/184/1*2GDcaeYIx_bQAZLxWM4PsQ@2x.png" width="80"></p>
___________________________

**Owner**: Alvaro Gil

**Bootcamp**: Ironhack - Data Analytics Part Time Nov 2020

## Overview
This is the second project of two. In this last one, we have taken the same Diamonds dataset as before, and trained a model through Machine Learning to be able to estimate the price of Diamonds according to their characteristics (color, carats, cut, dimensions...)

- EXPLORATORY DATA ANALYSIS:
- - There are some Zero values in Columns x, y, z and some outliers in y and z.
- - Regarding correlation, Depth and Table are the only that don't have any correlation with Price (-0.014864 and 0.130111 respectively). The rest of the features have a very high and possitive correlation with Price.
- - Carats doesn't have a normalized distribution.
- DATA ENGINEERING:
- - I eliminated all the rows with one of the values x, y or z as 0.
- - I eliminated all the outliers (values above 10 for y and 6 for z).
- - Used a logaritmic transformation for the Carat column, to use have it normalized.
- - New Features:
- - - Created a new column to calculate the volume of the diamond depending on x, y and z.
- - - Created a new column to calculate the ratio between x and y, all of them are around 1.
- - - Created a new column regarding the shape of the diamond based on Table and Depth. More information on this can be found [here](https://beyond4cs.com/grading/depth-and-table-values/).
- MODEL TRAINING:
- - Features used: carat, volume, ratio_xy, cut, color, clarity, shape
- - Scaler used: MinMaxScaler
- - Model Used: LGBMRegressor
- - grid_search.best_score_ = 512.7
