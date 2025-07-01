## Business Understanding

Our company is embarking on an exciting new venture, expanding its portfolio into the dynamic world of aviation which encompasses both commercial and private air enterprises. This strategic diversification aims to strengthen our market position and open new avenues for growth. However, entering an industry as complex and regulated as aviation presents unique challenges, particularly concerning inherent operational risks associated with an aircraft.
To ensure a successful and secure entry into this sector, a critical first step is to thoroughly understand and mitigate potential risks. This project is specifically designed to address this imperative need.  

A dataset containing civil aviation accident and incident data from 1948 to 2022, sourced from the National Transportation Safety Board via Kaggle.


### Aim
Identify and assess the risk profiles of Airplanes and Helicopters in order to pinpoint  an aircraft that represent the lowest o risk interms of fatalities, thereby providing a robust foundation for the head of the aviation division.

### Objectives

 1. Examine Purpose of Flight and Accident Frequency.
 2. Determine Accident Phase Dominance.
 3. Compare Aircraft structural damage and Type to Fatalities.
 4. Identify Aircraft Model and Make with Lowest Fatalities.


## Data Understanding

### 1. Data loading and Inspection
The dataframe contains floats and objects. There are 31 columns and 90348 rows including the column names.
For the purpose of this investigation, outliers within the passenger classification data (fatal, serious, minor, and uninjured categories) will be preserved. The rationale for this decision is rooted in the potential for these outliers to reveal significant determinants of aircraft safety. 

### 2. Data Cleaning and Processing

The dataframe contained 1447 duplicated entries which were dropped.
Percentage missing value for columns with over 40% missing values.

1. 61.4% of  Longitudes and Latitudes
2. 43.5% of Airport Code 
3. 40.7% of Airport Name 
4. 63.7% of Aircraft Category
5. 64.0% of FAR Description
6. 85.9% of Schedule
7. 81.3% of Air carrier

The above columns were all dropped.
Null values for the categorical columns were replaced with the mode.
Null values from the numerical columns(passenger fatalities) were filled in with the mean vaalue +1 as a saftey measure.
For Saftey purposes the median(1) was used as opposed to mean(6) to fill in the missing values in the total uninjured passengers.
This study's focus was solely on powered, traditional aircraft types i.e. those with engines.
The other categories that might not be relevant to the research questions.
To analyze only incidents involving "Airplanes" and "Helicopters," filtering  was used in order to isolate those records and prevent irrelevant data from skewing the results.


## Results
- Most accidents occur in the Landing phase of flight followed by Take-off then lastly during cruise.
- Aircrafts that seem to involved in more accidents seem to be used mostly for Personal and Instructional use.
- Most accidents in the dataset were of non-fatal injury severity.
- Most accidents occured in (Weather_Conditions)VMC - Visual Meteorological Conditions.


## Visualisations  
1. Distribution of Accidents in different Flight Phases
2. Distribution of Injuries in different Aircraft Categories
3. Distribution of Injuries in different Aircraft Damage Categories
4. Safest Aircraft Make/Model by Total Fatalities


## Findings and Conclusion
Accident Phase Dominance: The Landing phase of flight accounts for the majority of recorded air accidents. This suggests a critical period for pilot focus, aircraft performance, and environmental factors.

Purpose of Flight and Accident Frequency: Aircraft utilized for personal and instructional purposes exhibit the highest number of recorded accidents. This indicates a potential area for targeted safety improvements, pilot training enhancements, or a closer look at the experience levels of pilots involved in these flight types.

Aircraft Category and Fatality Rates: Airplanes show a higher fatality rate at 69.5% when compared to helicopters at 63.0%. This difference warrants further investigation into the nature of accidents for each aircraft type that leads to these outcomes (e.g., impact forces, escape opportunities).

Aircraft Damage vs. Fatalities: Substantial Damage is the most frequently recorded outcome regarding aircraft damage. However, it's crucial to note that more fatalities are associated with aircraft classified as "Destroyed." This highlights that while substantial damage is common, complete destruction of the aircraft is a stronger indicator of a fatal outcome.

Aircraft Model with Lowest Fatalities: Among the analyzed aircraft models, the A310 Aircraft Model stands out for having the lowest number of recorded fatalities. This could suggest inherent safety features, operational procedures, or a lower accident rate for this specific model, though further context on its prevalence in the dataset would be beneficial.

Aircraft Make with Lowest Fatalities: Cirrus Design Corp and Fokker aircraft makes are associated with the lowest number of fatalities. Similar to the A310 model, this finding could point to design safety, operational practices, or potentially a lower exposure to high-risk scenarios for these manufacturers. Further investigation into specific models under these makes could be insightful.




## Recommendations
1. Develop a Robust Entry Strategy with Landing Safety as a Core Pillar:

Recommendation: Any business model for aviation entry must include significant upfront investment in comprehensive pilot training programs, simulator time, and adherence to best-in-class operational procedures specifically for the landing phase.
Business Impact: Mitigates the most frequent operational risk (landing accidents), potentially reducing early-stage incidents, costly repairs, and significant disruptions to nascent operations.

Linked to: Finding 1 (Landing Phase Accidents).


2. Carefully Evaluate Market Segment Entry Based on Inherent Risk:

Recommendation: If considering entry into personal or instructional flight segments, a distinct and highly rigorous safety management system must be a foundational element. Alternatively, prioritize segments with lower historical accident rates.
Business Impact: Allows for a clear-eyed assessment of the risk vs. reward of different market niches, ensuring our operational model is suited to the inherent safety profile of our chosen segment, and avoiding unforeseen compliance or reputational challenges.

Linked to: Finding 2 (Personal & Instructional Flight Accidents).

3. Prioritize Aircraft Acquisition & Design Principles for Survivability:

Recommendation: During fleet planning and aircraft acquisition, prioritize models with demonstrated lower fatality rates and robust crashworthiness (e.g., A310, and those from Cirrus Design Corp/Fokker, after normalizing for usage). Focus on designs that aim to prevent catastrophic "Destroyed" outcomes.
Business Impact: Directly impacts the potential for human loss and catastrophic asset write-offs, reducing the most severe financial and reputational impacts of an incident. It also informs strategic partnerships with manufacturers or MRO providers.

Linked to: Finding 3 (Fatalities & Damage Outcomes) and Additional Findings (Safer Aircraft Models/Makes).

