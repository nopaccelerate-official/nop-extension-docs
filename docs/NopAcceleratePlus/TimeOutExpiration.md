# TimeOut Expiration Error on Plugin installation

## **Question**

I am getting the following error while installing the plugin:

Timeout expired. The timeout period elapsed prior to completion of the operation
or the server is not responding

---

## **Cause of the Problem**

This issue occurs when there is a **large amount of data**, and during plugin installation the system attempts to create the **Incremental_Table**.

While doing so, the stored procedure:

NopAcc_Plus_ManageIncrementalSolrProductTable

takes too long to execute and results in a timeout.

---

## **Solution**

Follow the steps below:

1. Open the file:  
   **Plugin > NopAcceleratePlus.Search > SqlScript > Sp_SolrInstall.sql**

2. **Remove** the following line from the script:

EXEC NopAcc_Plus_ManageIncrementalSolrProductTable


3. Manually execute the stored procedure directly in SQL Server:


4. After the stored procedure completes successfully,  
**install the plugin again**.

[← Previous](CreateCore.md) | [Next →](Category&ManufacutreNavigation.md)