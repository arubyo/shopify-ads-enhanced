FORKED FROM: https://github.com/TechnicalWebAnalytics/dataLayer-shopify

This is a GTM set up of enhanced ecommerce tracking for Shopify. 
It includes UA, GA4 and Google Ads - all from GTM. 

For all ecommerce tracking, ensure the below is completed prior to set up;
1. Add UA to preferences in Shopify and turn on Ecommerce in UA settings
2. Make sure ecommerce settings are switched on for UA 
3. If both UA and GA4 coexist, the accounts should NOT be connected in the UA admin settings. GA4 will be getting data from GTM directly. 

There are three different folders for three different variations of GTM containers, there are different requirements to set up shopify ecommerce tracking. All include a basic GA4 and UA container
1. [shopify ads] 
includes a GTM container that tracks, enhanced user conversions on the purchase event for google ads 
2. [shopify-ads-googleapp]
this is still google ads enhanced user conversions on the pruchase however, if shopify account uses the free Google app, it will send through datalayer events automatically and duplicate events (view_item, add_to_cart, purchase). this container separates the duplicates, changes the tag to fire once per page
3. [shopify-analytics]
this set up is pure UA and GA4 enhanced ecommerce 


All containers follow the below set up guide
**Add the GA4 datalater to all pages**
1. Create a new snippet in the Shopify code files
2. Online Store > Themes > Edit Code > Snippets > Create New
3. Name the new snipper **dataLayer-allPages**
5. Copy & paste the dataLayer-allPages script file 
5. Update the GTM variable at the end of the file

**Add the snippet to the theme.liquid**
Within the theme.liquid layout, place the datalayer snippet directly before the closing <head>. 
{% include 'dataLayer-allPages' %}
  
**Add script to checkout page, change the GTM at the bottom**  
Settings -> Checkout and accounts -> Scroll to bottom to find 'Order status page'
Copy & paste in the checkout-section
Update the GTM variable at the end of the script
  
**Import container into GTM**
1. Change UA Constant, Variables -> UA Constant
2. GA4 Constant, Tags -> GA4 Configuration 
3. If required update the Google Ads tags, there are 2 that need to be updated. Gads User Data and GAds Purchase Tag. 
Test and confirm the data is coming through GA4 correctly. 
  
  

