Tableau Visual 2.md
 What software did you use to create your data visualization?
            Data set: Toronto’s 311 Service Requests – Customer Initiated Dataset 2025            
            https://open.toronto.ca/dataset/311-service-requests-customer-initiated/
            https://ckan0.cf.opendata.inter.prod-toronto.ca/en/dataset/ward-profiles-25-ward-model
            https://ckan0.cf.opendata.inter.prod-toronto.ca/dataset/city-wards
            Visual: https://public.tableau.com/app/profile/b.p8060/viz/Toronto311Requestsper10000ResidentsbyWard2025/Sheet1?publish=yes 
            
            Tableau Public for an interactive ward‑level choropleth; data joins use City ward boundaries (25‑ward model, GeoJSON) and 2021 ward population. 
            title: 311 Requests per 10,000 Residents by Ward (2025)

    > Who is your intended audience? 

             Councillors, city planners, BI teams, and engaged residents comparing request rates across wards.
    
    > What information or message are you trying to convey with your visualization? 

             Where per‑capita demand for City services is highest, after normalizing by population—surfacing hotspots that absolute counts can mask.

    > What aspects of design did you consider when making your visualization? How did you apply them? With what elements of your plots? 

            Normalization: requests per 10,000 residents using 2021 Census ward populations for fair comparisons. 
            Map symbology: quantile bins; color‑blind‑safe sequential palette; tooltips with both rate and count (and top request type).
    
    > How did you ensure that your data visualizations are reproducible? If the tool you used to make your data visualization is not reproducible, how will this impact your data visualization? 
            
            Workbook published to Tableau Public (free) so reviewers can download the data and workbook; however, manual steps (style edits, map projection choices) reduce bit‑for‑bit reproducibility vs. scripted code. I mitigate this by exporting the ward‑level CSV from Python, combining the 2021 population data manually into this excel.
             

    > How did you ensure that your data visualization is accessible?  
           
             Not relying on color only (tooltip text, legend ticks); ensuring contrast of labels and legend meets WCAG 2.2 thresholds
             Adding visual alt text

    > Who are the individuals and communities who might be impacted by your visualization?  
            
             Wards with aging infrastructure or limited digital access may be misrepresented; I include a tooltip disclaimer about coverage (only five divisions; location validation requirement)

    > How did you choose which features of your chosen dataset to include or exclude from your visualization? 

            Included: 2025 counts by Service Request Ward (normalized by 2021 ward population).
            Excluded: fine‑grained point mapping (privacy, over‑interpretation risk) and historical years (scope focus).
    
    > What ‘underwater labour’ contributed to your final data visualization product?
        
            Extracting ward numbers from the dataset’s ward field, deduping name/number variations, verifying the 25‑ward join to GeoJSON, normalizing per‑capita, and documenting the pipeline. Attempted to cleanse the data at the source further to break up the hyphenation of area names like 'scarborough-guildwood' that made it too long to visualize however the source data would corrupt as such this change could not be made. in some cases the boxes do not have room to display the area name because of space limits. Smallest lettering size that could be used and still be legible was size 8.
