# How can I search with synonyms?

## **Question**

I have products with the name **"Laptop"**, and the user types **"NoteBook"** in the search box.  
I want the search results to show **Laptop** products when someone searches for "NoteBook".  
How can I configure this in Solr, and which file should I modify?

---

## **Solution**

You need to add synonym mapping inside the **synonyms.txt** file.

### **1. Locate the synonyms file**

You can find it here:

C:\solr-6.4.2\server\solr<YourCoreName>\conf\synonyms.txt

---

### **2. Add your synonym rule**

Append the following line at the end of the file:


This tells Solr that searching for **NoteBook** should return results for **Laptop**.

---

### **3. Reload your Solr Core**

> **Important:** After modifying the synonyms file, you must **reload the core** for the changes to take effect.

