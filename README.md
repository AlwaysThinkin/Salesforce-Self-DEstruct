Salesforce-Self-DEstruct
========================

A Destructive Package to remove the extra metadata from a Salesforce.com Developer Edition

Much of the metadata that is included in Developer Edition orgs for demonstration purposes can be deleted through the metadata api. However, it has many dependencies. Some of those dependencies can be controlled through the API but some are still only controlled throught the UI.

This project will provide tools for removing the metadata through the API that can be removed, and instructions for removing the metadata through the UI that can only be changed in the UI.

Additionally, there is sample data for which an Apex class can be implemented. After solving the metadata removal, I will be adding a scheduled class that will remove all the data upon install.

