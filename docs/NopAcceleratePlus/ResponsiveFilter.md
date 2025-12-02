# Responsive Filter Not Working with nopTemplate Theme

## **Question**
Responsive filters of **nopAccelerate Plus** are not working with **nopTemplate** themes?

## **Solution**
If the responsive filter isn't working with a nopTemplate theme, apply the CSS updates below.

---

## **CSS Changes → Themes**

If you're using any of these nopTemplate themes, follow **Section 1**:

- Lighthouse  
- Alfresco  
- Jewelry  
- NeoFashion  
- Beauty  
- Fashion  
- Electronics  
- Shop All  

---

## **UI Changes → Themes → Section 1**

### File: `nopaccelerate-style.min.css`

- Replace **`max-width:1000px`** with **`max-width:767px`**
- Replace **`min-width:1001px`** with **`min-width:768px`**

### File: `nopaccelerate-style.rtl.min.css`

- Replace **`max-width:1000px`** with **`max-width:767px`**
- Replace **`min-width:1001px`** with **`min-width:768px`**

---

If you're **not** using any of the themes listed above, apply **Section 2**.

## **UI Changes → Themes → Section 2**

### File: `nopaccelerate-style.min.css`

- Replace **`max-width:1000px`** with **`max-width:1024px`**
- Replace **`min-width:1001px`** with **`min-width:1025px`**

### File: `nopaccelerate-style.rtl.min.css`

- Replace **`max-width:1000px`** with **`max-width:1024px`**
- Replace **`min-width:1001px`** with **`min-width:1025px`**


[← Previous](LicensingIssues.md) | [Next →](FontError.md)