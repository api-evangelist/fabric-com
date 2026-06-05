# fabric (fabric-com)

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/fabric-com/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/fabric-com/refs/heads/main/apis.yml)

## Scope

- **Access:** 3rd-Party

## Tags

- Commerce
- Composable Commerce
- Headless Commerce
- E-commerce
- Retail
- Cart
- Catalog
- PIM
- OMS
- Inventory
- Offers
- Pricing
- Promotions
- Checkout
- Identity
- Experiences
- Agentic Commerce

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## APIs

### fabric Identity API

fabric's Identity API issues OAuth2 access tokens used by every other fabric service. Implements the standard authorization-code and client-credentials flows on a per-tenant Okta-backed auth server, returning bearer tokens scoped to the calling account. Used to authenticate both first-party storefronts and third-party integrations against the v3 commerce APIs.

- **Human URL:** [https://developer.fabric.inc/v3/api-reference/identity](https://developer.fabric.inc/v3/api-reference/identity)
- **Base URL:** `https://{customer_name}.login.fabric.inc`

#### Tags

- Authentication
- Authorization
- Identity
- OAuth2

#### Properties

- [Documentation](https://developer.fabric.inc/v3/api-reference/identity)
- [OpenAPI](openapi/fabric-identity-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/fabric-identity.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fabric-identity.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### fabric Customers API

Create and manage storefront customers (shoppers), their profiles, addresses, and self-service operations. The Customers API is the system of record for shopper identity inside fabric and feeds Cart, Orders, and Experiences with the customer object referenced across the platform.

- **Human URL:** [https://developer.fabric.inc/v3/api-reference/customers](https://developer.fabric.inc/v3/api-reference/customers)
- **Base URL:** `https://api.fabric.inc/v3`

#### Tags

- Customers
- Profiles
- Addresses
- Shoppers

#### Properties

- [Documentation](https://developer.fabric.inc/v3/api-reference/customers)
- [OpenAPI](openapi/fabric-customers-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/fabric-customers.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fabric-customers.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### fabric Product Catalog (PIM) API

fabric's Product Information Management (PIM) service for modeling products, variants, categories, attribute schemas, and bulk imports. Powers the merchandiser-facing Copilot UI and exposes the canonical product catalog that downstream services (Catalog Connector, Cart, Offers, Experiences) consume.

- **Human URL:** [https://developer.fabric.inc/v3/api-reference/product-catalog](https://developer.fabric.inc/v3/api-reference/product-catalog)
- **Base URL:** `https://live.copilot.fabric.inc`

#### Tags

- Catalog
- Products
- PIM
- Attributes
- Categories

#### Properties

- [Documentation](https://developer.fabric.inc/v3/api-reference/product-catalog)
- [OpenAPI](openapi/fabric-pim-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/fabric-pim.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fabric-pim.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Git Hub](https://github.com/FabricCommerce/fabric-pim-samples)

### fabric Catalog Connector API

Catalog Connector (formerly PIM Connector) is a lightweight ingestion service for customers who already own their PIM. It accepts CSV/JSON template files, runs async import/export jobs, and pushes the resulting products and SKUs into fabric's downstream commerce surface without forcing migration off the existing system of record.

- **Human URL:** [https://developer.fabric.inc/v3/api-reference/catalog-connector](https://developer.fabric.inc/v3/api-reference/catalog-connector)
- **Base URL:** `https://api.fabric.inc/v3`

#### Tags

- Catalog
- Connector
- Import
- Export

#### Properties

- [Documentation](https://developer.fabric.inc/v3/api-reference/catalog-connector)
- [OpenAPI](openapi/fabric-catalog-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/fabric-catalog.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fabric-catalog.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### fabric Offers - Prices API

Create, update, and look up base and sale prices for SKUs across price lists. The Prices API is the system of record for fabric's pricing data and is the source the Real-time Pricing Engine evaluates against at cart time.

- **Human URL:** [https://developer.fabric.inc/v3/api-reference/offers](https://developer.fabric.inc/v3/api-reference/offers)
- **Base URL:** `https://api.fabric.inc/v3`

#### Tags

- Pricing
- Offers
- SKU

#### Properties

- [Documentation](https://developer.fabric.inc/v3/api-reference/offers)
- [OpenAPI](openapi/fabric-offers-prices-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/fabric-offers-prices.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fabric-offers-prices.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### fabric Offers - Real-time Pricing Engine API

The Real-time Pricing Engine (RTPE) evaluates list prices, sale prices, and active promotions for a set of products, SKUs, or an entire cart in a single call. Returns the calculated effective price and the promotion attribution chain used to surface live prices on storefronts.

- **Human URL:** [https://developer.fabric.inc/v3/api-reference/offers](https://developer.fabric.inc/v3/api-reference/offers)
- **Base URL:** `https://api.fabric.inc/v3`

#### Tags

- Pricing
- Engine
- Offers
- Cart

#### Properties

- [Documentation](https://developer.fabric.inc/v3/api-reference/offers)
- [OpenAPI](openapi/fabric-offers-pricing-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/fabric-offers-pricing.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fabric-offers-pricing.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### fabric Offers - Promotions API

Create, search, toggle, and end promotions — discounts on items, carts, or shipping methods. The Promotions API is the authoring surface; the Pricing Engine applies the active promotions returned by these endpoints to live cart and pricing calculations.

- **Human URL:** [https://developer.fabric.inc/v3/api-reference/offers](https://developer.fabric.inc/v3/api-reference/offers)
- **Base URL:** `https://api.fabric.inc/v3`

#### Tags

- Promotions
- Discounts
- Coupons
- Offers

#### Properties

- [Documentation](https://developer.fabric.inc/v3/api-reference/offers)
- [OpenAPI](openapi/fabric-offers-promotions-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/fabric-offers-promotions.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fabric-offers-promotions.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### fabric Inventory API

Manage stock counts, locations, and inventory networks across stores, warehouses, and dropship partners. Inventory feeds the cart, OMS, and storefront product detail pages with the available-to-promise figures that drive fulfillment decisions.

- **Human URL:** [https://developer.fabric.inc/v3/api-reference/inventory](https://developer.fabric.inc/v3/api-reference/inventory)
- **Base URL:** `https://api.fabric.inc/v3`

#### Tags

- Inventory
- Stock
- Locations
- Networks

#### Properties

- [Documentation](https://developer.fabric.inc/v3/api-reference/inventory)
- [OpenAPI](openapi/fabric-inventory-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/fabric-inventory.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fabric-inventory.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### fabric Cart API

The v3 Cart API is fabric's modular cart service for adding, updating, and removing items; managing fulfillments, addresses, fees, taxes, coupons, and payments; and producing the order draft that Checkout consumes. Supports both guest and authenticated shopper carts.

- **Human URL:** [https://developer.fabric.inc/v3/api-reference/cart](https://developer.fabric.inc/v3/api-reference/cart)
- **Base URL:** `https://api.fabric.inc/v3`

#### Tags

- Cart
- Checkout
- Commerce
- Storefront

#### Properties

- [Documentation](https://developer.fabric.inc/v3/api-reference/cart)
- [OpenAPI](openapi/fabric-cart-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/fabric-cart.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fabric-cart.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### fabric Checkout API

Completes the checkout process and places an order for the items in a cart. Takes the cart-produced order draft, validates payments, and hands the resulting order off to OMS for fulfillment.

- **Human URL:** [https://developer.fabric.inc/v3/api-reference/checkout](https://developer.fabric.inc/v3/api-reference/checkout)
- **Base URL:** `https://api.fabric.inc/v3`

#### Tags

- Checkout
- Cart
- Order Drafts
- Commerce

#### Properties

- [Documentation](https://developer.fabric.inc/v3/api-reference/checkout)
- [OpenAPI](openapi/fabric-checkout-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/fabric-checkout.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fabric-checkout.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### fabric Cart Orchestrator (ShopperXP) API

The Cart Orchestrator (ShopperXP) wraps Cart, Offers, Inventory, and Identity into a single storefront-facing surface. Storefront clients call one orchestrator endpoint per shopper action and the service fans out to the underlying commerce APIs in the correct sequence.

- **Human URL:** [https://developer.fabric.inc/v3/api-reference/shopper-xp](https://developer.fabric.inc/v3/api-reference/shopper-xp)
- **Base URL:** `https://api.fabric.inc/v3`

#### Tags

- Cart
- Orchestrator
- ShopperXP
- Storefront

#### Properties

- [Documentation](https://developer.fabric.inc/v3/api-reference/shopper-xp)
- [OpenAPI](openapi/fabric-shopperxp-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/fabric-shopperxp.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fabric-shopperxp.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### fabric Orders (OMS) API

fabric's Order Management System (OMS) — order creation, lookup, status transitions, payment authorization, address and fee updates, and the operational surface used by customer service, fulfillment teams, and downstream finance systems.

- **Human URL:** [https://developer.fabric.inc/v3/api-reference/orders](https://developer.fabric.inc/v3/api-reference/orders)
- **Base URL:** `https://api.fabric.inc/v3`

#### Tags

- Orders
- OMS
- Fulfillment
- Returns

#### Properties

- [Documentation](https://developer.fabric.inc/v3/api-reference/orders)
- [OpenAPI](openapi/fabric-orders-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/fabric-orders.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fabric-orders.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### fabric Shipments API

Manage the shipment lifecycle inside OMS — create, look up, update, and cancel shipments; associate carrier and tracking information; and notify downstream systems as packages move from the warehouse to the customer.

- **Human URL:** [https://developer.fabric.inc/v3/api-reference/orders](https://developer.fabric.inc/v3/api-reference/orders)
- **Base URL:** `https://api.fabric.inc/v3`

#### Tags

- Shipments
- Fulfillment
- OMS
- Tracking

#### Properties

- [Documentation](https://developer.fabric.inc/v3/api-reference/orders)
- [OpenAPI](openapi/fabric-shipments-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/fabric-shipments.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fabric-shipments.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### fabric Invoices API

Issue and manage invoices generated from shipped or fulfilled orders. The Invoices API captures the financial event tied to an order's fulfillment and is the integration point for ERP, tax, and finance systems consuming fabric order data.

- **Human URL:** [https://developer.fabric.inc/v3/api-reference/orders](https://developer.fabric.inc/v3/api-reference/orders)
- **Base URL:** `https://api.fabric.inc/v3`

#### Tags

- Invoices
- Billing
- OMS
- Finance

#### Properties

- [Documentation](https://developer.fabric.inc/v3/api-reference/orders)
- [OpenAPI](openapi/fabric-invoices-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/fabric-invoices.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fabric-invoices.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### fabric Experiences (XM) API

fabric Experiences (formerly XM) is the headless storefront content service — pages, global components, and menus served from a CDN-backed read API. Powers the merchandiser-authored, shopper-facing surfaces of fabric storefronts.

- **Human URL:** [https://developer.fabric.inc/v3/api-reference/experiences](https://developer.fabric.inc/v3/api-reference/experiences)
- **Base URL:** `https://cdn.xm.fabric.inc/api`

#### Tags

- Experiences
- XM
- Content
- Storefront
- Pages

#### Properties

- [Documentation](https://developer.fabric.inc/v3/api-reference/experiences)
- [OpenAPI](openapi/fabric-experiences-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/fabric-experiences.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fabric-experiences.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Git Hub](https://github.com/FabricCommerce/Fabric-React-Components)

### fabric Product Agent API

fabric NEON's Product Agent — the agentic commerce control plane that monitors product visibility across AI search surfaces, benchmarks against custom prompts, and enriches product data with intent signals for downstream channel activation. fabric's headline 2026 capability.

- **Human URL:** [https://developer.fabric.inc/product-agent/overview](https://developer.fabric.inc/product-agent/overview)
- **Base URL:** `https://commerceos.aiagents.fabric.inc/api`

#### Tags

- AI
- Agentic Commerce
- NEON
- Product Agent
- Agents

#### Properties

- [Documentation](https://developer.fabric.inc/product-agent/overview)
- [OpenAPI](openapi/fabric-product-agent-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/fabric-product-agent.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fabric-product-agent.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Sign Up](https://fabric.inc/request-demo)
- [Portal](https://developer.fabric.inc/home)
- [Documentation](https://developer.fabric.inc/v3/api-reference)
- [Documentation](https://developer.fabric.inc/llms.txt)
- [Authentication](https://developer.fabric.inc/v3/api-reference/identity)
- [Changelog](https://developer.fabric.inc/release-notes)
- [Blog](https://fabric.inc/blog)
- [About](https://fabric.inc/company/about)
- [Contact Us](https://fabric.inc/contact-us)
- [Git Hub](https://github.com/FabricCommerce)
- [Postman](https://github.com/FabricCommerce/public-fabric-api-postman-collections) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [LinkedIn](https://www.linkedin.com/company/fabricinc)
- [Twitter](https://twitter.com/fabriccommerce)
- [Press Room](https://fabric.inc/news)
- [Plans](plans/fabric-com-plans-pricing.yml)
- [Rate Limits](rate-limits/fabric-com-rate-limits.yml)
- [Fin Ops](finops/fabric-com-finops.yml)
- [Vocabulary](vocabulary/fabric-com-vocabulary.yml)
- [JSON-LD](json-ld/fabric-com-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Spectral Rules](rules/fabric-com-rules.yml)

## Maintainers

**FN:** Kin Lane
**Email:** info@apievangelist.com
**URL:** https://apievangelist.com
