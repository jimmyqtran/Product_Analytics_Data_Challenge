# Product Analytics Data Challenge
A company in the San Francisco Bay Area tasked me with the challenge of analyzing their search and usage data as a part of their hiring process. Though I was unsuccessful in reaching the final round interview, this analysis moved me forward in the interview process. For the purposes of maintaining anonymity, I've changed all mentions of the company's name in my analysis. For my analysis, I've chosen to use R.

# Analysis
[Click here to view the analysis.](https://htmlpreview.github.io/?https://github.com/jimmyqtran/Product_Analytics_Data_Challenge/blob/master/report.html "Analysis") 

## Data and Schema
Two CSV files were provided to me along with the following lists with the name, data structure, and description of each variable.

### Visitors CSV
This dataset contains a list of search results. Each result is a pro that matched a specific visitor’s search.
* `row_number`  (integer): row number in data set
* `visitor_id`  (integer): unique identifier for the visitor that the search result is associated with
* `search_timestamp`  (timestamp): timestamp of when the visitor loaded the search results
* `category`  (string): category of the visitor’s search
* `pro_user_id` (integer): unique identifier for the pro
* `num_reviews` (integer): number of reviews that the pro had at the time of the search
* `avg_rating`  (float): average rating across pro’s reviews
* `pro_last_active_time_before_search`  (timestamp): timestamp of when the pro last
responded to a customer that contacted them, prior to the search_timestamp
* `cost_estimate_cents` (integer): pro’s price estimate for the visitor’s project, in cents. For
House Cleaning searches, this is the price estimate for the entire project. For Local Moving
searches, this is the estimated hourly rate.
* `result_position` (integer): pro’s rank in search results. Rank = 1 means the pro was ranked
first among the search results.
* `service_page_viewed` (boolean): TRUE indicates that the visitor clicked to view the pro’s
profile, FALSE otherwise

### Contacts CSV
This dataset contains a list of customers reaching out to pros. Each row is a visitor that reached out to a
pro through a search in the Visitors CSV.
* `visitor_id`  (integer): unique identifier for the visitor that reached out to the pro
* `pro_user_id` (integer): unique identifier for the pro that the visitor contacted
* `contact_id`  (integer): unique identifier for the visitor-pro contact
* `hired` (boolean): TRUE indicates that the visitor eventually hired the pro, FALSE otherwise
