# Using Solr as a service in Windows Server

## **Question**

How can I run Solr as a **Windows service** on a Windows Server?

---

## **Solution**

To run Solr as a Windows service, follow the official guidelines provided here:

**(Insert your Solr service setup link here)**

This guide explains how to install, configure, and manage Solr so it runs as a background service.

---

## Things to Take Care Of

- **Solr should not stop when you log off** from the system.  
  Running it as a service ensures it stays active even after user logout.

- **Solr must start automatically after system restart**.  
  Make sure the service startup type is set to **Automatic**, and it restarts on the same port you configured.

