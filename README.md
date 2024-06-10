# Data-Science-A-B-Tesing

## Designing Eniac's A/B Test
Welcome to the designing Eniac's A/B Test Project! This project focuses on evaluating and enhancing the user experience on Eniac’s website to increase conversions, to increase the **iPhone 13** sales.

### Project Overview
A common challenge of internet companies is to increase conversions through a better User Interface (an appealing design) and User Experience (intuitive and usable interactions). This is initially a task for the Design team, but once visitors start to flow, purchases begin to happen and designers are out of improvement ideas, it is time for the Data Analytics team to step in and support improvements through rigorous experimentation.

### Skills & Tools
1. Data Collection & Cleaning
2. Hypothesis Testing
3. A/B Testing
4. Chi-Square Testing

### Challenge:
To test all four versions of the button(SHOP NOW)

### User's Path
The steps needed for a user to purchase the iPhone 13 are the following:
1. Visit Eniac’s site.
2. Click on the “SHOP NOW” button in the iPhone banner.
3. Click on the model to purchase (13, 13 Pro, 13 Pro Max…).
4. Add the product to the shopping basket.
5. Go to the “Check-out” page.
6. Add the delivery details.
7. Add the payment details.
8. Confirm the purchase.

### Eniac's Conversion Funnel:
In one week Eniac attracted very substantial web traffic (50.000 visits). However, only a very small portion of these visitors went down the funnel, with 30 iPhone sales confirmed.

![Eniac's Conversion Funnel](https://github.com/PriyankaSPawar/Data-Science-A-B-Tesing/assets/168557945/174e3678-2865-49c7-975b-2742c15207e3)

### Conversion Rates
Here it becomes clearer where in the funnel is Eniac losing the most potential buyers: 
1. The “SHOP NOW” button, at the top of the funnel, only has a 2% conversion rate.
2. The rest of the steps perform at more than 30%.

### CTR:
With the goal of increasing the conversion rate of the “SHOP NOW” button (when a conversion is a “click”, abbreviated CTR),Marketing has asked the Design team for a redesign of the button, which results in new 3 different versions as follows:
- Version A: the original site.
- Version B: the SHOP NOW button is now red.
- Version C: the SHOP NOW button has a new text, “SEE DEALS”
- Version D: both the B and the C changes to the button have been applied.

![image](https://github.com/PriyankaSPawar/Data-Science-A-B-Tesing/assets/168557945/8b01e09a-a6a8-410b-a20d-4e621b97865d)

### Experimental Design Questions:
When designing the experiment, several questions can arise:
1. How many different versions should be tested?
2. What kind of changes can we implement in each version of the test (from changing just the colour of a button to redesigning the whole site)?
3. How can we show one version to a selected group of users and another version to a different group?
4. Which metric should we choose to compare the different versions?
5. Should Eniac experiment with other elements of the site instead (or in addition to) the “SHOP NOW” button?
6. How can we track, store and analyze the data from each version?
7. How can we ever be sure that the version with the best performance does not have more clicks due to just chance?
8. How long can we expect the experiment to last?

### Metrics to perform the Test:

- The decision was reached to test all four versions of the button:
  - White “SHOP NOW”
  - Red “SHOP NOW”
  - White “SEE DEALS”
  - Red “SEE DEALS”
    
- The metrics that were deemed relevant enough to be tracked were the following:
  1. **Click-through rate (CTR)** for the homepage. Amount of clicks on the button divided by the total visits to the page. Selected as a measure of the initial ability of a website element to lead users to interact with it.
  2. **Drop-off rate for the linked page** This metric represents the percentage of visitors who initiate a conversion process (such as a purchase or sign-up) but do not complete it. It serves as an indicator of how engaged users remain at any point in the conversion process.
  3. **Homepage-return rate for the category pages**
  4. The hypotheses to be tested in the experiment are the following:
  - Null Hypothesis: all versions have the same CTR.
  - Alternative Hypothesis: there is a difference in the CTR for the different versions.
       
- While all the metrics will be relevant for the decision-making process, it was decided that for a version to be considered superior, there must be statistical significance in the click-through rate.
- A typical statistical significance of 95% was chosen. Minimum detectable effect was set to 20%, it having been determined that even a small increase in the conversion pipeline would cover the costs of a small change to the website.

### Experiment & Analysis:

![image](https://github.com/PriyankaSPawar/Data-Science-A-B-Tesing/assets/168557945/c5f61b5b-4910-4a29-a938-000c7f2e76c0)
It seems like the red variations are the worst performers, while the white buttons perform much better. But, are those differences due to chance? This is what we are going to test:

**Null Hypothesis**: The 4 versions of the button are equally likely to receive clicks, and the observed differences are due to chance.
**Alternative Hypothesis**: The observed differences are not due to chance: there is at least one version that got so many more/much less clicks than the others that this can hardly be explained just by chance (i.e. they have a better/worse CTR, a better/worse performance).

Since we were only interested in people clicking on that single element, here the counts on “Click” are the clicks on that element and “No-click” is simply calculated as visits - clicks

![image](https://github.com/PriyankaSPawar/Data-Science-A-B-Tesing/assets/168557945/f4ca1c66-740c-4258-9527-a05b3e6181a8)

This is how data has been shaped so that we have performed a chi-square test using the **chi2_contingency** function from **scipy**, and finally saw whether the results are significant. 

### Final Results :

![image](https://github.com/PriyankaSPawar/Data-Science-A-B-Tesing/assets/168557945/4b57df51-d509-4d37-abb0-adde2493f863)

Analysing the heatmap above , The version with the highest click-through rate, **Version_C**, exhibits a statistically significant difference when compared Versions B and D, but not to Version_A, which possesses the second-highest click-through rate. As a result, declaring a clear winner based on post hoc tests becomes challenging, therefore we can only say that both Version_C and Version_A are the winners.

However, if a definitive winner is required, additional steps need to be implemented. This is where we transition from the realm of statistics to the business world. The following actions can help in determining the version to be featured on the website in the future:
- Consider other metrics alongside click-through rate.
- Incorporate qualitative research findings.
- Seek input from subject-matter experts.
- Redesign the experiment and conduct it once more.

### Conclusion :

By performing this project, I have learnt how to perform A/B Testing with several testing methods and how to interpret the results efficiently. To perform the testing we should take care of cleaned and formatted data. Even when the significant statistics are not clear, taking into consideration that other metrics are implicated as well. These additional insights can provide a more comprehensive understanding of user behavior and guide better decision-making for future optimizations.






