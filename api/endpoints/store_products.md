# store/products Endpoint

The store/products endpoint lists all available products in the store.

### Endpoint

**store/products**

**store/products/:type/:category**

### Method

_GET_

### URL Parameters

**Note**: Not setting these will retrieve the full list of items available

**type**: Same as the type member of the store item

**category**: Same as the category member of the store item

### Possible error messages

Insufficient permissions (not being logged in)
```json
{
    "data": [
        "You are not authorized to access this resource."
    ],
    "status": "notAuthorized",
}
```

### Data returned

```js
{
    'data': [{                              // Contains the requested data in an array of objects
        'cash': 0.0,                        // Only set if the item costs actual IRL money
        'base': true,                       // ?? (the first base products that are enabled for new accounts)
        'category': 'xxx',                  // This is shown in the store drop down i.e.: 'hiphop'
        'category_id': 0,                   // Internal ID for the category
        'currency': 7,                      // Internal ID for the type of currency
        'currency_name': 'plug_points',     // Readable name of the currency
        'expires': 'xxx',                   // Date when the item gets removed from the store
        'id': 'xxxyy',                      // The actual item ID
        'level': 1,                         // The level needed to purchase this item
        'name': 'xxx',                      // The name of the item (after purchase saved as avatarID e.g.: base01)
        'parent_id': 0,                     // Set for items that derive from another item (i.e.: hiphop01 => base01)
        'pp': 0,                            // Plug points needed to purchase this item
        'price': 0,                         // Either a copy of pp or cash
        'product_id': 0,                    // ID of the item
        'tier_name': 'xx_xx_xx_y',          // Different tier types for example 'cash_avatar_tier_2'
        'type': 'xxxx'                      // Type of the item (e.g.: 'avatars' or 'badges') 
    }],
    'meta': {},
    'status': 'ok',
    'time': 'xx.xxxxxxxxxxx'
}
```