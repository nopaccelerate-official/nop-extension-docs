# Setup core if your Solr is hosted on a shared server

If you are using a **Shared Server** for Solr, you need to perform additional setup steps for the Solr Core.

---

## Steps

### **1. Configure Solr Core URL**
- Enter the **remote Solr server URL** in the *Solr Core URL* field.
- Save the configuration page.

### **2. Run Core Setup**
- Click **Core Setup**.
- It may take some time.
- After completion:
  - ✔ Managed Schema  
  - ✔ Core Stream Body  
  - ✔ Pattern Handler  
  - ❌ DB Config File  
  - ❌ Request Handler  
- The red cross icons indicate some manual setup is required.

---

## Manual Setup Steps for Remote Solr Hosting

### **1. Download required setup files**
- Go to: **nopAccelerate Plus → nopAccelerate+ Search → Configure**
- Find **Setup files download**
- Click the download button to get a ZIP containing required files.

### **2. Copy configuration files**
Unzip the file — you will find **3 files**:

- `db-data-config.xml`
- `solrconfig.xml`
- `synonyms.txt`

Copy these files into the **conf** folder of your Solr data directory.

After copying, **Reload the Core** from Solr Admin.

---

### **3. Install Microsoft JDBC Driver**
Solr needs the MS SQL JDBC driver to connect to SQL Server.

- Copy the file: `sqljdbc42.jar`
- Paste it into Solr’s **dataimporthandler/lib** folder.

Example (Windows):
C:\solr-7.5.0\contrib\dataimporthandler\lib

Create the folder if it does not exist.

---

### **4. Reload Core from nopAccelerate**
- Go back to the plugin **Configure** page.
- Click **Reload** to apply all manual changes.

---

### **5. Verify Core Setup**
Return to **Core Setup**:
- This time the **Request Handler** should show ✔ **correctly done**.
- Manually update `DbConfigFileStatus` to **true**.
- Perform **Indexing**.

If indexing works successfully, your **remote Solr core setup is complete**.
