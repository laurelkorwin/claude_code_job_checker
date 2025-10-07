# Overall task summary and goal
Your goal is to search company career pages and find roles that would be a good match for the user given their career profile.
You can find their career profile at ~/cc_jobs_setup/context/career_profile.md.

# Steps to take
1. Look in ~/cc_jobs_setup/context/company_websites.md to find the job pages you should go through (under the heading "Pages to check")
2. For each page, load the page using the playwright mcp server and identify any potential job matches. For each potential match, you should identify the job title and URL to the specific job posting (the href associated with each job). DO NOT try to load individual job pages at this stage. Match to user profile based on role title and department only.
3. Once you have found this information for the given company, close the page with playwright.
4. Identify the company jobs markdown file in ~/cc_jobs_setup/jobs (e.g. acorns.md). It should be the company name in all lowercase. Spaces should be snake_cased. If no markdown file exists for the company, create it.
5. Then, for each potential job match, load the URL you found with your web fetch tool. 
6. If the job is already in the company's markdown file, just leave it and proceed to the next.
7. If it's not in the markdown file, insert it at the top (make sure to leave existing content below):
   - The job title should be a heading
   - There should be a "date found" section with today's date
   - There should be a subheading with salary (if stated), location (if stated) and type (full time, part time, etc.)
   - There should be an overview section with a 1-2 sentence overview of your reading of the job function.
   - There should be a key responsibilities section 
   - There should be a requirements / qualifications section
   - There should finally be a match analysis section where you opine on how good a fit the job would be given the career_profile.
8. DO NOT INCLUDE ANY OTHER ROLES in the company markdown file if you don't think they're a match. We don't need any extra info on roles that don't work. We also don't need any "overall" metadata in the file -- relevant roles and their fields only.