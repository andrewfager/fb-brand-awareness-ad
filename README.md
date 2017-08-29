# A Getting Started Guide to the Facebook Marketing API 
A step-by-step guide to automatically creating Ads in Python with the Facebook Marketing API. This guide provides a sample python code (``ad_brand_awareness.py``) that creates a 'Brand Awareness' Ad.

## Install API
Install Marketing API for Python with pip
```
pip install facebookads
```
See <a href="github.com/facebook/facebook-python-ads-sdk">github.com/facebook/facebook-python-ads-sdk</a> for more information on installation.

## Setup


### App
You will need a Facebook App. Create a new app at https://developers.facebook.com

<img src="images/fb-create-app2.png" width="650">

API access to the app needs to be enabled. This can be done under the App's advanced settings

<img src="images/fb-api-access.png" width="650">


### Ad Account

If not already setup you will need to create an Ad account. This can be done at: https://www.facebook.com/ads/manager/

### Page

The ad needs to reference a Facebook page. If you do not have a page you can create one here: https://www.facebook.com/pages/create

## User Input

Before running ``ad_awareness.py`` fill out the ``### User Input ###`` section at the top of the code  

### Access Token

Enter access token (as a string). 
```
access_token    = '<ACCESS_TOKEN>'
```

To create one you can use the graph API explorer.
https://developers.facebook.com/tools/explorer. Select app

<img src="images/fb-access-token-1.png" width="650">

Select 'get user access token'

<img src="images/fb-access-token-3.png" width="650">

Make sure permisions are enabled for: 
``ads_management``, ``ads_read``, ``read_insights``

<img src="images/fb-access-token-4.png" width="650">

copy and paste into ```access_token``` variable.  

### Ad Account ID

Enter ad account ID (as a string). 
```
ad_account_id   = '<AD_ACCOUNT_ID>'
```

You can obtain your Ad Account ID from the Ads manager (https://www.facebook.com/ads/manager/).

<img src="images/fb-ad-id3.png" width="400">


### Page ID

You will need to input your FB page ID  (again, as a string).
```
page_id         = '<PAGE_ID>'
```

You can find your page ID by going to the page's 'About' section. 

<img src="images/fb-page-id2.png" width="650">


### Campaign/Adset/Ad Settings
These are settings such as naming, targeting, budget, etc. For this example you can keep the defaults and succesfully create an Ad. 

Active status is specified using the ```campaign_status```/```adset_status```/```ad_status``` variables. To prevent any charges from being incurred the Campaign, Adset & Ad are all paused when initially created. 


These Ad Settings are required input:
```
img_filename    = '/path/to/image.jpg'    #local image path to be uploaded by the API.
link_url        = 'http://www.mylink.com' #link to your brand's website.
```

### Link App & Ad Account
One last step, you will also need to link your app and ad account. At https://developers.facebook.com enter Ad account ID under app's advanced settings.

<img src="images/fb-ad-id2.png" width="650">

## Create Ad

Now it's time to automatically create an ad using the API
```
python ad_brand_awareness.py
```

Verify ad created successfully by checking that it appears in the Ads Manager (https://www.facebook.com/ads/manager/)


## Resources
<a href="github.com/facebook/facebook-python-ads-sdk">github.com/facebook/facebook-python-ads-sdk</a>

www.facebookmarketingdevelopers.com
