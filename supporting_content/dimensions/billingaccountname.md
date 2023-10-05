# Column: BillingAccountName

## Example provider mappings

Current column mappings found in available data sets:

| Provider  | Data set                 | Column                                                    |
|-----------|--------------------------|-----------------------------------------------------------|
| AWS       | CUR                      | Not available (bill_payer_account_id maps to BillingAccountId) |
| GCP       | BigQuery Billing Export  | Not available (billing_account_id maps to BillingAccountId) |
| Microsoft | Cost details             | EA: BillingAccountName, MCA: BillingProfileName, MOSA: SubscriptionName |
| OCI       | Cost reports             | Not available (cost/subscriptionId maps to BillingAccountId)

## Documentation

- GCP: [Resource Hierarchy](https://cloud.google.com/resource-manager/docs/cloud-platform-resource-hierarchy#resource-hierarchy-detail)
- Azure: [Organizing resources](https://learn.microsoft.com/en-us/azure/cost-management-billing/manage/view-all-accounts)
- AWS: [Org Concepts](https://docs.aws.amazon.com/organizations/latest/userguide/orgs_getting-started_concepts.html)
- OCI: [Managing your Accounts, Promotions, and Subscriptions](https://docs.oracle.com/en/cloud/get-started/subscriptions-cloud/mmocs/managing-your-accounts-promotions-and-subscriptions.html#GUID-F20286FC-EB1D-4CAA-9232-95D609BAE4FE)

## Example usage scenarios

Current values observed in billing data for various scenarios:
| Provider  | Data set                 | Scenario      | Value              |
|-----------|--------------------------|---------------|--------------------|
| AWS       | CUR                      | Not available |                    |
| GCP       | BigQuery Billing Export  | Not available |                    |
| Microsoft | Cost details             | EA            | BillingAccountName |
| OCI       | Cost reports             | Not available |                    |
