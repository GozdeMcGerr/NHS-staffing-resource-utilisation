# NHS Staffing and Resource Utilisation

## Project Overview

This project analyses NHS appointment activity in England between January 2020 and June 2022, with particular attention to changes following the easing of COVID-19 restrictions from August 2021.

The analysis explores how appointment demand, service settings, appointment modes, healthcare professional types and attendance patterns affected NHS capacity and resource utilisation.

The project was completed as part of the **Data Analytics Career Accelerator at the London School of Economics and Political Science (LSE)**.

## Business Objective

The objective was to identify opportunities to:

- Allocate NHS resources more efficiently
- Understand appointment demand and capacity pressures
- Examine changes in appointment delivery following COVID-19
- Reduce missed GP appointments
- Support evidence-based workforce and scheduling decisions

## Data Source

This project used publicly available NHS appointment datasets covering:

- Appointment dates and activity
- Regional appointment information
- National appointment categories
- Healthcare professional types
- Appointment status, mode and service setting

Regional information was supplemented using publicly available health geography data from the Office for National Statistics.

## Tools and Technologies

- Python
- Jupyter Notebook
- Pandas
- Matplotlib
- Seaborn
- Excel
- Exploratory Data Analysis
- Data Cleaning and Transformation
- Data Visualisation

## Analytical Approach

### Data Preparation

The analysis began with cleaning and validating the appointment datasets. This included:

- Checking for missing values
- Identifying and removing duplicates
- Removing 21,604 duplicate records from the regional appointments dataset
- Reviewing data types and field consistency
- Combining datasets where required
- Adding regional information using an external ICB reference dataset

The datasets were imported and managed using Pandas. DataFrames were named consistently and the Python code was structured in line with PEP 8 principles.

### Data Exploration

Functions and techniques used during the exploratory analysis included:

- `groupby()`
- `sum()`
- `nlargest()`
- `nunique()`
- `sort_values()`
- `len()`
- `loc[]`

The analysis examined:

- Monthly and daily appointment trends
- Capacity utilisation
- Healthcare professional types
- Appointment attendance
- Time between booking and appointment
- Appointment modes
- Service settings
- Regional variation

Twitter data was available within the original project materials but was excluded from the final analysis because it did not directly support the primary business objective.

### Data Visualisation

Matplotlib and Seaborn were used to create bar charts and line charts.

Visualisations were designed to:

- Compare appointment categories
- Show changes over time
- Highlight differences between regions and service settings
- Communicate findings clearly to non-technical audiences

Consistent formatting, labels, legends, colour palettes and data annotations were applied throughout the analysis.

## Key Insights

### NHS Appointment Trends

The first COVID-19 lockdown in March 2020 was associated with a substantial decline in NHS appointments.

Appointment activity subsequently fluctuated alongside changes in restrictions. Following the easing of restrictions in 2021, activity increased and reached approximately 30 million appointments during the busiest months, including October, November and March.

![image_alt](https://github.com/GozdeMcGerr/NHS-staffing-resource-utilisation/blob/bffab4a62befc08c014eb129c13ce24977d9f6a7/images/Total%20Monthly%20Appointments.png)

### Capacity Utilisation

Using a daily capacity threshold of 1.2 million appointments, demand exceeded the threshold on 52% of the 334 days analysed.

Appointment demand was particularly high earlier in the week, with Tuesdays emerging as a peak day.

![image_alt](https://github.com/GozdeMcGerr/NHS-staffing-resource-utilisation/blob/b74db4558e15c38f2e3eac077aa6f81031b88090/images/Capacity%20Utilisation.png)

### Healthcare Professional Types

General Practitioners managed 51.1% of recorded appointments, while other practice staff managed 45.7%.

Following the easing of COVID-19 restrictions, appointment activity increased for both groups. From August 2021, the increase for other practice staff was greater than the increase recorded for GPs.

![image_alt](https://github.com/GozdeMcGerr/NHS-staffing-resource-utilisation/blob/bffab4a62befc08c014eb129c13ce24977d9f6a7/images/Professional%20Type.png)

### Attendance

Overall, 91.3% of appointments were attended.

The analysis identified a positive relationship between non-attended appointments and the busiest months, suggesting that increased demand may be associated with a higher number of missed appointments.

![image_alt](https://github.com/GozdeMcGerr/NHS-staffing-resource-utilisation/blob/bffab4a62befc08c014eb129c13ce24977d9f6a7/images/Did%20Not%20Attended.png)

### Time Between Booking and Appointment

Same-day appointments accounted for 44.3% of the analysed activity, while 20.5% of appointments took place between two and seven days after booking.

The results indicate a strong demand for prompt access to consultations.

![image_alt](https://github.com/GozdeMcGerr/NHS-staffing-resource-utilisation/blob/bffab4a62befc08c014eb129c13ce24977d9f6a7/images/Unattended%20Appointments%20by%20Waiting%20Time.png)

### Appointment Modes

Face-to-face appointments represented 59.2% of recorded activity, while telephone appointments accounted for 36.1%.

Telephone appointments increased following March 2020. Although face-to-face activity began to recover after restrictions eased, it remained below its earlier level.

During the busiest months, both face-to-face and telephone appointments increased, with face-to-face appointments showing the larger rise.

![image_alt](https://github.com/GozdeMcGerr/NHS-staffing-resource-utilisation/blob/0a11b8992d7b6f5af73a583eb23f1d63ba3ed653/images/Changes%20in%20Appointment%20Mode.png)

### Service Settings and Regional Activity

General Practice accounted for 91.5% of appointments.

NHS North East and North Cumbria recorded the highest activity among the ICB areas examined, while the Midlands represented 19.39% of regional appointment activity.

Unmapped service settings exceeded one million appointments from August 2021 and became the second-largest service-setting category. This may indicate an area requiring further data-quality investigation.

![image_alt](https://github.com/GozdeMcGerr/NHS-staffing-resource-utilisation/blob/bffab4a62befc08c014eb129c13ce24977d9f6a7/images/Service%20Settings.png)

## Recommendations

### 1. Increase Early-Week Staffing

Review staffing levels earlier in the week, particularly on high-demand days, and assess whether greater weekend availability could help distribute demand more evenly.

### 2. Support Appropriate Telephone Appointments

Continue offering telephone appointments where clinically appropriate, particularly during periods of increased demand.

### 3. Prioritise Timely Appointments

Maintain short waiting periods where possible and consider increasing access to same-day appointments, which recorded strong attendance.

### 4. Understand Patient Preferences

Consult patients about preferred appointment times and modes to support accessible scheduling and reduce missed appointments.

### 5. Improve Online Scheduling

Consider accessible online scheduling options that allow patients to book and manage appointments more conveniently.

### 6. Investigate Unmapped Service Settings

Review the coding and completeness of service-setting information to understand why a substantial volume of appointments was recorded as unmapped.

## Project Files

- `Gozde_McGerr_DA201_Assignment_Notebook.ipynb` – complete Python analysis
- `README.md` – project overview, findings and recommendations
- `images/` – selected charts and visualisations

## Limitations

- The analysis is based on aggregated public datasets and does not include individual patient-level information.
- The 1.2 million daily appointment threshold was used as an analytical benchmark within the project.
- The analysis identifies relationships and trends but does not establish direct causation.
- Unmapped service-setting records may affect interpretation of activity by service type.
- Findings relate to the period and datasets included in the original analysis.

## Skills Demonstrated

- Healthcare data analysis
- Python programming
- Data cleaning and validation
- Exploratory data analysis
- Time-series analysis
- Data visualisation
- Capacity and resource analysis
- Data-quality assessment
- Evidence-based recommendations
- Communication of analytical findings

## About the Project

This project was completed as part of the **LSE Data Analytics Career Accelerator**.

It demonstrates how Python and public healthcare data can be used to investigate operational demand, resource utilisation, capacity pressures and appointment trends within the NHS.
