# Data Visualization

## Assignment 2: Good and Bad Data Visualization

### Requirements:

- Data visualizations are important tools for communication and convincing; we need to be able to evaluate the ways that data are presented in visual form to be critical consumers of information 
- To test your evaluation skills, locate two public data visualizations online, one good and one bad  
    - You can find data visualizations at https://public.tableau.com/app/discover or https://datavizproject.com/, or anywhere else you like! 
- For each visualization (good and bad):  
    - Explain (with reference to material covered up to date, along with readings and other scholarly sources, as needed) why you classified that visualization the way you did.
      ```
      Your answer...

      Good Visualization: Where On Earth People Aren’t” by Agata Ketterick
        Source: Tableau Public 
        This dashboard visualizes global population density patterns using an interactive heat map and includes written insights.
        A. Why it is good:
        1. Substantive honesty & provenance. The dashboard focuses on a single, well‑defined question—where population density is <1 person/km²—reducing the chance of cherry‑picking or spurious comparisons. It pairs the map with concise written insights, which aligns with best practice to include clear sources/explanations (provenance rhetoric) to bolster perceived objectivity. 
        2. Perceptual clarity. The primary focus is position on a map with a continuous color scale to visualize population sparsity in a low-cognitive‑load manner; this achieves the goal of spatial pattern recognition. 
        3. Aesthetic restraint. Color is limited and functional, avoiding unnecessary 3D or heavy decoration. Typography is readable; visual hierarchy leads with the map, then supporting text/filters—consistent with cognitive‑load heuristics.
        4. Purpose–audience–medium fit. Intended for a broad public audience on the web, the interactive map supports exploration without demanding advanced literacy. 
        5. Reproducibility signals. Access to download/workbook and source notes make it easier to audit methods.

        B. How to improve

        1. Accessibility (color). Offer a color‑blind‑safe sequential palette (e.g., viridis) and ensure sufficient contrast for ramps and overlays
        2. Alternative encodings. Add optional pattern/texture overlays for extreme sparsity so meaning isn’t color‑only
        3. Descriptive text for screen readers. Provide alt‑text and a short data‑rich caption covering levels 2–3 content (summary stats, clusters, exceptions).
        4. Explicit source & method card. Add a “methods” pop‑over describing data vintage, threshold choice, and pre‑processing; this strengthens provenance and reproducibility. [tableau.com]




    BAD Visualization: “People on welfare” vs. “people with full‑time jobs” (2013)
    Source: Media Matters 
    Why it is bad:
    1. Substantive accuracy fails. Context is not normalized. Apples‑to‑oranges comparison. Fox counted “anyone residing in a household with benefits” for the welfare number, but only individuals themselves employed for full‑time work, and many beneficiaries also work—compounding the distortion.
    2. Perceptual framing. Viewers preattentively compare bar heights; truncation creates a large framing effect, the opposite of the “blank page” conventions (2D, clean layout, clear source line) that foster trust. 
    3. Reproducibility & transparency. The broadcast graphic lacks adequate on‑screen methods/source context (definitions, time window, data lineage), failing  reproducibility guidance.
    4. Cognitive load. Minimal labeling plus a deceptive scale increases extraneous load, forcing viewers to mentally reconcile the mismatch between numbers and bars and potentially leading to inccurate results (as likely intended)

    How to improve

    1. Perceptual: Use a zero baseline for bars. Explicitly show absolute and % differences.
    2. Substantive: Align definitions - compare people in households with benefits vs people in households with a full‑time worker, or compare individual beneficiaries vs individual full‑time workers—not mixed units. Cite sources directly on the image. 
    3.Provide context: Small multiples for time (trend), and stratifications beneficiaries (i.e. working beneficiaries) would reduce framing effects and aid interpretation.
    4. Accessibility: Use high‑contrast, readable sans‑serif fonts (≥12pt) and include alt‑text summarizing Level 2–3 content (e.g., “Two bars: 108.6M vs 101.7M; both in 2011; definitions differ”). 

   
      ```
- Word count should not exceed (as a maximum) 500 words for each visualization (i.e. 
300 words for your good example and 500 for your bad example)

### Why am I doing this assignment?:

- This assignment ensures active participation in the course, and assesses the learning outcomes
* Apply general design principles to create accessible and equitable data visualizations
* Use data visualization to tell a story

### Rubric:

| Component               | Scoring   | Requirement                                                 |
|-------------------------|-----------|-------------------------------------------------------------|
| Data viz classification and justification | Complete/Incomplete | - Data viz are clearly classified as good or bad<br />- At least three reasons for each classification are provided<br />- Reasoning is supported by course content or scholarly sources |
| Suggested improvements  | Complete/Incomplete | - At least two suggestions for improvement<br />- Suggestions are supported by course content or scholarly sources |

## Submission Information

🚨 **Please review our [Assignment Submission Guide](https://github.com/UofT-DSI/onboarding/blob/main/onboarding_documents/submissions.md)** 🚨 for detailed instructions on how to format, branch, and submit your work. Following these guidelines is crucial for your submissions to be evaluated correctly.

### Submission Parameters:
* Submission Due Date: `23:59 - 02/16/2026`
* The branch name for your repo should be: `assignment-2`
* What to submit for this assignment:
    * This markdown file (assignment_2.md) should be populated and should be the only change in your pull request.
* What the pull request link should look like for this assignment: `https://github.com/<your_github_username>/visualization/pull/<pr_id>`
    * Open a private window in your browser. Copy and paste the link to your pull request into the address bar. Make sure you can see your pull request properly. This helps the technical facilitator and learning support staff review your submission easily.

Checklist:
- [ ] Create a branch called `assignment-2`.
- [ ] Ensure that the repository is public.
- [ ] Review [the PR description guidelines](https://github.com/UofT-DSI/onboarding/blob/main/onboarding_documents/submissions.md#guidelines-for-pull-request-descriptions) and adhere to them.
- [ ] Verify that the link is accessible in a private browser window.

If you encounter any difficulties or have questions, please don't hesitate to reach out to our team via our Slack. Our Technical Facilitators and Learning Support staff are here to help you navigate any challenges.
