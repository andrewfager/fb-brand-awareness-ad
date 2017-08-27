# Getting Started with Facebook Marketing API 
A step-by-step guide to automatically creating Ads in Python with the Facebook Marketing API. In this guide a 'Brand Awareness' Ad is automatically created in the example ``ad_brand_awareness.py`` code

## Install Marketing API SDK for Python
Use pip to install
```
pip install facebookads
```
See <a href="github.com/facebook/facebook-python-ads-sdk">github.com/facebook/facebook-python-ads-sdk</a> for more information

## Account Setup


### Create App
create a new app at https://developers.facebook.com

![ScreenShot](images/fb-create-app2.png)

### Allow API access to the App
API access to our new app needs to be enabled.  
developers.facebook.com
settings > advanced

![ScreenShot](images/fb-api-access.png)

## Setup
Use sample code to create a brand awareness ad. First fill our 'User Input' section at begining of ``ad_awareness.py``

```
### User Input ###

access_token    = '<ACCESS_TOKEN>'
ad_account_id   = '<AD_ACCOUNT_ID>'
page_id         = '<PAGE_ID>'

img_filename    = '/path/to/local/image.jpg'
link_url        = 'http://www.mylink.com'
link_message    = 'try it out'

campaign_name   = 'My Campaign2'
campaign_status = 'ACTIVE'
campaign_status = 'PAUSED'

adset_name      = 'My Adset'
adset_status    = 'ACTIVE'
adset_status    = 'PAUSED'

ad_name         = 'My Ad'
ad_status       = 'ACTIVE'
ad_status       = 'PAUSED'
```

### Access Token
You'll need to create user access token for input the ```access_token``` variable.  One way to do this is in the graph API explorer.
https://developers.facebook.com/tools/explorer

Select correct app

![ScreenShot](images/fb-access-token-1.png)

Select 'create user access token'

![ScreenShot](images/fb-access-token-3.png)

Make sure permisions are enabled for: 
ads_management, ads_read, read_insights

![ScreenShot](images/fb-access-token-4.png)

Once an access token has been create copy and paste to the ```access_token``` variable.  

### Ad Account ID

You can obtain your Ad Account ID from the Ads manager (https://www.facebook.com/ads/manager/). If not already setup you will need to create an account. Enter ID (as a string) into the the ```ad_account_id``` variable.

![ScreenShot](images/fb-ad-id3.png)


You will also need to link your app and ad account. Enter Ad account ID under app's advanced settings.
![ScreenShot](images/fb-ad-id2.png)

### Page ID

You will need to reference your FB page to create this ad. You can find your page ID by going to the page's 'About' section. Enter ID (as a string) into the the ```page_id``` variable. If you do not have a page you can create one here: https://www.facebook.com/pages/create

![ScreenShot](images/fb-page-id2.png)



Run the python file to automatically create an Ad

```
python ad_brand_awareness.py
```

## Resources
<a href="github.com/facebook/facebook-python-ads-sdk">github.com/facebook/facebook-python-ads-sdk</a>

www.facebookmarketingdevelopers.com
