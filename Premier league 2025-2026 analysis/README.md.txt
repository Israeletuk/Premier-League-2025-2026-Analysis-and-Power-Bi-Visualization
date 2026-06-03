# Premier League 2025/2026 Season Analysis

![Dashboard Canvas](assets/dashboard_screenshot.png)

## Project Overview
This Power BI dashboard was built to analyze the entire 2025/2026 Premier League season. Instead of just dragging and dropping basic totals, the goal was to focus on clean data analysis, proper table relationships, and creating a UI that looks like an official Premier League application rather than a default spreadsheet.

## Data Modeling & Engineering
The biggest challenge with the raw data was how match statistics are split into independent Home and Away columns. Trying to filter or combine these natively creates relationship loops and many-to-many filtering errors.

To solve this properly, the analyst:
* Built a standalone master Clubs dimension table containing a unique list of all teams.
* Created clean, one-to-many paths to the main data table.
* Used the TREATAS function in my DAX measures to dynamically map filter contexts across tables without having to alter the physical dataset structure.
* Wrote custom logic to prevent Power BI from automatically truncating large numbers into messy "1K" labels, keeping the numbers exact.

## Key Insights From the Data
The calculations and measures I set up surfaced some great trends from the 2025/2026 season:
* Arsenal won the league title, leading the pack with 85 points and 26 wins.
* Bournemouth became the ultimate stalemate team, hitting a high of 18 full-time draws.
* Tottenham Hotspur showed the highest-risk defensive style, racking up 104 total disciplinary cards.
* Burnley and Wolves struggled the most with resilience, both dropping a league-high 24 matches.

## Design & UI Choices
The analyst deliberately moved away from default Power BI styling to make the dashboard look like a premium sports app:
* Home Stadium Performance: A 100% stacked bar chart that isolates matches played inside each team's own stadium. This clearly shows who made their home ground a fortress versus who collapsed under pressure.
* Halftime vs. Fulltime Shifts: A customized Ribbon Chart that tracks momentum. By mapping the halftime state against the final whistle, it shows which teams made great second-half adjustments and who let leads slip away.
* Official Visual Branding: Used exact Premier League hex color codes including #3D195B (Deep Purple) and #00FF87 (Neon Cyan) on a soft gray background. 
* Clean Formatting: Analyst removed the default, repetitive "Total" summary rows from the tables to save vertical space and used rounded corners on the cards for a modern look.

## How to View the Project
* PDF Version: If you don't have Power BI installed, you can open the dashboard folder and download the PL_Dashboard_Portfolio.pdf file to see a high-quality export[cite: 1].
* Power BI File: To inspect the actual relationships, model schema, and DAX formulas, clone the repository and open the PL_Season_Analysis_2026.pbix file in Power BI Desktop.

## Developed by
* Analyst Israel