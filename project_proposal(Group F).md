---
editor_options: 
  markdown: 
    wrap: 72
---

# Analyzing the Impact of Mr. Trash Wheel: A Journey Through Waste Collection Trends and Composition

## 

Group F - member: - Vu Nguyen - Nguyen Nhat Minh - Le
Nguyen Nhat Minh

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
|:---------------|:----------|:------------------------------------------------------------------------------------------------------------------------------------------|
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

-   Visualization and Awareness:

    -   Design and disseminate interactive dashboards and infographics
        that vividly illustrate the types and sources of ocean
        pollution.

    -   Conduct educational campaigns in collaboration with
        environmental organizations to raise public awareness.

-   Trend Analysis:

    -   Variables involved: Date (Month, Year), weight or volume.

    -   New variable: X - Time enconded as numerical type.

    -   Approach: Using the linear regression method to check if the
        slope of each waste category is negative or positive.

-   Solution Formulation and Implementation

    -   Formulate actionable strategies aimed at reducing trash inputs
        into the ocean, including waste management reforms, recycling
        incentives, and community engagement programs.

    -   Collaborate with policymakers, environmental groups, and the
        community to implement these solutions.

## Conclusion

This comprehensive approach, grounded in data collection and analysis
facilitated by Mr. Trash Wheel, promises not only to enhance our
understanding of ocean pollution but also to drive significant strides
towards mitigating this global issue. Through targeted analysis,
widespread awareness, and strategic interventions, we aim to
significantly reduce the volume of trash entering our oceans, thereby
preserving these vital ecosystems for future generations.
