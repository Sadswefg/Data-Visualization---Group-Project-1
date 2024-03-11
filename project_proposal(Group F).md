# Analyzing the Impact of Mr. Trash Wheel: A Journey Through Waste Collection Trends and Composition
##
Group F - member:
- Vu Nguyen (V202000145)
- Nhat Minh
- Le Nguyen Nhat Minh
##
### Introduction

### Dataset Description
- Domain: The dataset contains information across several years, detailing the amount and types of waste collected.
- Description:
    - ID & Name: Identifier and name of the Trash Wheel device.
    - Dumpster: The numbered dumpster used for collection.
    - Month & Year: When the data was recorded.
    - Date: The specific date of data entry.
    - Weight: The weight of trash collected (in tons).
    - Volume: The volume of trash collected (in cubic yards).
    - PlasticBottles, Polystyrene, CigaretteButts, GlassBottles, PlasticBags, Wrappers, SportsBalls: Specific categories of items collected, quantified.
    - HomesPowered: Each ton of trash equates to on average 500 kilowatts of electricity. An average household will use 30 kilowatts per day.
### Questions to answer
- What are the types of waste composition that has their weight/volume increase in the last 6 months?
- 
### Plan for answering the questions
- Trend Analysis:
    - Variables involved: Date (Month, Year), weight or volume.
    - New variable: X - Time enconded as numerical type.
    - Approach: Using the linear regression method to check if the slope of each waste category is negative or positive.
- 
### Conclusion