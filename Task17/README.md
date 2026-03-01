# Task 17: DynamoDB Table Creation (Basic)

## Objective
To learn serverless database basics by provisioning a NoSQL table using Amazon DynamoDB.

## Implementation Steps

### 1. Table Provisioning
- Navigated to the Amazon DynamoDB console and initiated the creation of a new NoSQL table.
- Named the table `ProductCatalog` and defined `ProductID` (String) as the primary Partition Key to uniquely identify each record.
- Utilized default capacity and routing settings for a standard serverless deployment.

### 2. Data Insertion (Item Creation)
- Accessed the 'Explore items' interface to manually populate the database.
- Inserted multiple sample items into the table, demonstrating the flexible schema nature of NoSQL by adding a `ProductName` attribute to the items.

## Proofs of Completion
- dynamodb_table_active.png: Screenshot of the DynamoDB console showing the successful creation and 'Active' status of the table.
- dynamodb_items.png: Screenshot of the 'Explore items' view displaying the successfully inserted sample records.