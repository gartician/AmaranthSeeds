# Exploratory Data Aanalysis of Amaranth Seeds

Amaranth (莧菜) is a South American crop originally planted by the Aztecs, and is consumed around the world today. Its leaves are fibrous and filling, the plant itself is a prolific grower in hot and humid climates, and amazingly each plant generates a staggering number of seeds about the size of the period at the end of this sentence. In fact, one plant can produce thousands of potent seeds; in other words, **one plant can seed an acre of land.** It is also one of my favorite plants because its leaves are great for soup, its seeds are nutritious and tastes like popcorn, and it's a beautiful purple-pink, unwieldy, lavish mess of a plant to witness in person. In this project, I want to observe physical properties (width, height, volume, mass) of amaranth seeds, and amount of seeds produced per plant. I will be using tools of data science like R and basic statistics to supplement my observations.

# Method: Harvesting the Seeds

Harvesting amaranth seeds is not difficult, but it was time consuming (1.5 hrs) because to maximize yield. About 100 grams of the flowering structure were harvested and placed into a bag. To separate the seeds from its flower, firmly pinch, rub, and pull on the flower structure - like the posture of the left hand in the above picture. This process takes the longest time because there are lots of branches and flowers. 

 Once this is done, the seed / flower petal / branch mixture are sifted through a fine filter. The results won't be biased for seeds that go through this filter because > 95% of the seeds can pass through this filter. Although this step is shorter, it is the step where seeds can get lost and scattered if impatient. The result is a mixture of seeds plus from the flower petals. Since the flower petals are much lighter (and purplier) than the seeds, I purify the seeds by collecting them into a bowl, and gently blow on the seeds while one hand is cupped under the bowl and makes a swirling motion (as if mixing a very, very large bowl of beans). To improve the confetti-like experience, wearing sunglasses in this step will protect the eyes from scattering petals and enhance the confusion factor to strangers passing by. The seeds were laid on a flat surface for drying.
 
# Method: Seed Measurement
To estimate the approximately [spheroid](https://en.wikipedia.org/wiki/Spheroid) shape of amaranth seeds, the height and width must be experimentally determined. The height axis and width axes will be measured with digital calipers. Seeds were randomly selected out of a bag, measured, and then placed back, to yield 20 observations for height and width. To get a better estimation of the average size and standard deviation of amaranth seeds in this year's crop (aka the population, I will bootstrap the sample (sample_size = 14, 100K iterations), take the average and stdev per bootstrap sample, and calculate / visualize mean and sd of seed size parameters.
# Results: Volume of amaranth seeds
  After random sampling of the original data 100K times with sample_size of 14 and taking each iteration's mean and sd, we arrive to the following statistics: 
  
  * bootstrapped mean seed height = 0.74 mm
  * bootstrapped mean seed width = 1.09 mm
  * bootstrapped sd of mean seed height = 0.01 mm
  * bootstrapped sd of mean seed width = 0.01 mm
  
To calculate the volume of an amaranth seed, I use the formula of an [oblate spheroid](https://en.wikipedia.org/wiki/Spheroid) to yield a volume of 0.46 mm<sup>3</sup>. Now that is tiny!
  
# Results: Yield calculations
Here are quick back-of-the-envelope calculations to see the yield of amaranth plants per season. Assuming I isolated 20 g of seed from 100 g of amaranth biomass (seeds + branches) from 12 plants, that is 1.67 grams of seeds per plant or 0.2 grams of seeds per gram of plant biomass.

For summer 2019, I harvested enough seeds to fill a snack sized ziploc bag (16.5 cm x 8.2 cm x about 2 cm depth) - that’s about 5.81x10<sup>5</sup> number of seeds. If I 
were to sow the seeds I harvested in one season 1 feet apart, this ficticious plantation would have 762 rows and columns (I don’t recommend pulling this off, but do it in Missouri if you must). To put that into perspective, that’s like clearing 3 oblong city blocks (260 m x 89 m) or 9 normal city blocks (81 m x 81 m) and that's from just 12 plants!

# Conclusions
The amaranth plant is a hardy and proliferative crop whose seeds are tiny and numerous. In this project, the physical aspects of the amaranth seed was quantitatively described; the average height is 0.74 mm, width is 1.09 mm, sd of 0.01 mm for both height and width, and volume of 0.46 mm<sup>3</sup>. 

Make sure to check out this [link](http://garthkong.com/how-small-is-the-average-amaranth-seed/) to see photos and graphs associated with this project.

# Addendum: amaranth math

The volume of a mol of amaranth seeds (2.7692x10<sup>23</sup> mm<sup>3</sup>) is enough to:
  * smother and fill the Stowers research institute 1.08 million times assuming [600K sq.ft](https://www.stowers.org/about/campus) workspace and 15 ft ceilings.
  * cover the [entire volume of the Great Lakes](https://en.wikipedia.org/wiki/Great_Lakes) 12 times over
  * pack the Pacific Ocean at 0.04% capacity
