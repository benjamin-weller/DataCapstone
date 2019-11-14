# Background

**You're a trader at RBC.** Using your economics background you think about your favorite restaurants that you've eaten at through out the city. Why did you like those restaurants, why not others? Was it that you really like their food; or is it that you like the neighborhood, that the existence of other options when you initial ate there lured you in and you had one single enjoyable experience? Your background tells you that more options is good, that it yields higher consumer surplus numbers, and that obviously a neighborhood with more options will yield better experiences for the people who eat there. **You think that neighborhoods with more restaurants will have higher satisfaction ratings.**

**Your psychology focused "performance coach" disagrees.** They believe that in tight urban dining districts the paradox of choice kicks in. In such situations they believe that often people will have a hard time picking someplace to eat, and when they do, they aren't as satisfied as they would be with a more paired down set of options. **Your performance coach thinks that neighborhoods with a smaller set of restaurants will ultimately have higher satisfaction numbers.**

## Observation

You have noticed that often you do enjoy grabbing a bite to eat for lunch at the shop down the corner, but you also have noticed that you more then once trek all the way across town to eat at your favorite restaurant tucked away in a rich suburb, why do you continue to do that? Is it just because you're more mindful about your choices when you have more free time?

## Question

Does the existence of a higher number of restaurants in a neighborhood have a discernable effect on the satisfaction customers have when eating at any one of them?

## Hypothesis/Prediction

Following your gut instincts (you are a successful stock trader after all) you believe that having more restaurant choices in a neighborhood will result in higher satisfaction at the establishments.

This problem lends itself to the data we can gather from Foursquare, and it would appear that a linear regression would be in order here, does the number of restaurants positively correlate with higher average satisfaction scores?

## Data/Analysis

To gather the data a few steps need to be taken.

1. Gather all restaurants in the post code, this is done in a rough manner, with an arbitrarily large radius value.
2. Remove duplicates (the rough data collection above needs to be smoothed over).
3. Remove entries that don't represent restaurants (this step removes about 50% of data points in the list).
4. Gather the remaining list of data ~1000 individual entries.
   1. The data that was gathered for each of the entries is the number of likes, and the total number of restaurants in that post code.
5. Oftentimes data scientists tend to over-complicate things. A simple linear regression works in most cases, as such I analyzed my data fitting a linear regression and then examining a R2 score.

## Results

It would appear that the results are fairly conclusive. It can be said that the total number of restaurants in a post code will result in ~60% of the variation in the average number of likes for a restaurant in that post code. While there is a significant cluster of points at the low end (~0,~0), but I believe that the trend line is clear that there is a correlation. While there is a correlation I wouldn't say it's very strong, I believe that there is more variable data that would have to be taken in to account to reach a stronger correlation.

## Conclusions

It can be said that the data supports the hypothesis that more restaurants in a post code does indeed correlate with a higher amount of average likes in that post code. You (our RBC stock trader) can now gently nudge your performance coach (gently because there's still ~40% of the variation that needs to be accounted for), feel free to let your coach know that sometimes the "sullen science" (economics) will trump the mind (psychology).