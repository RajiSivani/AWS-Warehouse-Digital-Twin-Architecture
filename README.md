# AWS Warehouse Digital Twin Architecture

## Overview

This project designs an AWS-based digital twin architecture for warehouse equipment monitoring, inventory visibility, predictive maintenance, and operational analytics. The goal is to create a cloud-powered virtual representation of warehouse operations using IoT sensor data, streaming pipelines, machine learning, and business intelligence dashboards.

The solution focuses on helping warehouse teams monitor equipment health, track inventory status, detect anomalies, reduce downtime, and make faster data-driven operational decisions.

## Business Problem

Many warehouse systems operate in silos, making it difficult to monitor equipment, inventory, and workflow performance in real time. This can lead to delayed maintenance, inaccurate inventory records, inefficient routing, downtime, and reactive decision-making.

This project addresses the problem by proposing a digital twin architecture that connects IoT sensor data, cloud processing, predictive analytics, and visual dashboards into one integrated AWS solution.

## Proposed Solution

The architecture uses AWS services to support real-time data ingestion, processing, storage, digital twin synchronization, predictive analytics, alerting, and reporting.

Key capabilities include:

* Real-time equipment and inventory monitoring
* IoT sensor data ingestion and stream processing
* Predictive maintenance using machine learning
* Digital twin visualization of warehouse assets
* Operational dashboards for equipment health and inventory accuracy
* Alerting for anomaly detection and maintenance risks
* Scalable and secure cloud architecture

## Architecture Components

The proposed architecture includes the following AWS services:

* **AWS IoT Core** for secure IoT device connectivity
* **AWS IoT Greengrass** for edge preprocessing and buffering
* **Amazon Kinesis** for real-time streaming data ingestion
* **AWS Lambda** for event-driven data transformation and anomaly checks
* **Amazon S3** for raw and historical IoT data storage
* **Amazon DynamoDB** for structured equipment and status data
* **AWS IoT SiteWise** for industrial asset modeling and time-series data organization
* **AWS IoT TwinMaker** for digital twin visualization
* **Amazon SageMaker** for predictive maintenance modeling
* **Amazon SNS** for alert notifications
* **Amazon QuickSight** for operational dashboards
* **Amazon CloudWatch** for monitoring logs, metrics, and alarms
* **AWS IAM, KMS, and CloudTrail** for access control, encryption, and audit tracking

## Data Flow

1. IoT sensors collect warehouse equipment and inventory data such as temperature, vibration, energy usage, and stock movement.
2. AWS IoT Greengrass performs local preprocessing and buffering at the edge.
3. AWS IoT Core securely sends telemetry data to the cloud.
4. Amazon Kinesis streams the incoming data for near real-time processing.
5. AWS Lambda cleans, transforms, and validates incoming records.
6. Processed data is stored in Amazon S3, DynamoDB, and AWS IoT SiteWise.
7. AWS IoT TwinMaker updates the virtual warehouse representation using live operational data.
8. Amazon SageMaker supports predictive maintenance and anomaly detection workflows.
9. Amazon SNS sends alerts when risk conditions are detected.
10. Amazon QuickSight provides dashboards for warehouse managers and operations teams.

## Cost and Scalability Estimate

The architecture was evaluated for a mid-sized warehouse with approximately **500 IoT sensors** transmitting data every **10 seconds**, producing around **129 million messages per month**.

Estimated monthly cloud cost:

| Category                         |   Estimated Cost |
| -------------------------------- | ---------------: |
| AWS IoT Core                     |             $215 |
| Amazon Kinesis                   |             $150 |
| AWS Lambda                       |              $25 |
| Amazon DynamoDB                  |              $85 |
| Amazon S3                        |              $55 |
| AWS IoT SiteWise                 |             $135 |
| AWS IoT TwinMaker                |             $180 |
| Amazon SageMaker                 |             $310 |
| Amazon QuickSight                |              $70 |
| AWS CloudWatch                   |              $40 |
| Amazon SNS                       |               $5 |
| **Total Estimated Monthly Cost** | **$1,270/month** |

The architecture can be optimized further using IoT message batching, S3 Intelligent Tiering, on-demand SageMaker endpoints, AWS Budgets, and Cost Explorer.

## Expected Business Impact

The proposed digital twin solution is designed to support:

* **28–35% reduction** in unplanned equipment downtime
* **95–99% inventory synchronization** between physical stock and digital records
* **25–30% faster order processing**
* **18–22% energy savings**
* **15–18% annual operational cost reduction**
* Improved visibility into warehouse performance and asset health

## My Contributions

This was completed as an academic cloud architecture project. My major contributions included:

* Defining business and user requirements for warehouse monitoring and inventory optimization
* Designing the AWS digital twin architecture and service-level data flow
* Mapping IoT sensor data movement from edge devices to cloud analytics layers
* Evaluating AWS services for ingestion, processing, storage, digital twin modeling, ML, alerts, and dashboards
* Estimating cost and scalability for a 500-sensor warehouse environment
* Documenting architecture trade-offs, expected outcomes, and future improvements

## Repository Contents

```text
AWS-Warehouse-Digital-Twin-Architecture/
│
├── Warehouse_Digital_Twin_FinalReport.pdf
├── Warehouse_Digital_Twin_Proposal.pdf
└── README.md
```

## Project Type

This is an architecture and cloud design project. It focuses on solution design, AWS service selection, cost estimation, scalability analysis, and operational impact rather than deployed production code.

## Future Improvements

Future work can include:

* Simulating IoT sensor data using Python
* Building a proof-of-concept AWS Lambda ingestion workflow
* Creating a sample DynamoDB schema for equipment status data
* Developing a QuickSight dashboard mockup
* Adding predictive maintenance model examples using SageMaker
* Extending the design to support multiple warehouses
