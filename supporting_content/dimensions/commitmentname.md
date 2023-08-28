# Column: CommitmentName

## Example provider mappings

Current column mappings found in available data sets:

| Provider  | Data set                 | Column                                     |
|-----------|--------------------------|--------------------------------------------|
| AWS       | CUR                      | Not present as a separate column in data.  |
| GCP       | Big Query Billing Export | credits.full_name                          |
| Microsoft | Cost details             | ReservationName (old)<br>BenefitName (new) |


## Documentation

- GCP: [Structure of Standard data export](https://cloud.google.com/billing/docs/how-to/export-data-bigquery-tables/standard-usage), [Committed Use Discounts](https://cloud.google.com/docs/cuds)
- Azure: [Azure Savings Plans](https://learn.microsoft.com/en-us/azure/cost-management-billing/savings-plan/savings-plan-compute-overview), [Azure Reservations](https://learn.microsoft.com/en-us/azure/cost-management-billing/reservations/save-compute-costs-reservations)
- AWS: [Reserved Instances](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-reserved-instances.html), [Savings Plans](https://docs.aws.amazon.com/savingsplans/latest/userguide/what-is-savings-plans.html)


## Example usage scenarios

Current values observed in billing data for various scenarios:

| Provider  | Data set                   | Scenario                                       |
|-----------|----------------------------|------------------------------------------------|
| AWS       | CUR                        | Not present as a separate column in data.      |
| GCP       | Big Query Billing Export   | Examples: "Spend-based committed use discount" |
| GCP       | Big Query Billing Export   | Empty if credits.id is a description type id.  |
| Microsoft | Commitment purchase        | Commitment order name (string)                 |
| Microsoft | Amortized usage            | Commitment instance name (string)              |


## Discussion / Scratch space:

* Discussions on whether this is nullable or not.
* Suggested to follow the same pattern as billingaccountname, resourcename, subaccountname in v0.5.
* Clarification on nullability
  * Should CommitmentId be specified as CommitmentName when name is null (when resource id is not null)
  * Do providers put Id / name for everything?
  * Based on these findings, CommitmentName column cannot be a non-null column
  * See [null_handling](../attributes/null_handling.md) for additional context