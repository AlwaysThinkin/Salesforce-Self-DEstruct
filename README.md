Salesforce-Self-DEstruct
========================

A Destructive Package to remove the extra metadata from a Salesforce.com Developer Edition

Much of the metadata that is included in Developer Edition orgs for demonstration purposes can be deleted through the metadata api. However, it has many dependencies. Some of those dependencies can be controlled through the API but some are still only controlled throught the UI.

This project will provide tools for removing the metadata through the API that can be removed, and instructions for removing the metadata through the UI that can only be changed in the UI.

Additionally, there is sample data for which an Apex class can be implemented. After solving the metadata removal, I will be adding a scheduled class that will remove all the data upon install.

The Sample Data consists of:
Opportunities
Contracts
Leads
Cases
Photos
Contacts
Accounts
Solutions
Campaigns

For which the following Apex Code will delete EVERYTHING. This is easiest to run from the Developer Console but I think can be built into an automated script to run on install.

Delete [Select ID from Campaign];
Delete [Select ID from Opportunity];
Delete [Select ID from Contract];
Delete [Select ID from Lead];
Delete [Select ID from Case];
Delete [Select ID from Solution];
Delete [Select ID from Contact];
Delete [Select ID from Account];
Delete [Select ID from FeedItem];

A potential refinement would be to add a filter to the query that matches the record CreateDate to that of the org itself if there is such a global variable.
This would ensure that if the script is run in an org with subsequently added data that only the pre-populated data is deleted.

