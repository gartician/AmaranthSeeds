# Exploratory Data Aanalysis of Amaranth Seeds

Amaranth (莧菜) is a South American crop originally planted by the Aztecs, and is consumed around the world today. Its leaves are fibrous and filling, the plant itself is a prolific grower in hot and humid climates, and amazingly each plant generates a staggering number of seeds about the size of the period at the end of this sentence. In fact, one plant can produce thousands of potent seeds; in other words, **one plant can seed acres of land.** It is also one of my favorite plants because its leaves are great for soup, its seeds are nutritious and tastes like popcorn, and it's a beautiful purple-pink, unwieldy, lavish mess of a plant to witness in person. In this project, I want to observe physical properties (width, height, volume, mass) of amaranth seeds, and amount of seeds produced per plant. I will be using tools of data science like R and basic statistics to supplement my observations.

# Method: Harvesting the Seeds

Harvesting amaranth seeds is not difficult, but it was time consuming (1.5 hrs) because we are looking to maximize yield. I isolated about 120 grams of the flowering structure from the plant, collect everything into a bag or a box, and then pinch + pull the seeds from the branch, then rub intensely with the thumb and other fingers separate the seed from its flower. This process takes the longest time because there are lots of branches and flowers! 
Once this is done, the mixture is sifted through a fine filter. We won't be biasing our results for seeds that go through this filter because > 95% of the seeds can pass through this filter. Although this step is shorter, it is the step where seeds can get lost and scattered if you're being impatient. The result is a mixture of seeds plus impurities from the flower petals. Since the flower petals are much lighter (and purplier) than the seeds, we purify the seeds by collecting them into a bowl, and gently blow on the seeds while one hand is cupped under the bowl and makes a swirling motion (as if mixing a very, very large glass of wine). To improve the confetti-like experience, wearing sunglasses in this step will protect the eyes from scattering petals and enhance the confusion factor to strangers passing by. Successful execution of these steps will result in very pure, high yield of amaranth seeds.

# Method: Seed Measurement
To estimate the approximately [spheroid](https://en.wikipedia.org/wiki/Spheroid) shape of amaranth seeds, the height and width must be experimentally determined. However, it would be too time-consuming to measure both axes because they are too small to physically rotate, manipulate, and measure, manually. To approximate seed volume, the height axis will be measured, and the width will be 1.5-fold times the height. Seeds were randomly selected out of a bag, measured, and then placed back, to yield 20 observations. To get a better estimation of the average size and standard deviation of amaranth seeds in this year's crop (aka the population, we will bootstrap the sample (n = 20, 10K iterations), take the average and stdev per bootstrap sample, and calculate / visualize mean and sd of amaranth seeds.

# Results: Average Size of Amaranth Seeds I - Physical Properties
  
# Results: Average Size of Amaranth Seeds II - Seed Production
n_g seeds / 4 plants = rate of m_g seeds / plant.

# Results: Yield Calculations
  Assuming 150g of amaranth branches were collected, we get Vcontainer / Vseed = n_seeds.
  n_g seeds / 150g biomass = rate of m_g seeds / g biomass.
  
# Bonus: Exploring Principal Component Analysis

Here we compare the size of amaranth seeds compared to other object like an apple, an orange, a rock, a cantaloupe, and a watermelon. Since we have a large volume of multi-dimensional data (100k rows x width, height, volume, and mass columns), we would like to capture all the variables but visualize (or visually summarize) them in lower-dimensional space that we can see. One way is to use principal component analysis.
Imagine separating the objects on a one-dimensional line by width only. Amaranth seeds would lie to the lower end, the apple, orange, and rock lies in the middle, and cantaloupe and watermelon on the higher end. Plotting by width *and* mass would separate the apple, orange, and rock, since the rock is heavier than the fruits. 

# Conclusions
Amaranth seeds are indeed tiny!
