# Default Configuration – Display Reward Points

This plug-in displays reward points on the **Product Details Page** based on the product price and the reward point configuration set in nopCommerce.

Customers can view how many reward points they will earn before placing an order.

---

## ⚠️ Prerequisite

The plug-in will **not work** if reward points are disabled in nopCommerce.

To enable reward points:

1. Go to  
   **Configuration Management → Settings → Reward Points**
2. Enable **Reward Points**
3. Configure other reward point settings as required.

---

## Steps to Configure Reward Points Display

Follow the steps below to display reward points on the Product Details Page.

---

### Step 1: Open Plugin Configuration

Navigate to:

**Admin → Plugins → Display Reward Points → Configure**

---

### Step 2: Set CSS Selector for Reward Points

Enter the **CSS selector** where reward points should appear.

- Reward points will be displayed **after the selected element** on the product page.

**Example CSS Selector**

```css
.product-price
```

---

### Step 3: Configure Display Content

Add the message you want customers to see in the **Display Content** textbox.

You can customize the content using **HTML** and **inline CSS styles** to match your store theme.

---

## 💡 Important Requirement

It is mandatory to include the keyword below in your content where you want the calculated reward points to appear:

```text
RewardPoints
```

---

### Example Display Message

```html
You will earn %RewardPoints% reward points on this purchase.
```


![Test](../assets/img/DisplayRewardpoint_configure.png)


[← Previous](Licence.md) | [Next →](senerioOfUse.md)