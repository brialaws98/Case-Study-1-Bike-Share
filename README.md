# Case-Study-1-Bike-Share Analysis
## 1. Ask
* ***Business Task***
 * ***Characters and teams***
    * ***Cyclistic:***
       * A bike-share program that features more than *5,800 bicycles* and *600 docking stations*
       * Sets itself apart by offering reclining bikes, hand tricycles, and cargo bikes
          * Make bike-share more inclusive to people with disabilities and riders who can't use a standard two-wheeled bike
       * The majority of riders opt for traditional bikes
          * About 8% of riders use the assistive options
       *  More likely to ride for leisure
          * About 30% use them to commute to work each day
    * The ***director of marketing*** *(Lily Moreno)*
      * wants to maximize the number of annual memberships
       * Assigned question to be answered: *How do annual members and casual riders use Cyclistic bikes differently?*
        * Believes that maximizing the number of annual members will be key to future growth
    * ***My team*** *(Cyclistsic marketing team)*
        * Wants to understand how casual riders *(Customers)* and annual members *(Subscribers)* use Cyclistic bikes differently
        * Will design a new marketing strategy to convert casual riders into annual members
    * ***Cyclistic executives***
        * Must approve of recommendations
        * Back findings with compelling data insights and professional data visualizations ***Key tasks***
* **Identify the business task**
    * Maximize the number of annual members
    * How annual members and casual members use Cyclistic differently
* **Consider key stakeholders**
    * The ***Cyclist executives*** are the main stakeholders
* ***Clear Statement of the business task***
    *The main goal is to optimize the annual membership acquisition of Cyclistic. We aim to understand usage patterns among annual and casual members, exploring how they use the services differently. The key decision-makers in this effort are the **Cyclistic executive**.*

## 2. Prepare
* ***Data Information***
    * For this study, I will be using the [Cyclist trip](https://divvy-tripdata.s3.amazonaws.com/index.html)
        * The dataset has been made available by *Motiate International Inc.* under this [license](https://divvybikes.com/data-license-agreement)
        * Working with the *2019 Q1* dataset
            * Not up-to-date
* ***Data Organization and Verification***
    * Sorted by date with the following format: *YYYY/MM/DD*
    * The dates are not in order
    * Every user has a unique *tripID*

## 3. Process
* ***Errors***
   * *dates* are not in order
* ***Tools***
   * BigQuery for ***SQL***
      * Get rid of data with NULLs in the *gender* column
      * Order dates
   * Google sheets for ***Excel***
      * Separate the *TIMESTAMP* column into *date*, *start_at*, *end_at*, and *day_of_week* columns
   * Tableau for ***data visualizations***
* ***Cleaning Process***
   * Use BiqQuery to:
      * Get rid of the rows where the *gender* columns are NULL
         * Dataset was too large for Google Sheets so I used BigQuery to get rid of the NULLs in the *gender* section so that the code could then be extracted into Google Sheets
     * Once this was done I was able to export the new CSV file to Google Sheets to organize the data further

## 4. Analyze and Share
* Use **BigQuery** to organize and sort data even further in each
   * Identify the total number of rows
   * Edit out columns that will not be used in the research
   * Fix columns
      * Edit out NULLs
      * Made sure the *ride_length* column only includes numbers that are *greater than or equal to* 0
    * Order the columns by *date*
* What have I found with this analysis
   * More *Subscribers* and *Customers* use the bikes on Thursday
      * Why is that the case?
      * Is there a special deal for Thursdays
   * Which genders use the bikes more
     * Majority of males for * Subscribers* and *Customers*
     * There are more *Subscribers* than there are *Customer* members
* Questions that the Tableau dashboard can answer
   * The *ride_length* of each day of the week
   * Which membership do customers favor more?
      * *Subscribers* or *Customers*
   * What is the *age* and *gender* of majority of CYclists?
      * This could affect the advertisement in the future

## Act
* ***Final thoughts based on analysis?***
     * I see that there is a large number of adults that are male that ride the the cycles daily
     * The fact that this company offers many alternatives can be what adds to its success
     * The gender and age of *annual members ***(Subscriber)**** and *casual riders***(casual riders)**** can affect the advertisement in the future
* ***How can my team and business apply these insights?***
     * The goal reminder:
          * Maximize the number of annual members
          * Understand patterns to understand how the service is used differently
     * What are the insights:
          * There are more male and female annual riders than there are for casual riders
          * A majority of these riders are Adults
               * Could be due to a majority of riders using the services to get to work
          * The top three days people use this service are Tuesdays, Thursdays, and Fridays
* ***Top 3 recommendations based on my analysis?***
     1. ***Targeted Advertisement Strategy***
           * Based on the observation that a large number of adults, particularly males, ride the cycles daily and the majority of annual riders are adults, focus your advertising efforts on targeting adult audiences
           * Consider tailoring advertisements specifically towards the weekdays, particularly Tuesdays, Thursdays, and Fridays
                * Aligns with the top usage days
           * Highlight the convenience of using the service for daily commuting
                *Could potentially attract more annual memberships from this demographic
     2. ***Customized Membership Offers***
           * Leverage the fact that there are more male and female annual members compared to casual riders by offering special promotions or discounted annual membership rates for adults
           * Offer tailored membership packages that cater to the commuting needs of this demographic
           * Present data-driven incentives to encourage casual riders to convert to annual memberships, emphasizing the cost-effectiveness and convenience of long-term membership
  3. ***Engagement and Feedback Loop***
        * Establish a feedback with existing annual members
        * Conduct surveys to understand usage patterns and preferences
        * Utilize feedback to refine the service and engage with members effectively
