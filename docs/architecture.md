# Proposed AWS architecture

| Service | Role |
|---|---|
| S3 and Lambda | Sales exports stored per retailer, aggregated to SKU and week on arrival |
| SageMaker AI | Demand forecasts per SKU, retrained weekly |
| Bedrock | Plain summaries of seasonal changes for buyers |
| DynamoDB | SKUs, suppliers, reorders and the approval log |

One AWS account per customer, encrypted at rest and in transit. The public demo calls none of these services.
