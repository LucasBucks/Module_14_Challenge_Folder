# Module_14_Challenge_Folder
Module 14 Challenge

Baseline Anaylsis:

Our baseline model does a pretty great job of modeling the data and then outperforming the actual results. The model performs well in a "Long" scenario or better said when "1" is the predicted return.  This is backed up by the plot showing outperformance during up market scenarios ("Buy" scenarios") and the recall grading out to .96.  The model underperforms quite a bit to actual returns when "Short" scenarios (When our predicted return is -1).  This is confirmed by showing steeper declines in the plot and a recall of .04.  Thankfully, the "Longs" were more prevalent that the "Short" scenarios during this time frame.  This could be the impact of the training time fram happening during a more positive market environment vs. negative (2288 instances of a 1 vs 1804 for -1).

![alt text](https://github.com/LucasBucks/Module_14_Challenge_Folder/blob/main/Module_14_Challenge/baseline_plot.png)

                  precision    recall  f1-score   support

        -1.0       0.43      0.04      0.07      1804
         1.0       0.56      0.96      0.71      2288

    accuracy   
                                        0.55      4092
                                        
   macro avg       0.49      0.50      0.39      4092
   
weighted avg       0.50      0.55      0.43      4092


Linear Regression Analysis:  

The results for the Linear Regression analysis are quite mixed and inconclusive.  When looking at the plot, the linear regression starts off with underperformance relative to the actual returns.  This is a "Short" market scenario in which the market is on a decline.  When the market turns to a "long" scenario, the model has quite impressive outperromance until the next "Short" Scenario where it underperforms again.  When the situation calls for a "long" environment again, the outperformance returns and then all of a sudden, the model stops working and falls apart.  The linear regression back test visualization chart would lead me to believe this is not a reliable model to use for our data.  It's too volatile and lowers our overall recall score for the Long position.  It does have better numbers on the Short position but it is too unpredictable to be relied upon.

![alt text](https://github.com/LucasBucks/Module_14_Challenge_Folder/blob/main/Module_14_Challenge/linear_reg_plot.png)

                  precision    recall  f1-score   support

        -1.0       0.44      0.33      0.38      1804
         1.0       0.56      0.66      0.61      2288

    accuracy                           0.52      4092
    
   macro avg       0.50      0.50      0.49      4092
   
weighted avg       0.51      0.52      0.51      4092
