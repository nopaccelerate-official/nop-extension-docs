# **JAVA Setup**

To set up **SOLR** and **nopAccelerate Plus** on your machine, the first step is to install and configure **Java**.  
Follow the steps below:

---

## 1. Download and Install Java

Download JAVA Latest Version from [here](https://www.java.com/en/download/manual.jsp).

Install the latest Java version.  
You may choose the version as per your system requirements, but we recommend using the **Windows Offline (64-bit)** installer.

After successful installation, you can check the Java installation path:

- **For Windows 32-bit:**  
  `C:\Program Files (x86)\Java`

- **For Windows 64-bit:**  
  `C:\Program Files\Java`

    ![Test](../img/javadownload.png)
---

## 2. Define the `JAVA_HOME` Environment Variable

Defining the `JAVA_HOME` variable helps SOLR locate the Java installation on your machine.

### a) Open Environment Variable Settings

Do one of the following:

- **Windows 7:**  
  Right-click **My Computer** → **Properties** → **Advanced System Settings**

- **Windows 8:**  
  Control Panel → **System** → **Advanced System Settings**

- **Windows 10 / 11:**  
  Search for **Environment Variables** → Select **Edit the system environment variables**

---

### b) Click the **Environment Variables** button.

![Test1](../img/EnvironmentVariable.png)
---

### c) Under **System Variables**, click **New**.

![Test3](../img/Systemvariable.png)
---

### d) Add the JAVA_HOME Variable

- **Variable Name:**  
  `JAVA_HOME`

- **Variable Value:**  
  Add your Java installation path, for example:  
  `C:\Program Files\Java\jre1.8.0_201`

![Test4](../img/JDK_Path.png)
---

Click **OK**.  
You will now see the newly added `JAVA_HOME` variable in the environment variables list.

![Test5](../img/JAVAHOMEinList.png)

You have successfully configured the Java environment variable.

[← Previous](JAVASetup.md) | [Next →](SOLRSetup.md)
