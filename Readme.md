# Teams:
- **UI/UX**: Nathalie, Aline, Sheyla
- **Dev**: Bruno, Tony, Emerson, Plinio, Fernando, Mariana
- **Support**: Murilo ...

---
# Proposed tech

## Endpoints
- api.adoptmyshop.org - Api for data manipulation - DB Read/ Write
- admin.adoptmyshop.org - Private UI for data management
- dev.adoptmyshop.org - Public UI for client access

## Components
- Database: https://www.mongodb.com/
- Authetication: https://auth0.com (JWT token)

## Tech stack:
- [API](https://github.com/IT-in-Canada/adoptmyshop-api): node, express, jwt, mongoose (maybe just mongod)
- [Admin](https://github.com/IT-in-Canada/adoptmyshop-admin): react, sass, bootstrap - not necessarly need to be responsive

- [Web Client](https://github.com/IT-in-Canada/adoptmyshop-web): 
    1. Create a "widget like" structure, so that the existing UI can fetch data from our API and display on WP
        *e.g: city: api.adoptmyshop.org/cities*
    2. New UI: react, sass, bootstrap
            
## Pseudo DB Schema:

### Shops Schema

```json
    [{
        "shop": {
            "business_name": "3 Quarters Full Cafe",
            "business_address": "1789 Comox Street",
            "business_city": "Vancouver",
            "business_province": "British Columbia",
            "business_zip_code": "F5H 3S6",
            "business_country": "CA",
            "business_phone": "123123",
            "business_email" "contact@3quarters.ca"
            "business_description": "It may be called 3 Quarters Full, ...",
            "business_tags": ["delivery", "pickup","taiwanese"],
            "active": true,
            "featured_image": "",
            "images": [],
            "support_sales_options": [{
                "type": "gitfcard",
                "link": "https://www.instagram.com/3quartersfullcafe/"
            },{
                "type": "online_order",
                "link": "https://www.instagram.com/p/B97b-E9hBOg/"
            }],
            "nominee_id": "5e980a38a87d7343deea00fa"
        }
    }]
```
### Nominee Schema 
```json
    [{
        "nominee": {
            "business_name": "3 Quarters Full Cafe",
            "business_url": "https://quarterscafe.ca",
            "business_description": "It may be called 3 Quarters Full, ...",
            "nominator_name": "Emily Yang",
            "nominator_email": "emily_yang@gmail.com",
            "nominator_facebook_url": "",
            "nominator_twitter_url": "",
            "nominator_instagram_url": "",
            "nominator_linkedin_url": "",
            "adopt_my_shop_listing_url": "",
            "business_address": "1789 Comox Street",
            "business_city": "Vancouver",
            "business_province": "British Columbia",
            "business_zip_code": "F5H 3S6",
            "business_country": "CA",
            "business_phone": "123123",
            "business_email" "contact@3quarters.ca"
            "business_tags": ["delivery", "pickup","taiwanese"],
            "products_offered":["Taiwanese food", "Japanese food"],
            "support_sales_options": [{
                "type": "gitfcard",
                "link": "https://www.instagram.com/3quartersfullcafe/"
            },{
                "type": "online_order",
                "link": "https://www.instagram.com/p/B97b-E9hBOg/"
            }],
            "mention": "This is a family owned restaurant founded in 2018 .... ",
            "not_mention": "",
            "reference_materials": [{
                "type": "News",
                "link": "https://www.cbc.com/new_restaurants_north_america.php/"
            },{
                "type": "Event",
                "link": "https://www.vaancouver_news.ca/canada_day_food_providers.php"
            }],
            "story_features_link": [{
                "type": "Instagram",
                "link": "https://www.instagram.com/p/A97b-F9hBST/"
            },{
                "type": "Facebook",
                "link": "https://www.facebook.com/DeliciousTaiwaneseFood/photos/rpp.1257196241038716/2634847449940248/?type=3&theater"
            }],
            "social_posts": [{
                "key_messaging": "Family preparing the meal",
                "additional_campaign_materials": "https://www.instagram.com/p/A97b-F9hBST/"
            },{
                "key_messaging": "The bast food of Taiwan",
                "additional_campaign_materials": "https://www.facebook.com/DeliciousTaiwaneseFood/photos/rpp.1257196241038716/2634847449940248/?type=3&theater"
            }],
            "featured_image": "",
            "images": [],
            "can_use_images": true,
            "support_language": ["Mandarin","Japanese","English"],
            "validation_history": " I tried to reach out Emily on Monday, 02 April 2020, but I had no answer from her. I will try again after 2 days."
        }
    }]
```

### Shops History 

It is a schema-less and and the information saved on it will be the last data saved on Shops before the update. 

---
# Data entry options: 
1. Nominate a shop:
- Shop:
    Name: Rambo SA
    Line of business: coffe shop (restaurant, gift shop, coffe shop)
    Preffered language: English (English, mandarin, spanish...)

- Contact info:
    Phone:  133
    Responsibible: John Rambo
    Email: jrambo@gmail.com

- Online presence (If applicable):
    Order link:
    Gift card link

2. Business owner form (Are you a business? on about)
- similar form to nominate
- Pre-approved application

### Checklist for business validation:
*Pending on ideas*
- Is the business a real business?
    (suggestion, we can use: Businness licence + full address to autenticate the business)
- Do they have a website? no
- Online ordering? link? yes, doordash https://doordash.com/johnsa
- Acceps gift card? link? no
