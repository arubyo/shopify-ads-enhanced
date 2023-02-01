GTM / Tag Manager Installation or Modification Shopify

Add UA to preferences in Shopify and turn on Ecommerce

Create a Snippet 
Snippet: Online Store > Themes > ... > Edit HTML/CSS > Snippets > Create New
Name is dataLayer-allPages

Paste in dayaLayer-allPages (remember to change GTM)

Within the theme.liquid layout, place the datalayer snippet directly before the closing <head>.
{% include 'dataLayer-allPages' %}

Within the confirmation page the checkout-section (remember to change GTM)

