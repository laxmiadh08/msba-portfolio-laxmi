### What 3–5 source tables would you expect a real company to use for customer churn? For each source, what does one row represent, for example one customer, one month, one event
  
  Customer Master:
    demographic info (customer_id, signup_date, account_type, region)
  Subscription / Billing History: 
    monthly charges, payment status, plan type
  Activity Logs:
    monthly summary per customer (logins, product interactions, service usage0
  Customer Service Tickets:
    One ticket → complaints, inquiries, resolution times, ticket type

### What keys would you use to connect the data, for example customer_id, account_id, date, etc?
  
customer_id - primary key to link most tables
account_id - if customers have multiple accounts
date or month  - for time-based joins (billing, usage)
ticket_id / campaign_id - to join granular support or marketing events

### What are two risks and how would you reduce them? Examples of risks are duplicates, missing IDs, using information that only exists after churn happens, and definitions changing over time.
Duplicates / multiple records per customer: Deduplicate or aggregate by time window
Missing or inconsistent IDs: Remove or impute missing IDs; enforce referential integrity
Information leak (features only available post-churn): data available before churn date
Changing definitions over time: Track plan or product changes; normalize historical data for consistency


