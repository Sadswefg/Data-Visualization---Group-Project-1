---
editor_options: 
  markdown: 
    wrap: 72
---

# Analyzing the Impact of Mr. Trash Wheel: A Journey Through Waste Collection Trends and Composition

## 

Group F - member: - Vu Nguyen - Nguyen Nhat Minh - Le Nguyen Nhat Minh

## Introduction

Given the pressing issue of water pollution, a thorough analysis
underscores the importance of gaining an in-depth understanding of the
types of trash predominantly disposed of in the ocean. With the
assistance of Mr. Trash Wheel—a semi-autonomous trash interceptor
installed at the terminus of rivers, streams, or other outflows—we are
poised to enhance the application of these data through detailed
analysis and visualization. This approach will not only shed light on
the current situation but also pave the way for devising effective
solutions to combat future trash dumping.

## Dataset Analysis

### Dataset Brief Description

-   Domain: The dataset contains information across several years,
    detailing the amount and types of waste collected.

-   Description:

    -   ID & Name: Identifier and name of the Trash Wheel device.
    -   Dumpster: The numbered dumpster used for collection.
    -   Month & Year: When the data was recorded.
    -   Date: The specific date of data entry.
    -   Weight: The weight of trash collected (in tons).
    -   Volume: The volume of trash collected (in cubic yards).
    -   PlasticBottles, Polystyrene, CigaretteButts, GlassBottles,
        PlasticBags, Wrappers, SportsBalls: Specific categories of items
        collected, quantified.
    -   HomesPowered: Each ton of trash equates to on average 500
        kilowatts of electricity. An average household will use 30
        kilowatts per day.

### Data dictionary

| variable       | class     | description                                                                                                                               |
|:-----------------|:-----------------|:------------------------------------|
| ID             | character | Short name for the Trash Wheel                                                                                                            |
| Name           | character | Name of the Trash Wheel                                                                                                                   |
| Dumpster       | double    | Dumpster number                                                                                                                           |
| Month          | character | Month                                                                                                                                     |
| Year           | double    | Year                                                                                                                                      |
| Date           | character | Weight in tons                                                                                                                            |
| Weight         | double    | Volume in cubic yards                                                                                                                     |
| Volumn         | double    | Number of plastic bottles                                                                                                                 |
| PlasticBottles | double    | Number of polystyrene items                                                                                                               |
| Polystyrene    | double    | Number of cigarette butts                                                                                                                 |
| CigaretteButts | double    | Number of glass bottles                                                                                                                   |
| GlassBottles   | double    | Height of the item in Centimeter                                                                                                          |
| PlasticBags    | double    | Number of plastic bags                                                                                                                    |
| Wrappers       | double    | Number of wrappers                                                                                                                        |
| SportsBalls    | double    | Number of sports balls                                                                                                                    |
| HomesPowered   | double    | Homes Powered - Each ton of trash equates to on average 500 kilowatts of electricity. An average household will use 30 kilowatts per day. |

### Question that we want to answer

-   What are the types of waste composition that has their weight/volume
    increase in the last 6 months?

-   Which type of trash wheels have a highest performance, throughout
    the years, analyse the improvement of the usage of different trash
    wheel?

### Plan for answering the questions

-   Plan for answering question 1: What are the types of waste
    composition that has their weight/volume increase in the last 6
    months?

    -   For this analysis, our team aims to summarize the total weight
        of each type of trash over the past six months. We will then
        visualize this data using boxplots to compare and identify which
        types of trash have been most prevalent. This analysis will
        allow us to predict potential increases in trash volume
        attributed to a growing population and to pinpoint which
        specific types of trash are being dumped most frequently. To
        accomplish this, we will perform the following steps:

        -   **Data Summarization:** We will aggregate the total weight
            of each type of trash (Plastic bottles, Glass bottles, etc.
            ) over the last six months since we believe that analysing
            each day could be quite complicated and summarize it by
            seasons could be better to generalize the data but still can
            accurately analyze the trends**.**

        -   **Variable Use:**

            We will need to keep track on the Year and Date in order to
            get total weights in a specific amount of time ( in the
            scope of this question, we will focus on the data after
            5/4/23):

            |       |           |                |
            |:------|:----------|:---------------|
            | Month | character | Month          |
            | Year  | double    | Year           |
            | Date  | character | Weight in tons |

            To calculate the total weight of a specific trash being
            dumped over 6 months, we will need to have a specific weight
            for each type of trashes:

            |                |        |                                                                                                                                           |
            |:-----------------|:-----------------|:------------------------------------|
            | PlasticBottles | double | Number of polystyrene items                                                                                                               |
            | Polystyrene    | double | Number of cigarette butts                                                                                                                 |
            | CigaretteButts | double | Number of glass bottles                                                                                                                   |
            | GlassBottles   | double | Height of the item in Centimeter                                                                                                          |
            | PlasticBags    | double | Number of plastic bags                                                                                                                    |
            | Wrappers       | double | Number of wrappers                                                                                                                        |
            | SportsBalls    | double | Number of sports balls                                                                                                                    |
            | HomesPowered   | double | Homes Powered - Each ton of trash equates to on average 500 kilowatts of electricity. An average household will use 30 kilowatts per day. |

        -   **Visualization**: Create boxplots to visually compare the
            distribution of trash weights across different types. Each
            boxplot will represent a specific type of trash.

        -   **Interpretation**: By analyzing the boxplots, we can make
            predictions about potential increases in trash volume due to
            population growth and identify which specific types of trash
            are most prevalent. If the data includes timestamps, the
            boxplots can be grouped and analyzed by month or other time
            intervals to identify temporal trends in trash disposal.

            -   **Identifying Trends:** Patterns such as increasing or
                decreasing weights over time can be observed. We could
                make comparison whether certain types consistently have
                higher or lower weights, then also can identify presence
                of outliers, which may indicate unusual occurrences or
                specific patterns for certain types of trash.

            -   **Determining Dominant Trash Types:** Types with
                consistently higher median weights or larger
                interquartile ranges may indicate prevalent trash
                categories.

            -   **Predictive Analysis:** Trends observed in the boxplots
                can inform predictions about future trash disposal
                patterns, aiding in waste management planning and
                resource allocation.

    -   Next, we plan to plot a line graph in order to visualize trends
        in trash disposal over time. Line graph could be suitable in
        this case since it provides a clear and intuitive representation
        of how the weights of different trash types have varied over the
        past months. Here's a detailed explanation of how we can utilize
        a line graph for this purpose:

        -   **Data Preparation**: Before creating the line graph, we
            need to ensure that our data is properly formatted. Each row
            in our dataset should represent a specific measurement of
            trash weight, along with the corresponding timestamp
            indicating when the measurement was taken. Additionally, the
            data should be aggregated or summarized to calculate the
            total weight of each trash type for each time period (e.g.,
            month).

        -   **Variable use:**

            |                |           |                                                                                                                                           |
            |:-----------------|:-----------------|:-----------------------------------|
            | Month          | character | Month                                                                                                                                     |
            | Year           | double    | Year                                                                                                                                      |
            | Date           | character | Weight in tons                                                                                                                            |
            | Weight         | double    | Volume in cubic yards                                                                                                                     |
            | Volumn         | double    | Number of plastic bottles                                                                                                                 |
            | PlasticBottles | double    | Number of polystyrene items                                                                                                               |
            | Polystyrene    | double    | Number of cigarette butts                                                                                                                 |
            | CigaretteButts | double    | Number of glass bottles                                                                                                                   |
            | GlassBottles   | double    | Height of the item in Centimeter                                                                                                          |
            | PlasticBags    | double    | Number of plastic bags                                                                                                                    |
            | Wrappers       | double    | Number of wrappers                                                                                                                        |
            | SportsBalls    | double    | Number of sports balls                                                                                                                    |
            | HomesPowered   | double    | Homes Powered - Each ton of trash equates to on average 500 kilowatts of electricity. An average household will use 30 kilowatts per day. |

        -   **X-axis and Y-axis**: In the line graph, the x-axis
            represents time, typically plotted chronologically, while
            the y-axis represents the total weight of trash for each
            type. The time intervals (e.g., months) are plotted along
            the x-axis, and the corresponding total weights are plotted
            along the y-axis.

        -   **Visualization**: Each trash type will be represented by a
            separate line on the graph. The points on each line
            represent the total weight of that trash type for each time
            period (e.g., month). By connecting these points with lines,
            we can visualize the trend in trash disposal for each type
            over time.

        -   **Interpretation**:

            -   **Trend Analysis**: By examining the direction and slope
                of each line, we can identify whether the weight of each
                trash type has been increasing, decreasing, or remaining
                relatively stable over time.

            -   **Comparative Analysis**: We can compare the trends of
                different trash types to identify which types have shown
                the most significant changes in weight over the
                specified time period.

            -   **Seasonal Patterns**: If the data spans multiple years,
                we may observe seasonal patterns or fluctuations in
                trash disposal, such as increased waste during holiday
                seasons or specific months.

            -   **Outliers and Anomalies**: Sudden spikes or dips in the
                lines may indicate outliers or anomalies in the data,
                which could be further investigated to understand their
                causes.

        -   **Enhancements**:

            -   **Color Coding**: Assigning different colors to each
                line can make it easier to distinguish between trash
                types and enhance the visual appeal of the graph.

            -   **Annotations**: Adding labels, markers, or annotations
                to key data points or trends can provide additional
                context and help viewers interpret the graph more
                effectively.

            -   **Regression Analysis**: If desired, regression lines or
                curves can be added to the graph to visualize the
                overall trend and predict future values based on
                historical data.

        -   **Insight Generation**: Analyzing the line graph can help us
            gain insights into long-term patterns and changes in trash
            disposal behavior, which can inform decision-making and
            strategic planning for waste management initiatives,
            resource allocation, and environmental sustainability
            efforts.

    -   Last but not least, our team will plot a stacked bar chart to
        visualize the composition of total trash weight for each year
        with trends, providing insight into the proportion of each trash
        type relative to the total weight:

        -   **Data Preparation**: Similar to the line graph, our dataset
            needs to be properly formatted with rows representing
            measurements of trash weight, including timestamps (which
            have been interpreted in the table as Date and Year columns)
            that indicating when the measurements were taken.
            Additionally, the data should be aggregated or summarized to
            calculate the total weight of each trash type for each year.

        -   **Variable Use:**

            |                |           |                                                                                                                                           |
            |:-----------------|:--------------------|:--------------------------------|
            | Month          | character | Month                                                                                                                                     |
            | Year           | double    | Year                                                                                                                                      |
            | Date           | character | Weight in tons                                                                                                                            |
            | Weight         | double    | Volume in cubic yards                                                                                                                     |
            | Volumn         | double    | Number of plastic bottles                                                                                                                 |
            | PlasticBottles | double    | Number of polystyrene items                                                                                                               |
            | Polystyrene    | double    | Number of cigarette butts                                                                                                                 |
            | CigaretteButts | double    | Number of glass bottles                                                                                                                   |
            | GlassBottles   | double    | Height of the item in Centimeter                                                                                                          |
            | PlasticBags    | double    | Number of plastic bags                                                                                                                    |
            | Wrappers       | double    | Number of wrappers                                                                                                                        |
            | SportsBalls    | double    | Number of sports balls                                                                                                                    |
            | HomesPowered   | double    | Homes Powered - Each ton of trash equates to on average 500 kilowatts of electricity. An average household will use 30 kilowatts per day. |

        -   **X-axis and Y-axis**: In the stacked bar chart, the x-axis
            represents each year, while the y-axis represents the total
            weight of trash. Each bar on the chart represents a year,
            and the height of the bar corresponds to the total weight of
            trash for that year. The bars are divided into segments,
            with each segment representing a different trash type.

        -   **Plotting the Data**: Each bar on the chart is divided into
            segments, with each segment representing a different trash
            type. The length of each segment corresponds to the weight
            of that trash type relative to the total weight for the
            corresponding year. By stacking these segments on top of
            each other, we can visualize the total weight of each trash
            type relative to the total weight for each year.

        -   **Interpretation of the Stacked Bar Chart**:

            -   **Composition Analysis**: By examining the height of
                each segment within a bar, we can see the proportion of
                each trash type relative to the total weight for each
                year.

            -   **Year-on-Year Comparison**: We can compare the
                composition of trash types across different years to
                identify changes or trends in waste disposal patterns
                over time.

            -   **Identifying Dominant Trash Types**: Segments that
                consistently occupy a larger portion of the bar indicate
                trash types that contribute significantly to the total
                weight and may require specific attention in waste
                management strategies.

        -   **Enhancements**:

            -   **Color Coding**: Assigning different colors to each
                segment can make it easier to distinguish between trash
                types and enhance the visual appeal of the chart.

            -   **Labels and Legends**: Adding labels to the segments
                and a legend to the chart can provide additional context
                and help viewers interpret the chart more effectively.

            -   **Interaction**: If the chart is interactive, viewers
                can hover over segments to see specific weight values or
                click on segments to drill down into more detailed
                information.

        -   **Insight Generation**: Analyzing the stacked bar chart can
            help us understand the composition of trash disposal for
            each year, enabling stakeholders to identify trends,
            prioritize interventions, and allocate resources effectively
            to address waste management challenges and promote
            environmental sustainability.

## Question 2

-   In addressing the 2nd question of identifying the Trash Wheel that
    has demonstrated the highest level of waste collection performance
    over time, our analysis is based on a comprehensive and
    methodologically sound framework. This framework meticulously
    dissects the dataset, which records the operational outputs of
    various Trash Wheels, including key metrics like the weight and
    volume of collected waste, among other information. Our goal is to
    determine which Trash Wheel is the most efficient in terms of waste
    collection, as well as to understand the trajectory of operational
    improvements demonstrated over time.

-   Detailed analytical approach involves data segmentation and
    aggregation.

-   To begin, we separate the dataset by Trash Wheel, which are
    identified by unique "ID" and "Name" attributes. This step is
    essential for a thorough analysis. Following that, we aggregate the
    data for each Trash Wheel on an annual basis, calculating the total
    "Weight" and "Volume" of waste collected that year. This aggregation
    provides a yearly snapshot of performance, allowing for a long-term
    comparison of each Trash Wheel's effectiveness.

-   Performance metric analysis:

    -   To evaluate the operational efficiency of the Trash Wheels, we
        will use the `Weight` and `Volume` metrics similar to those used
        in the first question. An annual comparison of these metrics
        across different Trash Wheels will reveal performance trends and
        patterns, as well as areas for improvement.

    -   **Trend Analysis and Visualization:** We will use time-series
        analysis to chart the historical performance of each trash
        wheel. This will include a visual representation of `Weight` and
        `Volume` metrics over time, which will aid in identifying any
        significant performance trends, spikes, or declines that may
        require further investigation.

-   **Graphical Representations for Analysis:**

    -   Performance Over Time: **Line Graphs**

        -   **Purpose:** To illustrate the performance of each Trash
            Wheel over time, highlighting trends and year-on-year
            changes in waste collection.

        -   **Variables Displayed:** Total annual `Weight` and
            `Volume` of collected waste for each Trash Wheel.

        -   **New Variables:** `Yearly Performance Growth Rate`,
            calculated as the percentage change in `Weight` and
            `Volume` from one year to the next, to quantify
            performance improvements or declines.

    -   Comparative Analysis: **Boxplots**

        -   **Purpose:** To compare the variability and central
            tendency in the annual performance of Trash Wheels,
            identifying outliers and consistency in performance.

        -   **Variables Displayed:** Distribution of `Weight` and
            `Volume` metrics across years for each Trash Wheel.

        -   **New Variables:** `Seasonal Performance Indices`,
            representing aggregated `Weight` and `Volume` over
            predefined seasons within each year, to examine seasonal
            patterns and anomalies.

    -   Efficiency and Improvement Visualization: **Stacked Bar
        Charts**

        -   **Purpose:** To showcase the efficiency improvements and
            operational enhancements of Trash Wheels over the years.

        -   **Variables Displayed:** Breakdown of `Weight` and
            `Volume` by different waste types or categories each
            year, showing the composition and diversity of waste
            collection

        -   **New Variables:** `Operational Efficiency Score`, a
            composite metric derived from the volume of waste
            collected per operational hour or day, indicating the
            operational efficiency of each Trash Wheel.

    -   Correlation Analysis: **Scatter Plots**

        -   **Purpose:** To explore the relationship between
            operational enhancements (like technological upgrades)
            and performance metrics.

        -   **Variables Displayed:** Operational enhancements or
            changes as discrete events plotted against performance
            metrics (`Weight` and `Volume`).

        -   **New Variables:** `Technology Upgrade Index`,
            quantifying the extent and impact of technological
            upgrades on performance, mapped against the timeline of
            waste collection metrics.

    -   Newly Created Variables for In-Depth Analysis:

        -   `Yearly Performance Growth Rate`: This variable will be
            crucial for identifying trends in the performance of
            each Trash Wheel, highlighting whether there has been an
            improvement or decline in waste collection capabilities
            over the years.

        -   `Seasonal Performance Indices`: By aggregating "Weight"
            and "Volume" data into seasonal segments, we can analyze
            how seasonal variations and operational changes impact
            the performance of Trash Wheels.

        -   `Operational Efficiency Score`: This composite metric
            will consider factors such as the amount of waste
            collected per operational hour and the diversity of
            waste types handled, providing a holistic view of each
            Trash Wheel's operational efficiency.\

        -   `Technology Upgrade Index`: Reflecting the cumulative
            impact of technological upgrades on performance, this
            index will be correlated with waste collection metrics
            to assess the effectiveness of operational enhancements.

    -   Using these graphical representations and newly created
        variables, we will be able to conduct a detailed analysis of
        the Trash Wheels' performance and operational improvements
        over time. By visually illustrating trends, correlations,
        and comparative performance metrics, we can gain actionable
        insights into which Trash Wheels are the most efficient and
        how operational strategies can be optimized for better waste
        collection and environmental sustainability. This
        comprehensive approach, informed by the detailed methodology
        used for the first question, will result in a robust and
        insightful analysis that addresses our research's primary
        objectives.

-   Comprehensive Comparative and Statistical Analysis:

    -   To compare the performance of all Trash Wheels, we will use the
        same analytical depth as in the first question. This will entail
        using statistical measures, such as average annual performance
        and compound annual growth rate (CAGR), to identify the most
        efficient Trash Wheel in terms of waste collection and quantify
        the rate of performance improvement over time.

-   Recommendations for improvements:

    -   Peak Performance Evaluation: Identifying the peak performance
        years for each Trash Wheel will provide insight into the maximum
        operational efficiency achieved. This analysis will also take
        into account the events or initiatives that led to these peak
        performances, such as technological upgrades or expanded
        operational areas.

    -   Consistency Assessment: Evaluating the consistency of each Trash
        Wheel's performance using the variance or standard deviation of
        the annual metrics will highlight the dependability of waste
        collection efforts. A Trash Wheel with a lower variance in
        performance is considered more dependable and consistent.

    -   Contextual Analysis: In order to ensure a fair comparison,
        external factors such as changes in environmental policies,
        significant weather events, or operational challenges must be
        taken into consideration.

    -   Operational Enhancements: Based on the findings from the
        analysis, recommendations for operational improvements will be
        made. These could include technological upgrades to improve
        efficiency, strategies to expand the Trash Wheels' coverage
        area, or initiatives to raise public awareness and participation
        in waste management practices.

-   Conclusive Insights: This methodologically robust analysis reveals a
    clear ranking of Trash Wheel performance for waste collection
    efficiency. Beyond identifying the best-performing Trash Wheel, our
    approach seeks to trace each's improvement trajectory,
    contextualized against a backdrop of operational and environmental
    variables. The end result of this endeavor is expected to yield
    actionable insights that could inform strategic decisions to enhance
    the efficiency of existing Trash Wheels and guide the deployment of
    future installations, thereby significantly contributing to our
    collective efforts to mitigate aquatic pollution.

## Conclusion

This comprehensive approach, grounded in data collection and analysis
facilitated by Mr. Trash Wheel, promises not only to enhance our
understanding of ocean pollution but also to drive significant strides
towards mitigating this global issue. Through targeted analysis,
widespread awareness, and strategic interventions, we aim to
significantly reduce the volume of trash entering our oceans, thereby
preserving these vital ecosystems for future generations.
