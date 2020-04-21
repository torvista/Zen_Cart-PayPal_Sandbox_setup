# Zen Cart - PayPal Express Sandbox setup
How to setup sandbox accounts for development testing of PayPal Express Checkout.

Note that PayPal refers to the API used by Zen Cart as NVP/SOAP.

1.Create sandbox accounts

developer.paypal.com  
Create an account using your real PayPal address (the one you will be using for your shop) & Login.

SANDBOX->Accounts  
You need at least two sandbox accounts:

a) Business type   
which will be the shop sandbox account.

Note the details for this account as they will be used in the ZC Admin configuration for the PayPal payment module:  
API credentials Username  
Password  
Signature  
Account Merchant ID  

Note that in the Settings you can set fault conditions to test error/failed transaction handling later on.

b) Personal type  
which will be a buyer account.  
Create other sandbox personal accounts if you wish to try different buyer characteristics.

Other Sandbox sections (not needed initially)

SANDBOX->Notifications  
Will show transaction info.

SANDBOX->IPN Simulator  
Use the URL in the ZC Admin Payment eg: https://www.mywebsite ipn_main_handler.php
to test communications.

MOCK->Credit Card Simulator
Make a credit card.

MOCK->Negative Testing, goes to API BASICS->Sandbox->Negative Test NVP/SOAP APIs
Has instructions on how to do negative testing.

2.Configure sandbox Business account

sandbox.paypal.com

Login with the sandbox business account email and password.

Account Settings->Account Access->API Access
Paypal API->NVP/SOAP API Integration (Classic)->Manage credentials  
Confirm these are the same as you noted for this account in the developer site.

Account Settings->Business Profile->Business Information  
You can change the name of your store and confirm the Merchant ID.

Account Settings->Instant Payment Notifications  
Turn this on and add the url from the ZC Admin Paypal module.  
eg: https://www.mywebsite ipn_main_handler.php

Account Settings->Products and Services->Website Payments->Website Preferences  
Auto return for website payments.  
eg: https://mywebsite/index.php?main_page=checkout_process

Payment data transfer: On  
PayPal account optional: On  
Return to website  
https://www.motorvista.es/tienda/index.php?main_page=checkout_process

3.Enter sandbox Business credentials in Zen Cart Admin – PayPal Payment module

API credentials Username  
Password  
Signature  
Account Merchant ID

These are fixed, other options are for testing as per your necessities.

Testing
