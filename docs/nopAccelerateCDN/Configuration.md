General Tab Configuration:

You need to configure the plugin in the General tab, as shown in the figure below.

**Enable CDN :** Checking this box activates CDN integration for the store. If unchecked, all other settings below are ignored, and assets will be served directly from the application server.

**Is Azure Blob Storage enabled and set as the origin type for the CDN?:** Check this option only if you are storing your media files in Microsoft Azure Blob Storage and using it as the origin source for your CDN. This changes how file paths are generated to be compatible with Azure's container structure.

**Enable CDN for Images:** When enabled, all product images, category icons, and uploaded media will be served from the CDN URL.

**CDN Hostname(s) for Images:** Enter the URL provided by your CDN provider. 
**Note: In the screenshot, the value is set to http://demo.nopcommerce.com/. In a live production environment, this should be your actual CDN endpoint.**

**Enable CDN for CSS:** When checked, the application's stylesheet files (.css) will be loaded from the CDN.

**CDN Hostname(s) for CSS:** Enter the CDN URL for stylesheets. This is usually the same as the image hostname, but can be different if you have a specific sharding strategy

**Enable CDN for JS:** When checked, the application's script files (.js) will be loaded from the CDN.

**CDN Hostname(s) for Js:** Enter the CDN URL for JavaScript files.

**Disable CDN on SSL Pages:** If your CDN provider does not support HTTPS (SSL), enable this option. This ensures that when a user visits a secure page (like Checkout or Login), the assets are loaded from your secure server instead of the non-secure CDN to prevent "Mixed Content" security warnings in the browser.
 
![confgiure](../assets/img/CDN_GenralConfiguration.png)

[← Previous](License.md) | [Next →](DisplyCdnFront.md)