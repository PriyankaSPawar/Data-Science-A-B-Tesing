# Data-Science-A-B-Tesing

## Designing Eniac's A/B Test
Welcome to the designing Eniac's A/B Test Project! This project focuses on evaluating and enhancing the user experience on Eniac’s website to increase conversions, to increase the **iPhone 13** sales.

### Project Overview
A common challenge of internet companies is to increase conversions through a better User Interface (an appealing design) and User Experience (intuitive and usable interactions). This is initially a task for the Design team, but once visitors start to flow, purchases begin to happen and designers are out of improvement ideas, it is time for the Data Analytics team to step in and support improvements through rigorous experimentation.

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


