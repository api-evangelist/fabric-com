# fabric (fabric-com)
fabric is an API-first composable commerce platform headquartered in Seattle, WA. The fabric v3 platform decomposes the traditional commerce monolith into a set of modular services — Identity, Customers, Product Catalog (PIM), Catalog Connector, Offers (Prices, Real-time Pricing Engine, Promotions), Inventory, Cart, Checkout, Cart Orchestrator (ShopperXP), Orders (OMS), Shipments, Invoices, Experiences (XM) — that retailers and brands compose into their own storefront and back-office stack. In 2026 fabric layered NEON, its agentic commerce control plane, on top of the platform via the Product Agent API. Reported customers include Crate & Barrel, Debenhams, PetMeds, and Over the Moon; fabric publicly reports 1B+ API calls served per month with sub-50ms latency.

**URL:** [Visit APIs.json](https://raw.githubusercontent.com/api-evangelist/fabric-com/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags

 - Commerce, Composable Commerce, Headless Commerce, E-commerce, Retail, Cart, Catalog, PIM, OMS, Inventory, Offers, Pricing, Promotions, Checkout, Identity, Experiences, Agentic Commerce

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## APIs

### fabric Identity API
OAuth2-based authentication served from per-tenant Okta-backed auth servers. Issues the bearer tokens every other fabric v3 service requires.

**Human URL:** [https://developer.fabric.inc/v3/api-reference/identity](https://developer.fabric.inc/v3/api-reference/identity)

- [OpenAPI](openapi/fabric-identity-openapi.yml)
- [Naftiko Capability — Authentication](capabilities/identity-authentication.yaml)

### fabric Customers API
Storefront customer (shopper) profiles, addresses, and self-service operations. System of record for shopper identity across Cart, Orders, and Experiences.

**Human URL:** [https://developer.fabric.inc/v3/api-reference/customers](https://developer.fabric.inc/v3/api-reference/customers)

- [OpenAPI](openapi/fabric-customers-openapi.yml)
- [Naftiko Capability — Profiles](capabilities/customers-customers.yaml)
- [Naftiko Capability — Addresses](capabilities/customers-addresses.yaml)

### fabric Product Catalog (PIM) API
Product information management — products, variants, categories, attribute schemas, bulk imports. Powers the merchandiser-facing Copilot UI and is the canonical catalog downstream services consume.

**Human URL:** [https://developer.fabric.inc/v3/api-reference/product-catalog](https://developer.fabric.inc/v3/api-reference/product-catalog)

- [OpenAPI](openapi/fabric-pim-openapi.yml)
- [GitHub Samples](https://github.com/FabricCommerce/fabric-pim-samples)
- [Naftiko Capability — Products](capabilities/pim-products.yaml)
- [Naftiko Capability — Categories](capabilities/pim-categories.yaml)
- [Naftiko Capability — Attributes](capabilities/pim-attributes.yaml)

### fabric Catalog Connector API
Lightweight ingestion service for customers retaining their own PIM. Async import/export jobs pull CSV/JSON template files into fabric's downstream commerce surface.

**Human URL:** [https://developer.fabric.inc/v3/api-reference/catalog-connector](https://developer.fabric.inc/v3/api-reference/catalog-connector)

- [OpenAPI](openapi/fabric-catalog-openapi.yml)
- [Naftiko Capability — Files](capabilities/catalog-connector-files.yaml)
- [Naftiko Capability — Jobs](capabilities/catalog-connector-jobs.yaml)

### fabric Offers — Prices API
System of record for base and sale prices per SKU per price list. Source-of-truth the Real-time Pricing Engine evaluates against.

**Human URL:** [https://developer.fabric.inc/v3/api-reference/offers](https://developer.fabric.inc/v3/api-reference/offers)

- [OpenAPI](openapi/fabric-offers-prices-openapi.yml)
- [Naftiko Capability — Prices](capabilities/offers-prices.yaml)

### fabric Offers — Real-time Pricing Engine API
Evaluates list prices, sale prices, and active promotions for a set of products, SKUs, or an entire cart in a single call. Returns effective price plus promotion attribution.

**Human URL:** [https://developer.fabric.inc/v3/api-reference/offers](https://developer.fabric.inc/v3/api-reference/offers)

- [OpenAPI](openapi/fabric-offers-pricing-openapi.yml)
- [Naftiko Capability — Pricing Engine](capabilities/offers-pricing-engine.yaml)

### fabric Offers — Promotions API
Create, search, toggle, and end promotions — item, cart, or shipping discounts, optionally gated by coupon code.

**Human URL:** [https://developer.fabric.inc/v3/api-reference/offers](https://developer.fabric.inc/v3/api-reference/offers)

- [OpenAPI](openapi/fabric-offers-promotions-openapi.yml)
- [Naftiko Capability — Promotions](capabilities/offers-promotions.yaml)

### fabric Inventory API
Stock counts across stores, warehouses, and dropship partners. Feeds Cart, OMS, and storefront PDPs with available-to-promise figures.

**Human URL:** [https://developer.fabric.inc/v3/api-reference/inventory](https://developer.fabric.inc/v3/api-reference/inventory)

- [OpenAPI](openapi/fabric-inventory-openapi.yml)
- [Naftiko Capability — Inventory](capabilities/inventory-inventory.yaml)

### fabric Cart API
Modular v3 cart — items, fulfillments, addresses, fees, taxes, coupons, payments — producing the order draft Checkout consumes. Guest and authenticated shopper carts.

**Human URL:** [https://developer.fabric.inc/v3/api-reference/cart](https://developer.fabric.inc/v3/api-reference/cart)

- [OpenAPI](openapi/fabric-cart-openapi.yml)
- [Naftiko Capability — Cart](capabilities/cart-cart.yaml)
- [Naftiko Capability — Items](capabilities/cart-items.yaml)
- [Naftiko Capability — Fulfillments](capabilities/cart-fulfillments.yaml)
- [Naftiko Capability — Payments](capabilities/cart-payments.yaml)

### fabric Checkout API
Completes the checkout flow and promotes the cart-produced order draft into an OMS order.

**Human URL:** [https://developer.fabric.inc/v3/api-reference/checkout](https://developer.fabric.inc/v3/api-reference/checkout)

- [OpenAPI](openapi/fabric-checkout-openapi.yml)
- [Naftiko Capability — Checkout](capabilities/checkout-checkout.yaml)

### fabric Cart Orchestrator (ShopperXP) API
Storefront-facing surface that wraps Cart, Offers, Inventory, and Identity. Each shopper action is a single orchestrator call that fans out internally in the correct order.

**Human URL:** [https://developer.fabric.inc/v3/api-reference/shopper-xp](https://developer.fabric.inc/v3/api-reference/shopper-xp)

- [OpenAPI](openapi/fabric-shopperxp-openapi.yml)
- [Naftiko Capability — Orchestrator](capabilities/shopperxp-orchestrator.yaml)

### fabric Orders (OMS) API
Order creation, lookup, status transitions, payment authorization, address and fee updates. The operational surface used by customer service, fulfillment, and finance.

**Human URL:** [https://developer.fabric.inc/v3/api-reference/orders](https://developer.fabric.inc/v3/api-reference/orders)

- [OpenAPI](openapi/fabric-orders-openapi.yml)
- [Naftiko Capability — Orders](capabilities/orders-orders.yaml)

### fabric Shipments API
Shipment lifecycle inside OMS — create, look up, update, and cancel shipments; associate carrier and tracking details.

**Human URL:** [https://developer.fabric.inc/v3/api-reference/orders](https://developer.fabric.inc/v3/api-reference/orders)

- [OpenAPI](openapi/fabric-shipments-openapi.yml)
- [Naftiko Capability — Shipments](capabilities/shipments-shipments.yaml)

### fabric Invoices API
Invoices generated from shipped or fulfilled orders. Integration point for ERP, tax, and finance systems consuming fabric order data.

**Human URL:** [https://developer.fabric.inc/v3/api-reference/orders](https://developer.fabric.inc/v3/api-reference/orders)

- [OpenAPI](openapi/fabric-invoices-openapi.yml)
- [Naftiko Capability — Invoices](capabilities/invoices-invoices.yaml)

### fabric Experiences (XM) API
Headless storefront content — pages, global components, menus — served from a CDN-backed read API. Authoring lives in the Copilot UI.

**Human URL:** [https://developer.fabric.inc/v3/api-reference/experiences](https://developer.fabric.inc/v3/api-reference/experiences)

- [OpenAPI](openapi/fabric-experiences-openapi.yml)
- [GitHub Samples](https://github.com/FabricCommerce/Fabric-React-Components)
- [Naftiko Capability — Pages](capabilities/experiences-pages.yaml)
- [Naftiko Capability — Components](capabilities/experiences-components.yaml)

### fabric Product Agent API
fabric NEON's Product Agent — the agentic commerce control plane that monitors product visibility across AI search surfaces, benchmarks against custom prompts, and enriches product data with intent signals for channel activation. fabric's headline 2026 capability.

**Human URL:** [https://developer.fabric.inc/product-agent/overview](https://developer.fabric.inc/product-agent/overview)

- [OpenAPI](openapi/fabric-product-agent-openapi.yml)
- [Naftiko Capability — Monitor](capabilities/product-agent-monitor.yaml)
- [Naftiko Capability — Activate](capabilities/product-agent-activate.yaml)

## Common

- [SignUp / Request Demo](https://fabric.inc/request-demo)
- [Developer Portal](https://developer.fabric.inc/home)
- [v3 API Reference](https://developer.fabric.inc/v3/api-reference)
- [Documentation Index (llms.txt)](https://developer.fabric.inc/llms.txt)
- [Identity / OAuth2](https://developer.fabric.inc/v3/api-reference/identity)
- [Release Notes](https://developer.fabric.inc/release-notes)
- [fabric Blog](https://fabric.inc/blog)
- [About fabric](https://fabric.inc/company/about)
- [Contact fabric](https://fabric.inc/contact-us)
- [FabricCommerce on GitHub](https://github.com/FabricCommerce)
- [Public Postman Collections](https://github.com/FabricCommerce/public-fabric-api-postman-collections)
- [LinkedIn](https://www.linkedin.com/company/fabricinc)
- [News](https://fabric.inc/news)

## Artifacts

- [Plans and Pricing (API Commons)](plans/fabric-com-plans-pricing.yml)
- [Rate Limits (API Commons)](rate-limits/fabric-com-rate-limits.yml)
- [FinOps Mapping (API Commons)](finops/fabric-com-finops.yml)
- [Spectral Ruleset](rules/fabric-com-rules.yml)
- [JSON-LD Context](json-ld/fabric-com-context.jsonld)
- [Vocabulary](vocabulary/fabric-com-vocabulary.yml)

### JSON Schemas
- [Product](json-schema/fabric-product-schema.json)
- [Cart](json-schema/fabric-cart-schema.json)
- [Order](json-schema/fabric-order-schema.json)
- [Promotion](json-schema/fabric-promotion-schema.json)

### JSON Structure
- [Product Structure](json-structure/fabric-product-structure.json)
- [Order Structure](json-structure/fabric-order-structure.json)

### Examples
- [Create Cart](examples/fabric-create-cart-example.json)
- [Evaluate Cart Pricing](examples/fabric-evaluate-cart-pricing-example.json)
- [Update Order Status](examples/fabric-update-order-status-example.json)
- [Toggle Promotion](examples/fabric-toggle-promotion-example.json)
