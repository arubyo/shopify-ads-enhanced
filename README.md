GTM / Tag Manager Installation or Modification Shopify, this includes both GA4, UA and Google Ads Enhanced 

Add UA to preferences in Shopify and turn on Ecommerce in UA settings

**Add the GA4 datalater to all pages**
In Shopify Account, Theme, Create a Snippet 
Snippet: Online Store > Themes > ... > Edit HTML/CSS > Snippets > Create New
Name is dataLayer-allPages
Change the GTM at the bottom of the file 
Paste in dataLayer-allPages file & (remember to change GTM)

**Add the snippet to the theme.liquid**
Within the theme.liquid layout, place the datalayer snippet directly before the closing <head>. 
{% include 'dataLayer-allPages' %}
  
**Add script to checkout page, change the GTM at the bottom**  
Within the confirmation page the checkout-section (remember to change GTM)
  
**Import container into GTM**
Change UA Constant and GA4 Constant 
Test and confirm the data is coming through GA4 correctly. 
  
  
  -remove Gads if needed.
