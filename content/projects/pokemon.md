---
title: "Pokemon Card Dashboard"
#description: "Users can view card information about the Crown Zenith deck series."
dateString: "April 2023 ∙ "
ShowWordCount: true
ShowReadingTime: true
author: Gabriela Liera
draft: false
tags: ["JavaScript", "React", "API", "React Router", "Web Development", "Frontend Development", "HTML", "CSS"]
showToc: false
weight: 203
cover:
    image: "projects/pokemon/cover.png"
    alt: "Web - Users can view card information about the Crown Zenith deck series."
--- 
### 🔗 [GitHub](https://github.com/gabrielaliera/data-dashboard)

## Project Summary
***
The "Pokemon Card Dashboard" is a web app that provides a platform for displaying valuable information about the latest Pokemon deck series. It is built with **React** and uses the PokemonTCG API to fetch card and deck information.

![Walkthrough of Project](/walkthrough.gif)

## Features
***
- Users can view a list displaying data fetched using an API call
- Data uses the useEffect React hook and async/await syntax
- The app dashboard includes at least three summary statistics about the data such as:
    - Image
    - Name
    - Different market prices
- A search bar allows the user to search for an item in the fetched data
- Multiple different filters (2+) allow the user to filter items in the database by specified categories
- Clicking on an item in the list view displays more details about it
- Clicking on an item has a direct, unique link to that item's detail view page
- Multiple filters can be applied simultaneously
- Filters use different input types such as a text input, a selection, or a slider
- The user can enter specific bounds for filter values

## Lessons Learned
***
During the course of this project, I encountered several challenges that tested my skills and problem-solving abilities. One significant hurdle I faced was the learning curve associated with React Router. Understanding how to effectively utilize React Router to manage routing within the application required dedicated effort and research.

Another challenge arose when I needed to conditionally render specific data related to card information. Determining the appropriate logic and structure to display the desired information based on certain conditions was a complex task. It involved careful consideration of the data available and creating conditional rendering statements that accurately represented the desired outcome.

Additionally, the project involved retrieving deck information, including details about crown zenith and individual card data. However, this required making two separate API calls. Overcoming this challenge involved finding a way to combine these calls into a single fetch request, optimizing efficiency and reducing unnecessary network requests.

Lastly, implementing the search feature posed its own set of challenges. Developing a robust search functionality that effectively filtered and displayed relevant results required thoughtful consideration of the search algorithm, user experience, and handling various edge cases.

Despite these challenges, I persevered and gained valuable insights and experience. Through active problem-solving and a commitment to continuous learning, I successfully navigated these obstacles and delivered a functional and robust solution.

### 🔗 [GitHub](https://github.com/gabrielaliera/data-dashboard)
