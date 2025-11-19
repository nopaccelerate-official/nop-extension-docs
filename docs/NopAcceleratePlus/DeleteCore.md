You can delete core using the **delete** command of Apache Solr.

Let’s suppose we have a core named **my_core** in Solr, as shown below :

![Test1](../img/deletingcore.jpg)


You can delete this core using the **delete** command by passing the name of the core to this command as follows :

**solr delete -c my_core -p 8983**

On executing the above command, the specified core will be deleted displaying the following message.

![Test2](../img/deletecommand.png)

You can open the web interface of Solr to verify whether the core has been deleted or not.

![Test3](../img/Check_deleted.jpg)

[← Previous](DeleteCore.md) | [Next →](ReloadCore.md)