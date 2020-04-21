# MMA-Victory-Analyses

The purpose of this project is to bring together the many analytics skills I'ved learned over the last 6 months on a project that I came up with and executed myself. I use several different datasets to analyze major MMA fighter's methods of victory in past fights to both understand the data, and to make predictions about the outcomes of future fights.

Specific skills I leveraged in this project:
 - Exploratory Data Analysis
 - Machine learning for classification
 - Data cleaning with Pandas and Numpy
 - Interactive visualizations with Plotly
 - Custom Python functions and mathematics
 - Web scraping
 
The project is broken into three parts:
  Part 1: Analyzing fight data scraped from Wikipedia
      In this section, I use pandas to pull a list of current UFC fighters. I then created a short script to scrape 
      each fighter's Wikipedia page to create a dataframe with all fighter's with Wikipedia pages MMA records. I then
      go through a series of steps to clean the data into a final dataset containing their victories by each of three methods:
      Decision, Submission, and KO/TKO, which are the three primary ways that a fighter can win a fight. With that data 
      formatted for each fighter available, I then apply a k-means clustering model to the data. Finally, I apply the results
      of that classification to each fighter, and visualize the results using a 3D scatter chart using Plotly. The chart 
      displays each fighter as a datapoint on a three dimensional axis based on their number of Decision, Submission, and 
      KO/TKO victories. Each fighter point is colored based on the category they're grouped into. The scatter can then be 
      explored to understand what mix of those victory types the algorithm grouped them into.
      
   Part 2: Exploratory Data Analysis
      Following my initial analysis, I got curious about the specific victory method types. Each MMA record on a fighter's
      Wikipedia page lists both the general victory type (Submission, KO, Decision, etc.), and the specific method of that
      victory type. For instance, a fighter could win via submission by rear raked choke, or a KO via kick to the head. Mixed
      Martial Arts as a discipline is relatively new in the modern era, and I suspected that the methods of victory might have
      changed over time as different styles and counters to those styles have come into play. This did turn out to be the
      case. I cleaned up the data from the first analysis to include the specific victory method, then I visualized the number
      of victories of each type over type. From that analysis, it was quite clear which victory types have fallen out of 
      favor, which have always been rare, and which are consistently effective over time. The readme in this section will
      include an overview of my findings.
      
   Part 3: Fight Outcome Predictor
       As I worked through the analysis described above, I realized the most interesting things to do with this data would be
       to try to classify fighters to enable predictions based on the past outcomes of fighter of various classes. The 
       included takes a previously scraped dataset, which includes statistics such as takedowns and striking accuracy
       for every UFC fighter. I had to use several unique EDA activities and cleaning methods to format this data for another
       round of classification. Once I got it into the right format, I now have a basic template to start to analyze outcome
       probabilities for future fights. I used the classifications the model came up with to compare the results of the range
       of the dataset (up to mid-2019), to the outcomes of fights with those same fighters from mid-2019 until mid-2020. 
       It was interesting to find that the win percentages for at least some of the matchups was fairly consistent. This
       suggests that it may be possible with further refinement (several of which I've already noted in the specific project
       file) to classify fighters based on their unique profile over time, and, for some fights, be able to determine
       a data-driven expectation of which fighter has the advantage based on their style.
      

