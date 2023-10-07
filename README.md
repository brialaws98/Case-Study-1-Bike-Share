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
        * Wants to understand how casual riders and annual members use Cyclistic bikes differently
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
* ***How can my team and business apply these insights?***
* ***Top 3 recommendations based on my analysis?***
