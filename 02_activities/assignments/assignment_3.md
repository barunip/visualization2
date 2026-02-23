# Data Visualization

## Assignment 3: Final Project

### Requirements:
- We will finish this class by giving you the chance to use what you have learned in a practical context, by creating data visualizations from raw data. 
- Choose a dataset of interest from the [City of Toronto’s Open Data Portal](https://www.toronto.ca/city-government/data-research-maps/open-data/) or [Ontario’s Open Data Catalogue](https://data.ontario.ca/). 
- Using Python and one other data visualization software (Excel or free alternative, Tableau Public, any other tool you prefer), create two distinct visualizations from your dataset of choice.  
- For each visualization, describe and justify: 
    > What software did you use to create your data visualization?
            Data set: Toronto’s 311 Service Requests – Customer Initiated Dataset 2025

            1. Python 3.11 with pandas, seaborn, and matplotlib to clean, aggregate, and plot a multi‑series time‑trend for the year. 
            Title: Toronto 311: Top Service Request Types by Month (2025)
            

            2. Tableau Public for an interactive ward‑level choropleth; data joins use City ward boundaries (25‑ward model, GeoJSON) and 2021 ward population. 
            title: 311 Requests per 10,000 Residents by Ward (2025)

    > Who is your intended audience? 
             Pytho Visual 1:
             City operations leaders, councillors, and service managers who need seasonality and workload signals for staffing and vendor planning.

             Tableau Public Visual 2:
             Councillors, city planners, BI teams, and engaged residents comparing request rates across wards.
    
    > What information or message are you trying to convey with your visualization? 
            Pytho Visual 1:
            Show when the highest‑volume request categories spike during the year (e.g., snow/road, tree maintenance, waste), enabling targeted resourcing and proactive outreach.

            Tableau Public Visual 2:
             Where per‑capita demand for City services is highest, after normalizing by population—surfacing hotspots that absolute counts can mask.

    > What aspects of design did you consider when making your visualization? How did you apply them? With what elements of your plots? 
            Pytho Visual 1:
            Comparability: consistent monthly granularity, same baseline (Jan–Dec).
            Color & accessibility: color‑blind‑friendly palette; line styles + direct labeling so meaning is not conveyed by color alone. Minimum 4.5:1 contrast for text and 3:1 for non‑text UI elements (legend swatches, gridlines), per WCAG guidance. 
            Clarity: thin grid, data‑ink forward, readable tick formatting, legend outside plot on wide screens.

            Tableau Public Visual 2:
            Normalization: requests per 10,000 residents using 2021 Census ward populations for fair comparisons. 
            Map symbology: quantile bins; color‑blind‑safe sequential palette; tooltips with both rate and count (and top request type).
    
    > How did you ensure that your data visualizations are reproducible? If the tool you used to make your data visualization is not reproducible, how will this impact your data visualization? 
            Pytho Visual 1:
            Fully scripted—from reading the official 2025 ZIP to export of a PNG—with pinned assumptions and deterministic transforms in a single notebook/script.
            Source URL and snapshot date are documented in comments; running the script on the released 2025 file regenerates the figure exactly.

            Tableau Public Visual 2:
            Workbook published to Tableau Public (free) so reviewers can download the data and workbook; however, manual steps (style edits, map projection choices) reduce bit‑for‑bit reproducibility vs. scripted code. I mitigate this by exporting the ward‑level CSV from Python and documenting join keys and binning thresholds in the README
             

    > How did you ensure that your data visualization is accessible?  
           Pytho Visual 1:
           High‑contrast labels; color‑blind safe palette; multi‑channel encoding (line style + label).
            Provided machine‑readable alt text template in code for posting to web or LMS; large export (300 DPI).

            Tableau Public Visual 2:
             Not relying on color only (tooltip text, legend ticks); ensuring contrast of labels and legend meets WCAG 2.2 thresholds

    > Who are the individuals and communities who might be impacted by your visualization?  
            Pytho Visual 1:
            Residents reporting issues; operations crews; councillors; neighbourhoods with infrastructure stress.
            Ethical note: avoid implying unmet need equals low request volume—reporting access varies geographically; dataset includes only geospatially validated locations and the five listed divisions

            Tableau Public Visual 2:
             Wards with aging infrastructure or limited digital access may be misrepresented; I include a tooltip disclaimer about coverage (only five divisions; location validation requirement)

    > How did you choose which features of your chosen dataset to include or exclude from your visualization? 

            Pytho Visual 1:
            Included: Service Request Creation Date and Time, Original Service Request Type, Service Request Status (excluding “Canceled”), to reflect public demand; monthly aggregation for comparability.
            Excluded: backend reclassified types to keep the customer’s original problem wording (per dataset notes)

            Tableau Public Visual 2:
             Included: 2025 counts by Service Request Ward (normalized by 2021 ward population).
            Excluded: fine‑grained point mapping (privacy, over‑interpretation risk) and historical years (scope focus).
    
    > What ‘underwater labour’ contributed to your final data visualization product?
           Pytho Visual 1: 
           Unzipping & concatenating monthly/partitioned CSVs; coercing timestamps; status filtering; normalizing category labels; handling null wards; verifying duplicates; exporting reproducible artifacts.

           Tableau Public Visual 2:
            Extracting ward numbers from the dataset’s ward field, deduping name/number variations, verifying the 25‑ward join to GeoJSON, normalizing per‑capita, and documenting the pipeline.

- This assignment is intentionally open-ended - you are free to create static or dynamic data visualizations, maps, or whatever form of data visualization you think best communicates your information to your audience of choice! 
- Total word count should not exceed **(as a maximum) 1000 words** 
 
### Why am I doing this assignment?:  
- This ongoing assignment ensures active participation in the course, and assesses the learning outcomes: 
* Create and customize data visualizations from start to finish in Python
* Apply general design principles to create accessible and equitable data visualizations
* Use data visualization to tell a story  
- This would be a great project to include in your GitHub Portfolio – put in the effort to make it something worthy of showing prospective employers!

### Rubric:

| Component         | Scoring  | Requirement                                                                 |
|-------------------|----------|-----------------------------------------------------------------------------|
| Data Visualizations | Complete/Incomplete | - Data visualizations are distinct from each other<br>- Data visualizations are clearly identified<br>- Different sources/rationales (text with two images of data, if visualizations are labeled)<br>- High-quality visuals (high resolution and clear data)<br>- Data visualizations follow best practices of accessibility |
| Written Explanations | Complete/Incomplete | - All questions from assignment description are answered for each visualization<br>- Explanations are supported by course content or scholarly sources, where needed |
| Code              | Complete/Incomplete | - All code is included as an appendix with your final submissions<br>- Code is clearly commented and reproducible |

## Submission Information

🚨 **Please review our [Assignment Submission Guide](https://github.com/UofT-DSI/onboarding/blob/main/onboarding_documents/submissions.md)** 🚨 for detailed instructions on how to format, branch, and submit your work. Following these guidelines is crucial for your submissions to be evaluated correctly.

### Submission Parameters:
* Submission Due Date: `23:59 - 02/23/2026`
* The branch name for your repo should be: `assignment-3`
* What to submit for this assignment:
    * A folder/directory containing:
        * This file (assignment_3.md)
        * Two data visualizations 
        * Two markdown files for each both visualizations with their written descriptions.
        * Link to your dataset of choice.
        * Complete and commented code as an appendix (for your visualization made with Python, and for the other, if relevant) 
* What the pull request link should look like for this assignment: `https://github.com/<your_github_username>/visualization/pull/<pr_id>`
    * Open a private window in your browser. Copy and paste the link to your pull request into the address bar. Make sure you can see your pull request properly. This helps the technical facilitator and learning support staff review your submission easily.

Checklist:
- [ ] Create a branch called `assignment-3`.
- [ ] Ensure that the repository is public.
- [ ] Review [the PR description guidelines](https://github.com/UofT-DSI/onboarding/blob/main/onboarding_documents/submissions.md#guidelines-for-pull-request-descriptions) and adhere to them.
- [ ] Verify that the link is accessible in a private browser window.

If you encounter any difficulties or have questions, please don't hesitate to reach out to our team via our Slack. Our Technical Facilitators and Learning Support staff are here to help you navigate any challenges.
