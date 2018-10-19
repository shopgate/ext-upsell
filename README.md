# Shopgate Connect - Upselling extension
[![Build Status](https://travis-ci.org/shopgate/ext-upselling.svg?branch=master)](https://travis-ci.org/shopgate/ext-upselling) [![Coverage Status](https://coveralls.io/repos/github/shopgate/ext-upselling/badge.svg?branch=master)](https://coveralls.io/github/shopgate/ext-upselling?branch=master)

Frontend extension which shows the upselling/related products slider on a Product Detail Page.


## Configuration

Currently it's possible to configure a slider which is rendered on the Product Detail Page and a product list which is shown as a Sheet/Drawer after user adds a product to a cart on Product Detail Page.

The configuration is done in the deployment process, as an extension config.

Product Detail Page configuration is a json with a following schema
```json
{
    "productPage": {
        "type": "Relation type. If empty no slider is rendered on Product Page. Possible: upselling, crossSelling, bonus, boughtWith, custom.",
        "position": "Portal position. If empty no slider is rendered on Product Page. Possible portal positions: product.description.after, product.header.after.",
        "headline": "Headline text rendered before the slider. If null or empty string, not headline is rendered.",
        "showPrice": "Boolean. If not true, no product price is shown",
        "showName": "Boolean. If not true, no product name is shown",
        "nameLines": "Number. Maximum lines item name should be possible. If empty defaults to 2",
    }
}
```

Product page add to cart sheet is a json with following schema:
```json
{
    "productPageAddToCart": {
        "type": "Relation type. If empty Sheet will never appear. Possible: upselling, crossSelling, bonus, boughtWith, custom.",
        "headline": "Headline text rendered as a Sheet title. If empty Sheet will never appear.",
        "showPrice": "Boolean. If not true, no product price is shown",
        "showName": "Boolean. If not true, no product name is shown",
        "nameLines": "Number. Maximum lines item name should be possible. If empty defaults to 2",
    }
}
```

## About Shopgate

Shopgate is the leading mobile commerce platform.

Shopgate offers everything online retailers need to be successful in mobile. Our leading
software-as-a-service (SaaS) enables online stores to easily create, maintain and optimize native
apps and mobile websites for the iPhone, iPad, Android smartphones and tablets.

## License

Shopgate Cloud - Extension Boilerplate is available under the Apache License, Version 2.0.

See the [LICENSE](./LICENSE.md) file for more information.

