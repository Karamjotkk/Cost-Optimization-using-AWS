# Cost-Optimization-using-AWS

Identifying Stale EBS Snapshots
This project focuses on cloud cost optimization using AWS services. It automates the process of identifying and deleting unused EBS volume snapshots that can incur unnecessary costs. By utilizing AWS Lambda, Boto3, the solution aims to streamline resource cleanup, improve cost-efficiency, and prevent resource wastage in AWS environments.


The Lambda function fetches all EBS snapshots owned by the same account ('self') and also retrieves a list of active EC2 instances (running and stopped). For each snapshot, it checks if the associated volume (if exists) is not associated with any active instance. If it finds a stale snapshot, it deletes it, effectively optimizing storage costs.
