---
title: Marketplace Shopping List feature overview
description: This document contains concept information for the Marketplace Shopping List feature.
template: concept-topic-template
---

A shopping list is a list of the items that shoppers buy or plan to buy frequently or regularly.

The *Marketplace Shopping List* feature lets customers add product offers and marketplace products to a shopping list in the Marketplace Storefront.

Merchant information is displayed in the *Sold by* field so that customer can always know which merchant is the owner of the product. Price and stock of the shopping list items are based on the price and stock of the respective product offers and marketplace products.

## Marketplace Shopping List on the Storefront

If the product offer or marketplace product is not available, the following behavior is observed on the Storefront:

<div class="width-100">

| CASE DESCRIPTION   | BEHAVIOR    |
| ------------------ | --------------------------- |
| **Product** stock is 0 and never out of stock flag is FALSE. | The shopping list item is marked as *not available*, there is no possibility to add it to cart, however the price and merchant information is displayed. |
| **Offer** stock is 0 and *never out of stock* flag is FALSE.   | The shopping list item is marked as *not available*, it is impossible to add it to cart, however the price and merchant information is displayed. |
| Merchant status is *Inactive*. The  **product** was added to the shopping list. | The shopping list item is marked as *not available*, it is impossible to add it to cart, the *Sold by* hint is not displayed, however the customer can still see the price. If the merchant is active again, the shopping list item gets the *Sold by* hint back with the actual merchant information. |
| Merchant status is *Inactive*. The **offer** was added to the shopping list. | The shopping list item is marked as *not available*, it is impossible to add it to cart, the *Sold by* hint is not displayed, however the customer can still see the price. If the merchant is active again, the shopping list item gets the *Sold by* hint back with the actual merchant information. |
| The **Offer** is **not** approved.                           | The shopping list item is marked as *not available*, it is impossible to add it to cart, the *Sold by* hint is not displayed, however the customer can still see the price. |
| The **Product** status is *Deactivated*.                     | The shopping list item is marked as *not available*, it is impossible to add it to cart, the *Sold by* hint and the price are not displayed, |
| The **Offer** status is *Inactive*.                          | The shopping list item is marked as *not available*, it is impossible to add it to cart, the *Sold by* hint is not displayed, the price (taken from the concrete product) is displayed. |
| **Product** is not in the current store.                     | The shopping list item is marked as *not available*, it is impossible to add it to cart, the *Sold by* hint is not displayed, however the customer can still see the price. |
| **Offer** is not in the current store.                       | The *Sold by* hint is not displayed. The shopping list item is switched to the normal product without stock, so the shopping list item is marked as *not available*, it is impossible to add it to cart, the price is displayed. |
| **Product** validity date does not include the current date. | The shopping list item is marked as *not available*, it is impossible to add it to cart, the *Sold by* hint and price are not displayed. |
| **Offer** validity date does not include the current date.   | The *Sold by* hint is not displayed. The shopping list item is switched to the normal product without stock, so the shopping list item is marked as *not available*, it is impossible to add it to cart, the price is displayed. |
| **Product** is discontinued.                                 | The shopping list item is marked as *discontinued*, the *Sold by* hint is shown in the Storefront. If an alternative [marketplace product](/docs/marketplace/user/features/{{page.version}}/marketplace-product-feature-overview.html) exists, it is displayed with the  *Sold by* hint. Product offers are not supported, so if the alternative product has an offer, it is displayed as a marketplace product or a merchant product. |

</div>

### Shopping list page

When adding a merchant product or an offer to the shopping list, a customer can see the merchant information in the *Sold by* hint:

![gif](https://spryker.s3.eu-central-1.amazonaws.com/docs/Marketplace/user+guides/Features/Marketplace+Shopping+List/add-marketplace-product-and-offer-to-shopping-list.gif)

### Share shopping list

Regardless of whether the shopping list is shared with full or read access, the merchant information is displayed to a user in the same way it is displayed to the shopping list owner.

![gif](https://spryker.s3.eu-central-1.amazonaws.com/docs/Marketplace/user+guides/Features/Marketplace+Shopping+List/share-shopping-list.gif)


## Constraints

The *Print Shopping List* functionality does not contain any merchant-related information.

{% info_block warningBox "Developer guides" %}

Are you a developer? See Marketplace Shopping Lists feature walkthrough <!---LINK--> for developers.

{% endinfo_block %}