# Commitment Discount ID

A commitment-based discount is a contractual commitment to use a certain amount of a specific type of usage for a fixed term in exchange for a discounted unit price. Commitment-based discounts can cover either usage or cost of various resources such as virtual machines or databases. A provider can offer various pricing models, payment options, and term durations for commitment-based discounts.

A Commitment Discount ID is the identifier assigned to a commitment-based discount by the provider. Commitment Discount ID is commonly used for scenarios like calculating utilization and savings per commitment-based discount.

The CommitmentDiscountId column MUST be present in the billing data. This column must be of type String and MUST NOT contain null values when a charge is related to a commitment-based discount. When a charge is not associated with a commitment-based discount, the column MUST be null. CommitmentDiscountId MUST be unique within the provider.

## Column ID

CommitmentDiscountId

## Display name

Commitment Discount ID

## Description

The identifier assigned to a commitment-based discount by the provider.

## Content constraints

|    Constraint   |      Value       |
|:----------------|:-----------------|
| Column required | True             |
| Data type       | String           |
| Allows nulls    | True             |
| Value format    | \<not specified> |

## Introduced (version)

1.0