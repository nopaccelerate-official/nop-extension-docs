# Error while performing indexing using DataImportHandler

## **Question**

You receive the following error when trying to index data using **DataImportHandler**:

com.microsoft.sqlserver.jdbc.SQLServerException: The TCP/IP connection to the host localhost, port 1433 has failed.
Error: "Connection refused: connect. Verify the connection properties. Make sure that an instance of SQL Server is
running on the host and accepting TCP/IP connections at the port. Make sure that TCP connections to the port are not
blocked by a firewall."


## **Solution**

Follow the steps below to resolve this issue:

### **1. Open SQL Server Configuration Manager**

Press **Windows Key + R** to open the Run dialog.

### **2. Run the Configuration Manager for your SQL Server version**

Use the appropriate command:

- `SQLServerManager15.msc` → SQL Server 2018  
- `SQLServerManager14.msc` → SQL Server 2017  
- `SQLServerManager13.msc` → SQL Server 2016  
- `SQLServerManager12.msc` → SQL Server 2014  
- `SQLServerManager11.msc` → SQL Server 2012  
- `SQLServerManager10.msc` → SQL Server 2008  

![SQl](../img/sql.png)

> **Note:** If SQL Configuration Manager is not found, verify your SQL Server installation.

---

### **3. Expand: _SQL Server Network Configuration_**

![SQl](../img/serverconfiguration.png)


---

### **4. Enable TCP/IP**

Right-click **TCP/IP** → select **Enable**.

![SQl](../img/tcp.png)

---

### **5. Restart SQL Server Services**

Restart the SQL service so changes take effect.

![SQl](../img/restart.png)



