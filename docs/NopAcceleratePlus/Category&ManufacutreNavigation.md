# Category and Manufacturer Navigation not working

## **Question**

Category and Manufacturer Navigation are not working on our store.

---

## **Cause of the Problem**

The `currentCategoryId` parameter used to invoke the **CategoryNavigation ViewComponent** is always `0` when using **nopAccelerate Plus**.

This happens because the controller name is **not** `catalog` anymore —  
nopAccelerate Plus **overrides** the default Catalog controller.

As a result, the navigation components do not receive the correct category context.

---

## **Solution**

You need to update the controller reference in your NopCommerce theme file.

### **Steps**

1. Open the file:  
   **_ColumnsTwo.cshtml**

2. Replace the controller name with **NopAcceleratePlusWebCatalog** This will correctly load **CategoryNavigation** and **Manufacturer Navigation** while using the nopAccelerate Catalog Plugin. 
