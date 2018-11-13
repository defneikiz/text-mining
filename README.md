# Text Mining Project

###MIS3640 - Problem Solving & Software Design

## Table of Contents

- [Project Overview](#Overview)
- [Implementation](#Implementation)
- [Results](#Results)
- [Reflection](#Reflection)

## Packages Used:
[re](https://docs.python.org/3/library/re.html)
[tweepy](https://github.com/tweepy/tweepy.git)
[textblob](https://textblob.readthedocs.io/en/dev/)

## <a name="Project">Project Overview:</a>
I used the librariries listed above and the class technique in this project. The goal of this project was to analyze Elon Musk's tweets and conduct a natural language sentiment assesment to determine whether his language was positive, negative or neutral. My interest in doing this project came from the recent price changes in Tesla stocks, some of which caused by Elon Musk's tweets. I hoped to create a tool that can be used in financial models to determine Tesla stock prices, looking at the sentiment analysis of his latest tweets. 
## <a name="Implementation">Implementation:</a>
I wrote this project in a class called TwitterClient, and used various methods that each served their own purpose. The first method __init__ is the initialization method I used to introduce the Twitter API. I also implemented checks in place to see if the consumer key/secret and token key/secret were authorized by Twitter, so that one can determine the program is working without error from Twitter's end.
The cleaning method I used was clean_tweet, to remove unnecessary characters from tweets to be able to analyze them using re library. I chose to clean the tweets this way because the code is much shorter, hence better optimized than individually picking out punctuation, links, and tags(@username). I also used textblob to conduct the sentiment analysis, instead of NLTK because my research showed that NLTK is a really big library compared to TextBlob which made it attractive to me as a learner. Additionally TextBlob is much more efficient than NLTK, especially in sentiment analysis. Lastly I used tweepy instead of twython because I wanted to get only @Elon Musk's tweets, and not just the tweets that included the string 'Elon Musk' in it, partly because 'elonmusk' was used in tweets that came from multiple languages creating a challange for analysis.

## <a name="Results">Results:</a>
I found out that 46.5% of Elon Musk's tweets were positive while 12.5% of them negative, with the remaining neutral. In order to check that the sentiment analyzer was workin correctly I also displayed examples of positive and negative tweets. 

Please find below an example of an output for sentiment analysis with 5 examples each of the tweets analyzed for positive and negative sentiment: 

Positive tweets percentage: 46.5 %
Negative tweets percentage: 12.5 %
Neutral tweets percentage: 41.0 %


Positive tweets:
Rest in peace, Stan Lee. The many worlds of imagination &amp; delight you created for humanity will last forever.
@_sheateher @MalibuWine Is he ok?
It naturally follows that a hotter system will have more energetic events. For example, as a pot of water becomes c… https://t.co/n0v2Aj7XCK
@kenlacovara Agreed, technically, mined hydrocarbons come primarily from ancient, decayed marine organisms &amp; partia… https://t.co/jsoD2VhpEG
@SeanGVarney That is true &amp; should be applauded. Right move is for oil companies truly to think of themselves as en… https://t.co/ILJkPvn8QW
@zandywithaz Because people on the ground know more about what’s actually needed than politicians do
@JackCydia Good, but not hospital grade. S &amp; X were designed to be proof against an actual bioweapon attack. Requir… https://t.co/h1DMCz5KBq
@tizmagik @TeslaSupport Fair point, will reenable
@mihk101 Agreed, top priority for Autopilot team. Being cautious for max safety.
Please lmk what you’d most like improved/fixed about your Tesla. Thanks!


Negative tweets:
@karaswisher Scary sign of times to come. It will get worse.
Makes me so mad when smart, ethical scientists I know are accused of publishing climate papers for “grant money”. T… https://t.co/Jx44TRx9F5
We know we’ll run out of dead dinosaurs to mine for fuel &amp; have to use sustainable energy eventually, so why not go… https://t.co/UhjHQqKWEg
RT @AndreiBulu: Horrible Bay Area air quality due to Paradise, CA fire...  Check out this laser particle counter "Window Up / Window to Paradise, CA fire...  Check out this laser particle counter "Window Up / Window Down"…        ntly represents almost 36% of the total U.S. plug-in electric car market and togethRT @InsideEVs: Holy cow! The @Tesla #Model3 currently represents almost 36% of the total U.S. plugven inactive accounts. My follower count decreased by ~20k over the past few days.-in electric car market and together with…
I think Twitter is deleting fake, scam or maybe eonight. Disturbingly long. On track for opening party Dec 10. Will be very one-dimeven inactive accounts. My follower count decreased by ~20k over the past few days.
@bri_the_cheesy TrueWalked full length of Boring Co tunnel under LA tonight. Disturbingly long. On track for opening party Dec 10. Will be very one-dimeonight. Disturbingly long. On track for opening party Dec 10. Will be very one-dimensional.       ponges.
We didn’t even have kids back then. Just little sHopefully, partial presence in India, Africa &amp; South America end o… https://t.cponges.
@annerajb @vincent13031925 @Teslarati @panasonic
Hopefully, partial presence in India, Africa &amp; South America end o… https://t.co/f4ZoXZrjq1

## <a name="Reflection">Reflection:</a>

I found this project highly challenging but also very fun. It was enjoyable to set a goal, and try and find ways to reach that goal. I used libraries that we have not explored in class before which was incharted territory for a beginner like me. I think my research for different methods to do different methods paid off in the sense that I have much more concise code that I would have if I used other alternatives. I could improve the project by using more text analysis tools, and visualizing the outcome in a graph. This project can be used as a component of a financial modeling tool as well, determining the potential changes in stock prices in real time helping investors make investing decisions for Tesla stocks.