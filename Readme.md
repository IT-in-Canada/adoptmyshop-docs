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
- API: node, express, jwt, mongoose (maybe just mongod)
- Admin: react, sass, bootstrap - not necessarly need to be responsive

- Web Client: 
    1. Create a "widget like" structure, so that the existing UI can fetch data from our API and display on WP
        *e.g: city: api.adoptmyshop.org/cities*
    2. New UI: react, sass, bootstrap
            
## Pseudo DB schema:
```json
    [{
        "shop": {
            "name": "3 Quarters Full Cafe",
            "address": "1789 Comox Street",
            "city": "Vancouver",
            "country": "CA",
            "phone": "123123",
            "description": "It may be called 3 Quarters Full, ...",
            "tags": ["delivery", "pickup","taiwaneese"],
            "active": true,
            "featured_image": "",
            "images": [],
            "support_options": [{
                "type": "gitfcard",
                "link": "https://www.instagram.com/3quartersfullcafe/"
            },{
                "type": "online_order",
                "link": "https://www.instagram.com/p/B97b-E9hBOg/"
            }]
        }
    }]
```
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
- Do they have a website? no
- Online ordering? link? yes, doordash https://doordash.com/johnsa
- Acceps gift card? link? no