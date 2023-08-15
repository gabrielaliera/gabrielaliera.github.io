---
title: "BrenchWARNING"
description: "Breach WARNing shows up-to-date information on data breaches and job layoffs."
dateString: "May 2023 "
draft: false
tags: ["React", "React Router","Vite", "JavaScript", "Python", "Pandas","Web Development", "Frontend Development", "HTML", "CSS"]
showToc: false
weight: 202
cover:
    #image: "projects/kindle-to-notion/cover.jpg"
--- 
### 🔗 [GitHub](https://github.com/JakeGerber/LA_Hacks_2023)

## Project Summary
***
No two questions have ever been more relevant in the software dev world than: 

1. Is my data secure ? 

2. Is my job secure ?

Finding the answers may seem difficult, but it does exist: The California WARN Act legally requires employers to disclose to the government when they intend to let go of their employees. The U.S. Department of Health and Human Services (HHS) regularly posts records of large-scale data breaches across the country.

However, both sources are typical of government websites: reliable, but out-of-date with current UI/UX standards. Our aim was to bring the data together into a modern package, to allow software devs to alleviate their concerns with the utmost ease.

### What it does
***
Breach WARNing shows up-to-date information on data breaches and job layoffs that may affect the target user. This information is displayed in a human-friendly format and also shows an infographic on data breaches by state.

### How we built it
***
Data scraping and wrangling was performed using **Python**, where we converted the original Excel files into .JSON where it could be sorted or aggregated. The website was developed using **React**, where data retrieval was conducted locally on-disk. Afterwards the website was deployed on **Netlify**.

## Features
***
- Automatic web scraper grabs WARN data and data breach data every Tuesday and Thursday
- Scripts parse the data into varios JSON objects used in the website
- Users can view aggregate information about the top 3 companies with layoff notices and states affected by data breaches in Layoff-Warn.
- Users can view company information with layoff WARN notices ordered by newest/oldest effective date, number of employees affected, and alphabetically.
- Users can discover more company information along with a map displaying the address in Data breach.
- Users can view a US map displaying state information about data breaches.

## Lessons Learned
***
Built during the **LaHacks Hackathon**, this project involved a team of four individuals. Our primary challenges revolved around merging code seamlessly and avoiding merge conflicts. Combining multiple codebases and aligning our approaches required constant communication and coordination. Through teamwork, we successfully navigated the intricacies of merging code, fostering a cohesive and robust foundation for our project. Additionally, we tackled CSS design issues to ensure consistent component styling. Through effective collaboration, we overcame these obstacles and created BreachWARNING.

### 🔗 [GitHub](https://github.com/JakeGerber/LA_Hacks_2023)
### 🔗 [View Website](https://breachwarning.netlify.app/)