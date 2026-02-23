Python Visual.md
 What software did you use to create your data visualization?
            Data set: Toronto’s 311 Service Requests – Customer Initiated Dataset 2025
            https://open.toronto.ca/dataset/311-service-requests-customer-initiated/
            
            Python 3.11 with pandas, seaborn, and matplotlib to clean, aggregate, and plot a multi‑series time‑trend for the year. 
            Title: Toronto 311: Top Service Request Types by Month (2025)         

    > Who is your intended audience? 
         
             City operations leaders, councillors, and service managers who need seasonality and workload signals for staffing and vendor planning.

    
    > What information or message are you trying to convey with your visualization? 
        
            Show when the highest‑volume request categories spike during the year (e.g., snow/road, tree maintenance, waste), enabling targeted resourcing and proactive outreach.

           

    > What aspects of design did you consider when making your visualization? How did you apply them? With what elements of your plots? 
            
            Comparability: consistent monthly granularity, same baseline (Jan–Dec).
            Color & accessibility: color‑blind‑friendly palette; line styles + direct labeling so meaning is not conveyed by color alone. Minimum 4.5:1 contrast for text and 3:1 for non‑text UI elements (legend swatches, gridlines), per WCAG guidance. 
            Clarity: thin grid, data‑ink forward, readable tick formatting, legend outside plot on wide screens.

            
    
    > How did you ensure that your data visualizations are reproducible? If the tool you used to make your data visualization is not reproducible, how will this impact your data visualization? 
            Fully scripted—from reading the official 2025 ZIP to export of a PNG—with pinned assumptions and deterministic transforms in a single notebook/script.
            Source URL and snapshot date are documented in comments; running the script on the released 2025 file regenerates the figure exactly.

          
             

    > How did you ensure that your data visualization is accessible?  
           
           High‑contrast labels; color‑blind safe palette; multi‑channel encoding (line style + label).
            Provided machine‑readable alt text template in code for posting to web or LMS; large export (300 DPI).

           

    > Who are the individuals and communities who might be impacted by your visualization?  
          
            Residents reporting issues; operations crews; councillors; neighbourhoods with infrastructure stress.
            Ethical note: avoid implying unmet need equals low request volume—reporting access varies geographically; dataset includes only geospatially validated locations and the five listed divisions

           

    > How did you choose which features of your chosen dataset to include or exclude from your visualization? 

            Included: Service Request Creation Date and Time, Original Service Request Type, Service Request Status (excluding “Canceled”), to reflect public demand; monthly aggregation for comparability.
            Excluded: backend reclassified types to keep the customer’s original problem wording (per dataset notes)

         
    
    > What ‘underwater labour’ contributed to your final data visualization product?
     
           Unzipping & concatenating monthly/partitioned CSVs; coercing timestamps; status filtering; normalizing category labels; handling null wards; verifying duplicates; exporting reproducible artifacts.

           