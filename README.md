# FabricAzureDatabricksUCIntegration

![image](https://github.com/mahes-a/FabricAzureDatabricksUCIntegration/assets/120069348/3239573d-47eb-4c7d-8b34-dc5b04e36fed)

##  Proceed with Caution
- Refer to https://learn.microsoft.com/en-us/fabric/onelake/onelake-unity-catalog for the note on Granting users access to Storage, Below is the Note of caution copied from the link
  
  **Granting users direct storage level access to external location storage in ADLS Gen2 does not honor any permissions granted or audits maintained by Unity Catalog. Direct access will bypass auditing, lineage, and other security/monitoring features of Unity Catalog including access control and permissions. You are responsible for managing direct storage access through ADLS Gen2 and ensuring that users have the appropriate permissions granted via Fabric. Avoid all scenarios granting direct storage level write access for buckets storing Databricks managed tables. Modifying, deleting, or evolving any objects directly through storage which were originally managed by Unity Catalog can result in data corruption.**

- Databricks doesn’t recommend using mount points, service principals or credential passthrough; instead, Unity Catalog is suggested. This is a temporary solution until Unity catalog  OneLake direct integration is completed , creating external locations (+volumes) to OneLake are not yet possible.

## Read Fabric Mirrored warehouse in UC enabled Azure Databricks

- Refer to  [Reading Fabric Warehouse items](https://github.com/mahes-a/FabricAzureDatabricksUCIntegration/blob/main/FabricOnelakeDataIntegrationwithUnityCatalog.ipynb)


## Create Fabric Lakehouse shortcuts from  Unity Catalog Azure Databricks

- Once previous step is completed Refer to https://learn.microsoft.com/en-us/fabric/onelake/onelake-unity-catalog
