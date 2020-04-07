# Zen Cart - PayPal Sandbox setup
How to setup sandbox accounts for development testing of PayPal Express Checkout

Create sandbox accounts
In developer.paypal.com, create an account using your real PayPal address (the one you will be using for your shop) & Login
In SANDBOX->Accounts

You need at least two sandbox accounts
Business type, which will be the shop sandbox account. Use this account email and password to login to sandbox.paypal.com and make changes as though for your shop details.
Note the details for this account as they will be used in the ZC Admin configuration for the PayPal payment module:
API credentials Username
Password
Signature
Account Merchant ID
Note that in the Settings you can set fault conditions to test error/failed transaction handling.

Personal type, which will be the buyer account. Use this account email and password to login to sandbox.paypal.com and make changes with addresses etc, as though it was a real customer, or create other sandbox personal accounts if you wish to test very different characteristics.

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


Configure sandbox Business account
sandbox.paypal.com
Login with the sandbox business account email and password, as created above.
Account Settings->Account Access->API Access
Paypal API->NVP/SOAP API Integration (Classic)->Manage credentials
Confirm these are the same as you noted for this account in the developer site.
Account Settings->Business Profile->Business Information
You can change the name of your store and confirm the Merchant ID.
Account Settings->Instant Payment Notifications
Turn this on and add the url from the ZC Admin Paypal module: eg: https://www.mywebsite ipn_main_handler.php
Account Settings->Products and Services->Website Payments
Website Preferences
Auto return for website payments: https://mywebsite/index.php?main_page=checkout_process
Payment data transfer: On
PayPal account optional: On
Return to website
https://www.motorvista.es/tienda/index.php?main_page=checkout_process


Enter sandbox Business credentials in Zen Cart Admin – PayPal Payment module
API credentials Username
Password
Signature
Account Merchant ID
These are fixed, other options are for testing as per your necessities

