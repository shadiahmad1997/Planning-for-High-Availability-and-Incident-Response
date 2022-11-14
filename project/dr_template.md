# Infrastructure

## AWS Zones
Identify your zones here
##### us-east-2 region 
###### us-east-2a AZ
###### us-east-2b AZ
###### us-east-2c AZ
  ##### us-west-1 region
###### us-west-1a AZ
###### us-west-1c AZ

## Servers and Clusters

### Table 1.1 Summary
| Asset               | Purpose                                                                                         | Size                                                                   | Qty                                                             | DR                                                                                                           |
|---------------------|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| Asset name          | Brief description                                                                               | AWS size eg. t3.micro (if applicable, not all assets will have a size) | Number of nodes/replicas or just how many of a particular asset | Identify if this asset is deployed to DR, replicated, created in multiple locations or just stored elsewhere |
| Ubuntu-Web          | AWS ec2 instance that host flask app                                                            | t3.micro                                                               | 3                                                               | No DR                                                                                                        |
| udacity-cluster     | AWS EKS cluster for deploy kubernets workload such as prometus,grafana etc                      | -                                                                      | 1                                                               | NO DR                                                                                                        |
| EKS Node            | Amazon EKS managed node groups that is provisioning by udacity-cluster EKS Kubernetes clusters. | t3.medium                                                              | 2                                                               | NO DR                                                                                                        |
| udacity-db-cluster  | RDS data base cluster                                                                           | db.t2.small                                                            | 1                                                               | NO DR                                                                                                        |
| udacity-project VPC | Amazon Virtual Private Cloud for udacity project                                                | -                                                                      | -                                                               | -                                                                                                            |
| Load balancer       | Elastic load balancer for grafana dashboard                                                     | -                                                                      | 2                                                               | NO DR                                                                                                        |







### Descriptions
###### Ubuntu-Web it's a 3 vm's for hosting web flask python app and we installed promethues exporter.
###### udacity-cluster it's AWS EKS cluster and manged by AWS, we deployed the k8s workload on it it's created a cross two region.
###### EKS Node it's eks node group's the number of them two and we can increase them on demand based on the cluster load.
###### udacity-db-cluster it's RDS cluster for hosting the databases it's have two instances across two AZ's one as writer and other for reader and it's replicated to another RDS cluster on diff region 
###### udacity-project VPC have two subnets on two AZ's two public and two private
###### Load balancer load blancer deployed on two AZ's


## DR Plan
### Pre-Steps:
List steps you would perform to setup the infrastructure in the other region. It doesn't have to be super detailed, but high-level should suffice.
###### Determine the needed/critical assets to be deployed on DR region.
###### Ensure that the status of the assets is healthy.
###### Check the patches and updates have been done on DR assets. for example, os upgrade.
###### Prepare or document the manual steps to perform DR plan. for example, changing DNS records.    
###### Ensure both sites are configured the same.
###### Prepare infrastructure as code (IaC) for DR automation.
###### Deploy the terraform on DR region.

## Steps:
You won't actually perform these steps, but write out what you would do to "fail-over" your application and database cluster to the other region. Think about all the pieces that were setup and how you would use those in the other region
###### Check that the All assestes have been deployed successfully on DR site.
###### Check that all assests are healthy on DR site.
###### Manually force the secondary region to become primary at the database level.
###### check that the replica become primary.
###### Point your DNS to your secondary region
