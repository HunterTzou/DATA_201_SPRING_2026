# Food Establishment Inspection Overview

## **_GOALS_**: 
- Present our WIP findings at the [MAA Spring 2026 Meeting](http://sections.maa.org/mddcva/) from April 24–25, 2026



------
Links to the Dataset: 
- DATA.montgomerycountymd.gov: -- [HHS - Food Inspection Data from July 2024 and onward](https://data.montgomerycountymd.gov/Health-and-Human-Services/HHS-Food-Inspection-Data-from-July-2024-and-onward/dkrp-gr48/about_data)
- DATA.GOV -- [HHS - Food Inspection Data from July 2024 and onward](https://catalog.data.gov/dataset/hhs-food-inspection-data-from-july-2024-and-onward)

Possible Resources:
- [Environmental Health | Food Service Facilities](https://www.montgomerycountymd.gov/HHS/LandR/FoodServiceFacility.html)
- [Food Facility Closures | Licensing & Permit Process](https://www.montgomerycountymd.gov/HHS/LandR/FoodFacilityClosures.html)
- [Food Inspection Violations](https://www.montgomerycountymd.gov/HHS/Resources/Files/L%26R/Environmental%20Health/Food%20Safety/Food_Inspection_Violations_January72025_English.pdf)

GIS Tools:
- [Folium (python)](https://folium.readthedocs.io/en/latest/)
- [QGIS](https://qgis.org/)

Montgomery County Department of Health and Human Services:
- Dept phone number: 240-777-3986
- Dept email: HHSMAIL@montgomerycountymd.gov
- Shantel M. Robinson:
  -   Cell number: 202-308-8613
  -   E-mail: shantel.robinson@montgomerycountymd.gov

## Overview

The **Licensure & Regulatory Services Program** inspects all licensed retail food establishments in Montgomery County for permit issuance, routine oversight, and complaint investigations. Included in that list are two types of routine inspections: **Comprehensive** and **Monitoring**.

A **Comprehensive Inspection** is a full evaluation of sanitation, facility maintenance, and food service operations. It includes assessment of critical controls such as food temperatures, food handling procedures, and overall regulatory compliance. This inspection provides a complete review of operational food safety conditions.

A **Monitoring Inspection** is more focused in scope. It emphasizes critical food temperatures, equipment temperatures, and general food handling and cleanliness practices. Although less extensive than a comprehensive inspection, it serves as an ongoing safeguard to ensure facilities maintain safe operations throughout the year.

---

## Risk-Based Inspection Frequency

Inspection frequency is determined by the facility’s **foodborne illness risk level**, based on the complexity of food preparation processes.

**High Priority Risk** facilities prepare food in advance or use multiple complex processes (e.g., cooking, cooling, reheating, extended hot holding).  
- At least **two monitoring inspections per year**  
- At least **one comprehensive inspection per year**

**Moderate Priority Risk** facilities prepare and cook food for service within four hours.  
- At least **one monitoring inspection per year**  
- At least **one comprehensive inspection per year**

**Low Priority Risk** facilities serve prepackaged, non-potentially hazardous foods.  
- Typically **one comprehensive inspection every two years**

---

## Critical Violations

Items marked with **(C)** indicate a **Critical Violation**. These violations directly impact food safety and require **immediate correction**. Failure to correct a critical violation may result in suspension of some or all food operations or closure of the facility until compliance is achieved. We have added an additional column to this data dictionary to be able to have this noted in the column named `Critical Item`.

---

## Food Inspection Dataset – Data Dictionary

| Column Name | API Field Name | Data Type | Description | Inspection Criteria | Critical Item |
|-------------|----------------|----------|-------------|---------------------|----------------|
| Registration Number | registration_number | Text | Registration number for restaurant. | No | No |
| Inspection Number | inspection_number | Text | Unique inspection identifier. | No | No |
| Business Name | business_name | Text | Name of establishment. | No | No |
| Owner | owner | Text | Name of entity owning the establishment. | No | No |
| Address | address | Text | Business address. | No | No |
| City | city | Text | City where the establishment is located. | No | No |
| State | state | Text | State where the establishment is located. | No | No |
| Zip | zip | Text | ZIP code of the establishment. | No | No |
| Business Type | business_type | Text | Classification of business. | No | No |
| Business Subtype | business_subtype | Text | Sub-classification of business type. | No | No |
| Inspection Type | inspection_type | Text | Reason for inspection (e.g., monitoring, complaint, follow-up). | No | No |
| Inspection Date | inspection_start_date | Floating Timestamp | Date of inspection. | No | No |
| Inspection Results | status | Text | Overall result of the inspection. | No | No |
| Food From Approved Source (C) | food_from_approved_source | Text | All food or food ingredients must derive from a regulated source. | Yes | Yes |
| Food Protected from Contamination (C) | food_protected_from_contamination | Text | Food must be protected from contamination and unfit food is prohibited. | Yes | Yes |
| Ill Workers Restricted (C) | workers_restricted | Text | Food handlers with transmissible diseases must not handle food. | Yes | Yes |
| Proper Hand Washing (C) | proper_hand_washing | Text | Employees must properly wash hands before handling food or food-contact surfaces. | Yes | Yes |
| Cooling Time and Temperature (C) | cooling_time_and_temperature | Text | Potentially hazardous food must be cooled within required time and temperature parameters. | Yes | Yes |
| Cold Holding Temperature (C) | cold_holding_temperature | Text | Cold food must be held at or below required temperature. | Yes | Yes |
| Hot Holding Temperature (C) | hot_holding_temperature | Text | Hot food must be held at or above required temperature. | Yes | Yes |
| Cooking Time and Temperature (C) | cooking_time_and_temperature | Text | Food must be cooked to required internal temperature for specified time. | Yes | Yes |
| Reheating Time and Temperature (C) | reheating_time_and_temperature | Text | Food must be reheated to required internal temperature within specified timeframe. | Yes | Yes |
| Hot and Cold Running Water Provided (C) | hot_and_cold_running_water_provided | Text | Establishment must provide hot and cold running water under pressure. | Yes | Yes |
| Proper Sewage Disposal (C) | proper_sewage_disposal | Text | Sewage must be properly disposed of without overflow. | Yes | Yes |
| Toxic Substances & Pesticides | toxic_substances_and_pesticides | Text | Toxic substances and pesticides must be properly labeled and stored. | Yes | No |
| Rodents and Insects | rodents_and_insects | Text | Establishment must control and prevent rodents and insects. | Yes | No |
| Nutritional Labeling | nutritional_labeling | Text | Applicable restaurant chains must display calorie information. | Yes | No |
| Trans Fat Ban | trans_fat_ban | Text | Prohibits use or storage of foods containing partially hydrogenated oils above allowed limits. | Yes | No |
| No-Smoking Sign Posted | nosmoking_sign_posted | Text | No-smoking signage must be clearly posted where required. | Yes | No |
| Location | location | Point | Geocoded location of the establishment. | No | No |
