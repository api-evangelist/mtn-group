# MTN Group (mtn-group)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

MTN Group is Africa's largest mobile network operator, headquartered in Johannesburg, South Africa, serving roughly 290 million subscribers across around 16 markets in Africa. Beyond mobile voice, data and enterprise connectivity it runs MoMo, one of the continent's largest mobile-money platforms. Unusually for a carrier, MTN publishes a genuinely open developer surface: the MTN Developer Platform (MADAPI) at developers.mtn.com lists 221 API products across 15 African markets and lets anyone download the OpenAPI/Swagger definition for a product without an account, and momodeveloper.mtn.com is a self-serve Azure API Management portal with a sandbox for the MoMo Collection, Disbursements and Remittance APIs. Its catalogue is heavily TM Forum Open API shaped (TMF620, TMF621, TMF622, TMF629, TMF632, TMF633, TMF635, TMF637, TMF639, TMF652, TMF654, TMF658, TMF666, TMF667, TMF676, TMF677, TMF678, TMF681, TMF683, TMF685, TMF688, TMF720). MTN South Africa is a GSMA Open Gateway participant — it announced Number Verification and SIM Swap with Cell C and Telkom in February 2024 — but nothing in its published catalogue is CAMARA-shaped: its SIM Swap and Device Swap APIs are MTN-proprietary designs secured with OAuth2 client-credentials rather than the CAMARA OIDC/CIBA profile, and no CAMARA API is callable from either portal. MTN is not an Aduna shareholder. Sandbox access is self-serve; production access is vetted and commercially negotiated.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/mtn-group/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/mtn-group/refs/heads/main/apis.yml)

## Tags

- Telecommunications
- South Africa
- Africa
- Mobile Network Operator
- Network APIs
- Open Gateway
- TM Forum
- BSS
- Mobile Money
- Messaging
- SMS
- USSD
- IoT
- SIM Swap
- Identity Verification
- Payments

## Timestamps

- **Created:** 2026-07-25
- **Modified:** 2026-07-25

## Reviewer Notes

- **Developer portal:** [https://developers.mtn.com/](https://developers.mtn.com/) — HTTP 200, a real self-serve portal. The full 221-product catalogue across 15 African markets is browsable without an account, and every product with a definition exposes it at `/products/{slug}/download/swagger` anonymously.
- **Second portal:** [https://momodeveloper.mtn.com/](https://momodeveloper.mtn.com/) — HTTP 200, the MTN MoMo Open API portal on Azure API Management, with self-serve sign-up and a documented sandbox.
- **Specs harvested:** 115 of 221 products returned a real OpenAPI 3.x or Swagger 2.0 document (404 documented paths in total), saved verbatim under `openapi/`. The other 106 products are listed but return HTTP 500 on the download endpoint.
- **CAMARA posture:** GSMA Open Gateway participant with proprietary equivalents, not CAMARA specs. MTN South Africa announced Number Verification and SIM Swap with Cell C and Telkom on 22 February 2024, but the string `camara` appears zero times across all 116 downloaded documents, no Number Verification product exists in the catalogue, and MTN's SIM Swap and Device Swap APIs are MTN-proprietary shapes on `api.mtn.com` secured with OAuth2 client-credentials rather than the CAMARA OIDC/CIBA profile. A press release is not an implementation.
- **Aduna:** MTN is not a shareholder in the Ericsson-led Aduna joint venture, and no aggregator channel for MTN network APIs was found. MTN reaches developers directly — with a BSS/customer/mobile-money catalogue, not network APIs.
- **TM Forum:** deep and visible. A dedicated TMF category holds 21 products referencing TMF620, TMF621, TMF622, TMF629, TMF632, TMF633, TMF635, TMF637, TMF639, TMF640, TMF652, TMF654, TMF658, TMF666, TMF667, TMF676, TMF677, TMF678, TMF681, TMF683, TMF685, TMF688 and TMF720. No MTN-held TM Forum Open API Conformance badge was found; MTN participated as the operator in certifications held by its BSS vendor Tecnotree.
- **Auth:** OAuth2 client-credentials (77 specs) and a legacy `X-API-Key` header (72 specs); the FAQ confirms MTN is migrating from API key to OAuth. MoMo uses an Azure APIM subscription key plus a Wallet Platform OAuth2 token. **CIBA is present** — the MoMo APIs expose `POST /v1_0/bc-authorize` with `login_hint`, `scope` and `auth_req_id` — but only in mobile money, not in the network-API catalogue where CAMARA would require it. No OIDC discovery document is served on either portal (404).
- **3GPP:** no NEF/SCEF surface, no network slicing, no edge/MEC, no Quality on Demand.
- **SDKs:** none first-party. [github.com/MTN-Group](https://github.com/MTN-Group) is real but holds four incidental repos and no SDK.
- **Webhooks:** callback-style (`X-Callback-Url`, consent callbacks, a TMF688 hub/listener product). No AsyncAPI published.

## APIs (119)

### MTN Account Decisioning

API to consume and process account management actions to perform account status changes to customers with a MoMo Advance account. ChangeLog: 03-March-23 - First version.

- **Human URL:** [https://developers.mtn.com/products/account-decisioning](https://developers.mtn.com/products/account-decisioning)
- **Base URL:** `https://api.mtn.com/accountDecisioning/v1`

#### Tags

- Customer
- Uganda
- South Africa

#### Properties

- [Documentation](https://developers.mtn.com/products/account-decisioning)
- [API Reference](https://developers.mtn.com/products/account-decisioning)
- [OpenAPI](openapi/mtn-group-account-decisioning.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN TMF Customer Bill Management - TMF678

TMF API Reference: TMF 678 - Customer bill Management Release: 19.5 - December 2019 The Customer Bill Management API allows to find and retrieve one or several customer bills (also called invoices) produced for a customer. A customer bill is an electronic or paper document produced at the end of the billing process. The customer...

- **Human URL:** [https://developers.mtn.com/products/tmf-customer-bill-management](https://developers.mtn.com/products/tmf-customer-bill-management)

#### Tags

- TM Forum
- TMF678
- Benin
- South Sudan
- Eswatini

#### Properties

- [Documentation](https://developers.mtn.com/products/tmf-customer-bill-management)
- [API Reference](https://developers.mtn.com/products/tmf-customer-bill-management)
- [OpenAPI](openapi/mtn-group-tmf-customer-bill-management.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN Loans

Api Documentation.

- **Human URL:** [https://developers.mtn.com/products/mtn-customer-loans-api-v1](https://developers.mtn.com/products/mtn-customer-loans-api-v1)
- **Base URL:** `https://loan-channelvas-system-mtnapitest.e4ff.pro-eu-west-1.openshiftapps.com/`

#### Tags

- Customer
- Nigeria

#### Properties

- [Documentation](https://developers.mtn.com/products/mtn-customer-loans-api-v1)
- [API Reference](https://developers.mtn.com/products/mtn-customer-loans-api-v1)
- [OpenAPI](openapi/mtn-group-mtn-customer-loans-api-v1.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN Subscriber Details

Api Documentation.

- **Human URL:** [https://developers.mtn.com/products/subscriber-details](https://developers.mtn.com/products/subscriber-details)
- **Base URL:** `https://za.api.mtn.com/subscriberdetails`

#### Tags

- Customer
- South Africa

#### Properties

- [Documentation](https://developers.mtn.com/products/subscriber-details)
- [API Reference](https://developers.mtn.com/products/subscriber-details)
- [OpenAPI](openapi/mtn-group-subscriber-details.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN Subscriber Type

Api Documentation.

- **Human URL:** [https://developers.mtn.com/products/subscriber-type](https://developers.mtn.com/products/subscriber-type)
- **Base URL:** `https://za.api.mtn.com/customermanagement`

#### Tags

- Customer
- South Africa

#### Properties

- [Documentation](https://developers.mtn.com/products/subscriber-type)
- [API Reference](https://developers.mtn.com/products/subscriber-type)
- [OpenAPI](openapi/mtn-group-subscriber-type.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN Provisioning

Api Documentation.

- **Human URL:** [https://developers.mtn.com/products/provisioning](https://developers.mtn.com/products/provisioning)
- **Base URL:** `https://za.api.mtn.com/VasServices`

#### Tags

- Customer
- South Africa

#### Properties

- [Documentation](https://developers.mtn.com/products/provisioning)
- [API Reference](https://developers.mtn.com/products/provisioning)
- [OpenAPI](openapi/mtn-group-provisioning.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN Unified Balance V1

Api Documentation.

- **Human URL:** [https://developers.mtn.com/products/unified-balance-v1](https://developers.mtn.com/products/unified-balance-v1)
- **Base URL:** `https://za.api.mtn.com/v1`

#### Tags

- Customer
- South Africa

#### Properties

- [Documentation](https://developers.mtn.com/products/unified-balance-v1)
- [API Reference](https://developers.mtn.com/products/unified-balance-v1)
- [OpenAPI](openapi/mtn-group-unified-balance-v1.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN TMF Resource Inventory Management - TMF639

TMF API Reference: TMF639 - Resource Inventory Release : 19.5 - December 2019 Resource Inventory API goal is to provide the ability to manage Resources. Operations Resource Inventory API performs the following operations on the resources : - Retrieve an entity or a collection of entities depending on filter criteria - Partial...

- **Human URL:** [https://developers.mtn.com/products/tmf-resourceinventorymanagement-tmf639](https://developers.mtn.com/products/tmf-resourceinventorymanagement-tmf639)

#### Tags

- TM Forum
- TMF639
- Benin
- Côte d'Ivoire
- South Sudan
- Eswatini

#### Properties

- [Documentation](https://developers.mtn.com/products/tmf-resourceinventorymanagement-tmf639)
- [API Reference](https://developers.mtn.com/products/tmf-resourceinventorymanagement-tmf639)
- [OpenAPI](openapi/mtn-group-tmf-resourceinventorymanagement-tmf639.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN Sales Lead

TMF API Reference : TMF 699 - Sales This API provides interfaces for Sales Lead, Sales Opportunity, Sales Quote and the other management capabilities to support the sales activities to build relationship with the prospect customer who could be a person or organization that has an interest in the goods and/or services and possibly...

- **Human URL:** [https://developers.mtn.com/products/sales-management](https://developers.mtn.com/products/sales-management)
- **Base URL:** `https://za.api.mtn.com/sales/v1/`

#### Tags

- Customer
- South Africa

#### Properties

- [Documentation](https://developers.mtn.com/products/sales-management)
- [API Reference](https://developers.mtn.com/products/sales-management)
- [OpenAPI](openapi/mtn-group-sales-management.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN Service Activation and Configuration

TMF API Reference: TMF640 - Service Activation and Configuration Version 4.0 Service Activation and Configuration API goal is to provide the ability to activate and configure Service. This API features Monitor pattern allowing to manage service configuration/activation asynchronous request (server side will provide monitor as...

- **Human URL:** [https://developers.mtn.com/products/service-activation-and-configuration](https://developers.mtn.com/products/service-activation-and-configuration)
- **Base URL:** `http://api.mtn.com/v1`

#### Tags

- Customer
- Nigeria
- Uganda
- South Africa
- Zambia

#### Properties

- [Documentation](https://developers.mtn.com/products/service-activation-and-configuration)
- [API Reference](https://developers.mtn.com/products/service-activation-and-configuration)
- [OpenAPI](openapi/mtn-group-service-activation-and-configuration.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN Service Ordering

TMF API Reference : TMF 641 - Service Ordering Management Version 4.1 TMF641 performs the following operations on service order resource : - Retrieval of a service order or a collection of service orders by id - Creation of a service order - Deletion of service order Copyright © TM Forum 2020. All Rights Reserved.

- **Human URL:** [https://developers.mtn.com/products/service-ordering](https://developers.mtn.com/products/service-ordering)

#### Tags

- Customer
- South Africa

#### Properties

- [Documentation](https://developers.mtn.com/products/service-ordering)
- [API Reference](https://developers.mtn.com/products/service-ordering)
- [OpenAPI](openapi/mtn-group-service-ordering.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN BSS TT OAuth V1

Authentication API.

- **Human URL:** [https://developers.mtn.com/products/bss-tt-oauth-v1](https://developers.mtn.com/products/bss-tt-oauth-v1)
- **Base URL:** `https://api.mtn.com/v1/bss-oauth`

#### Tags

- TM Forum
- Eswatini
- Zambia

#### Properties

- [Documentation](https://developers.mtn.com/products/bss-tt-oauth-v1)
- [API Reference](https://developers.mtn.com/products/bss-tt-oauth-v1)
- [OpenAPI](openapi/mtn-group-bss-tt-oauth-v1.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN Balance Management V1

The Balance Management API facilitates the management of Customer Account capabilitites. It provides a generic API any client or back-end can call to request a Topup function that allows a reseller to refill/credit a subscriber airtime account from the reseller’s account.

- **Human URL:** [https://developers.mtn.com/products/balance-management-v1](https://developers.mtn.com/products/balance-management-v1)
- **Base URL:** `https://api.mtn.com/v1`

#### Tags

- Customer
- Côte d'Ivoire
- Liberia
- Zambia
- Nigeria

#### Properties

- [Documentation](https://developers.mtn.com/products/balance-management-v1)
- [API Reference](https://developers.mtn.com/products/balance-management-v1)
- [OpenAPI](openapi/mtn-group-balance-management-v1.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN Callmeback V1

callmeback API will be used to post a request in AYO, when initiated by Users via different Applications like "portal", "IVR" etc.

- **Human URL:** [https://developers.mtn.com/products/callmeback-v1](https://developers.mtn.com/products/callmeback-v1)
- **Base URL:** `https://za.api.mtn.com`

#### Tags

- Customer
- South Africa

#### Properties

- [Documentation](https://developers.mtn.com/products/callmeback-v1)
- [API Reference](https://developers.mtn.com/products/callmeback-v1)
- [OpenAPI](openapi/mtn-group-callmeback-v1.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN Callmeback V2

callmeback API will be used to post a request to Backend systems when initiated by Users via different Applications like "portal", "IVR" etc.

- **Human URL:** [https://developers.mtn.com/products/callmeback-v2](https://developers.mtn.com/products/callmeback-v2)
- **Base URL:** `https://za.api.mtn.com/v2`

#### Tags

- Customer
- South Africa

#### Properties

- [Documentation](https://developers.mtn.com/products/callmeback-v2)
- [API Reference](https://developers.mtn.com/products/callmeback-v2)
- [OpenAPI](openapi/mtn-group-callmeback-v2.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN RCS Communication

This API Provides a capability to create and send communications, notifications, and instructions to Parties, Individuals, Organizations or Users.

- **Human URL:** [https://developers.mtn.com/products/rcs-communication](https://developers.mtn.com/products/rcs-communication)
- **Base URL:** `https://api.mtn.com/v1`

#### Tags

- Customer
- Nigeria

#### Properties

- [Documentation](https://developers.mtn.com/products/rcs-communication)
- [API Reference](https://developers.mtn.com/products/rcs-communication)
- [OpenAPI](openapi/mtn-group-rcs-communication.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN Communication Management V1

This is Swagger UI environment generated for the TMF Communication Management specification.

- **Human URL:** [https://developers.mtn.com/products/communication-management-v1](https://developers.mtn.com/products/communication-management-v1)
- **Base URL:** `https://api.mtn.com/v1`

#### Tags

- Customer
- South Africa

#### Properties

- [Documentation](https://developers.mtn.com/products/communication-management-v1)
- [API Reference](https://developers.mtn.com/products/communication-management-v1)
- [OpenAPI](openapi/mtn-group-communication-management-v1.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN TMF681 Communication Management

This is Swagger UI environment generated for the TMF Communication Management specification.

- **Human URL:** [https://developers.mtn.com/products/tmf681-communication-management](https://developers.mtn.com/products/tmf681-communication-management)

#### Tags

- Customer
- TMF681
- TM Forum
- South Africa

#### Properties

- [Documentation](https://developers.mtn.com/products/tmf681-communication-management)
- [API Reference](https://developers.mtn.com/products/tmf681-communication-management)
- [OpenAPI](openapi/mtn-group-tmf681-communication-management.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN Consent Validation V1

A suite of apis for customer consent validation.

- **Human URL:** [https://developers.mtn.com/products/ayo-preapproval](https://developers.mtn.com/products/ayo-preapproval)
- **Base URL:** `https://api.mtn.com/v1`

#### Tags

- Customer
- Benin
- Congo
- Côte d'Ivoire
- Cameroon

#### Properties

- [Documentation](https://developers.mtn.com/products/ayo-preapproval)
- [API Reference](https://developers.mtn.com/products/ayo-preapproval)
- [OpenAPI](openapi/mtn-group-ayo-preapproval.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN Content Push

The API provides a target system with data content to be pushed via a channel to a customer. Supported Actions 1. SendSms. **Supported OpCo's:** MTN Uganda, MTN Ghana, MTN SA.

- **Human URL:** [https://developers.mtn.com/products/content-push](https://developers.mtn.com/products/content-push)
- **Base URL:** `https://api.mtn.com/v1`

#### Tags

- Customer
- Ghana
- Côte d'Ivoire
- South Africa

#### Properties

- [Documentation](https://developers.mtn.com/products/content-push)
- [API Reference](https://developers.mtn.com/products/content-push)
- [OpenAPI](openapi/mtn-group-content-push.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN Customer Bill Management

To facilitate the capability for consumers to retrieve bill information at service level , account level or invoice level etc.

- **Human URL:** [https://developers.mtn.com/products/mtn-customer-bill-management](https://developers.mtn.com/products/mtn-customer-bill-management)
- **Base URL:** `https://api.mtn.com/v1`

#### Tags

- Customer
- Ghana
- Nigeria
- Rwanda
- Eswatini

#### Properties

- [Documentation](https://developers.mtn.com/products/mtn-customer-bill-management)
- [API Reference](https://developers.mtn.com/products/mtn-customer-bill-management)
- [OpenAPI](openapi/mtn-group-mtn-customer-bill-management.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN Customer Billing Token V1

To register services and activate services content tokens.

- **Human URL:** [https://developers.mtn.com/products/customer-billing-token-v1](https://developers.mtn.com/products/customer-billing-token-v1)
- **Base URL:** `https://api.mtn.com/v1/customer`

#### Tags

- Customer
- South Africa

#### Properties

- [Documentation](https://developers.mtn.com/products/customer-billing-token-v1)
- [API Reference](https://developers.mtn.com/products/customer-billing-token-v1)
- [OpenAPI](openapi/mtn-group-customer-billing-token-v1.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN Data Gifting

The Data Gifting API facilitates purchase of data product for Beneficiary subscriber(Customer) and charging shall be done from Charging system using Requesting subscriber(Sponsor) msisdn and SMS will be sent to both subscriber’s.

- **Human URL:** [https://developers.mtn.com/products/mtn-nigeria-data-gifting-v1](https://developers.mtn.com/products/mtn-nigeria-data-gifting-v1)
- **Base URL:** `https://api.mtn.com/v1/datagifting`

#### Tags

- Customer
- Nigeria

#### Properties

- [Documentation](https://developers.mtn.com/products/mtn-nigeria-data-gifting-v1)
- [API Reference](https://developers.mtn.com/products/mtn-nigeria-data-gifting-v1)
- [OpenAPI](openapi/mtn-group-mtn-nigeria-data-gifting-v1.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN Customer Datashare

The Data Share API facilitates data share between Data Share Agent(Data Sender) and Customer(Data Receiver) also provides a data analytics. It also provides functionality to manage provider and consumer msisdns that are linked as part of the Internet Share Bundles Product **26-August-21: ChangeID: 0000000327** - Added a new GET endpoint...

- **Human URL:** [https://developers.mtn.com/products/mtn-nigeria-customer-datashare](https://developers.mtn.com/products/mtn-nigeria-customer-datashare)
- **Base URL:** `https://api.mtn.com/v1/datashare`

#### Tags

- Customer
- Congo
- Nigeria
- Cameroon

#### Properties

- [Documentation](https://developers.mtn.com/products/mtn-nigeria-customer-datashare)
- [API Reference](https://developers.mtn.com/products/mtn-nigeria-customer-datashare)
- [OpenAPI](openapi/mtn-group-mtn-nigeria-customer-datashare.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN Customer Delivery Booking

To retrieve and schedule delivery information for MTN Customers.

- **Human URL:** [https://developers.mtn.com/products/customer-delivery-booking](https://developers.mtn.com/products/customer-delivery-booking)
- **Base URL:** `https://api.mtn.com/v1`

#### Tags

- Customer
- South Africa

#### Properties

- [Documentation](https://developers.mtn.com/products/customer-delivery-booking)
- [API Reference](https://developers.mtn.com/products/customer-delivery-booking)
- [OpenAPI](openapi/mtn-group-customer-delivery-booking.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN Customer Identification V1

The Customer Identification API provides information about a customer and their historical usage events on voice, data, SMS, Roaming etc. Information can be retrieved by stating the date range for the period the API consumer is interested in. It will return date and time on which a specific event occurred on a customer's MSISDN as...

- **Human URL:** [https://developers.mtn.com/products/customer-identification-v1](https://developers.mtn.com/products/customer-identification-v1)
- **Base URL:** `https://api.mtn.com/v1/customerIdentification/`

#### Tags

- Customer
- Congo

#### Properties

- [Documentation](https://developers.mtn.com/products/customer-identification-v1)
- [API Reference](https://developers.mtn.com/products/customer-identification-v1)
- [OpenAPI](openapi/mtn-group-customer-identification-v1.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN KYC Consent

The Customer KYC Consent API facilitates the consent from the customer while capturing and retrieval of Customer Information. This aggregator service provides comprehensive Know Your Customer (KYC) consent management capabilities, enabling secure customer data capture, consent validation, and information retrieval operations across...

- **Human URL:** [https://developers.mtn.com/products/kyc-consent](https://developers.mtn.com/products/kyc-consent)
- **Base URL:** `https://api.mtn.com/v1`

#### Tags

- Customer
- Congo
- Cameroon
- Eswatini
- Zambia

#### Properties

- [Documentation](https://developers.mtn.com/products/kyc-consent)
- [API Reference](https://developers.mtn.com/products/kyc-consent)
- [OpenAPI](openapi/mtn-group-kyc-consent.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN Customer Loyalty Management

An API to manage customer loyalty operations. Can also be used by 3rd-party partners (3PP) to get a customer's loyalty products and rewards **04-Oct-21 ChangeID: 0000000000235** -Branched off from the original TMF document.

- **Human URL:** [https://developers.mtn.com/products/customer-loyalty-management](https://developers.mtn.com/products/customer-loyalty-management)
- **Base URL:** `http://api.mtn.com/v1/loyaltyManagement`

#### Tags

- Customer
- Ghana
- Nigeria
- Uganda
- South Africa

#### Properties

- [Documentation](https://developers.mtn.com/products/customer-loyalty-management)
- [API Reference](https://developers.mtn.com/products/customer-loyalty-management)
- [OpenAPI](openapi/mtn-group-customer-loyalty-management.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN Customer Management - COE

An API to Create customers,create admin users,activate/deactivate,disable Sims.

- **Human URL:** [https://developers.mtn.com/products/customer-management-coe-za-preprod](https://developers.mtn.com/products/customer-management-coe-za-preprod)
- **Base URL:** `https://coe.api.mtn.com/customerManagement/v1`

#### Tags

- Customer
- South Africa

#### Properties

- [Documentation](https://developers.mtn.com/products/customer-management-coe-za-preprod)
- [API Reference](https://developers.mtn.com/products/customer-management-coe-za-preprod)
- [OpenAPI](openapi/mtn-group-customer-management-coe-za-preprod.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN Customer Pin Management v2

To facilitate the capability for customer to create/validate/change Pin Information.

- **Human URL:** [https://developers.mtn.com/products/customer-pin-management-v2](https://developers.mtn.com/products/customer-pin-management-v2)
- **Base URL:** `https://api.mtn.com/customerPinManagement/v2`

#### Tags

- Customer
- Cameroon
- Liberia
- Nigeria

#### Properties

- [Documentation](https://developers.mtn.com/products/customer-pin-management-v2)
- [API Reference](https://developers.mtn.com/products/customer-pin-management-v2)
- [OpenAPI](openapi/mtn-group-customer-pin-management-v2.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN Customer Promotion

API Documentation.

- **Human URL:** [https://developers.mtn.com/products/customer-promotion](https://developers.mtn.com/products/customer-promotion)
- **Base URL:** `https://za.api.mtn.com/customerPromotion/v1`

#### Tags

- Customer
- Ghana
- Nigeria
- South Africa

#### Properties

- [Documentation](https://developers.mtn.com/products/customer-promotion)
- [API Reference](https://developers.mtn.com/products/customer-promotion)
- [OpenAPI](openapi/mtn-group-customer-promotion.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN Customer Survey

The API facilitates product survey with a MTN Customer.

- **Human URL:** [https://developers.mtn.com/products/customer-survey](https://developers.mtn.com/products/customer-survey)
- **Base URL:** `https://api.mtn.com/v1/survey`

#### Tags

- Customer
- Nigeria
- Eswatini
- South Africa

#### Properties

- [Documentation](https://developers.mtn.com/products/customer-survey)
- [API Reference](https://developers.mtn.com/products/customer-survey)
- [OpenAPI](openapi/mtn-group-customer-survey.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN Customer Data Transfer(ng prod)

API will enable MTN customers to transfer part of their active airtime or data to another MTN customer. This service excludes special data plans.

- **Human URL:** [https://developers.mtn.com/products/customer-data-transfer-ng-prod](https://developers.mtn.com/products/customer-data-transfer-ng-prod)
- **Base URL:** `https://api.mtn.com/v1`

#### Tags

- Customer
- Nigeria

#### Properties

- [Documentation](https://developers.mtn.com/products/customer-data-transfer-ng-prod)
- [API Reference](https://developers.mtn.com/products/customer-data-transfer-ng-prod)
- [OpenAPI](openapi/mtn-group-customer-data-transfer-ng-prod.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN Customer Data Transfer

API will enable MTN customers to transfer part of their active airtime or data to another MTN customer. This service excludes special data plans.

- **Human URL:** [https://developers.mtn.com/products/mtn-customer-datatransfer](https://developers.mtn.com/products/mtn-customer-datatransfer)
- **Base URL:** `https://api.mtn.com/v1`

#### Tags

- Customer
- Congo
- Côte d'Ivoire
- Cameroon
- Ghana

#### Properties

- [Documentation](https://developers.mtn.com/products/mtn-customer-datatransfer)
- [API Reference](https://developers.mtn.com/products/mtn-customer-datatransfer)
- [OpenAPI](openapi/mtn-group-mtn-customer-datatransfer.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN Device Swap V1

The Device Swap API is designed to detect changes in the International Mobile Equipment Identity (IMEI) associated with a mobile subscriber's number (MSISDN) within a specific period, typically the last 30 days. Supported Operations 1.Checks if the IMEI linked to an MSISDN has changed. 2.Returns the date of the latest IMEI change....

- **Human URL:** [https://developers.mtn.com/products/device-swap-v1](https://developers.mtn.com/products/device-swap-v1)
- **Base URL:** `https://api.mtn.com/v1/devices`

#### Tags

- Customer
- Cameroon
- Nigeria
- South Africa
- Zambia

#### Properties

- [Documentation](https://developers.mtn.com/products/device-swap-v1)
- [API Reference](https://developers.mtn.com/products/device-swap-v1)
- [OpenAPI](openapi/mtn-group-device-swap-v1.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN TMF 720 - Digital Identity Management

TMF API Reference: TMF720 - Digital Identity Management Digital Identity Management API goal is to provide the ability to manage a digital identity. This digital identity allows to identify an individual, a resource, or a partyRole (a specific role - or set of roles - for a given individual). A digital identity is associated with...

- **Human URL:** [https://developers.mtn.com/products/tmf-720-digital-identity-management](https://developers.mtn.com/products/tmf-720-digital-identity-management)

#### Tags

- TM Forum
- TMF720
- Cameroon
- South Africa

#### Properties

- [Documentation](https://developers.mtn.com/products/tmf-720-digital-identity-management)
- [API Reference](https://developers.mtn.com/products/tmf-720-digital-identity-management)
- [OpenAPI](openapi/mtn-group-tmf-720-digital-identity-management.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN Digital Partner Management

TM Forum Open APIs (Apache 2.0) Party Management API Provides standardized mechanism for digital partner management such as creation, update, retrieval, deletion and notification of events. Partner is an organization that has any kind of relation with the enterprise.

- **Human URL:** [https://developers.mtn.com/products/digital-partner-management](https://developers.mtn.com/products/digital-partner-management)
- **Base URL:** `https://api.mtn.com/digitalPartners/v1`

#### Tags

- Customer
- South Africa

#### Properties

- [Documentation](https://developers.mtn.com/products/digital-partner-management)
- [API Reference](https://developers.mtn.com/products/digital-partner-management)
- [OpenAPI](openapi/mtn-group-digital-partner-management.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN Document Management

TMF667 Document API describes the meta-data of a Document, such as the name, creationDate and lifecycle status. The (typically binary) body of this document (such as a Word.doc, PDF, Video clip, or Image) will be held in the associated Attachment(s) either by Ref or Value. If by value - the binary content is held in the...

- **Human URL:** [https://developers.mtn.com/products/document-managment](https://developers.mtn.com/products/document-managment)
- **Base URL:** `https://mtn.com/tmf-api/document/v4/`

#### Tags

- Customer
- Uganda
- Nigeria
- South Africa

#### Properties

- [Documentation](https://developers.mtn.com/products/document-managment)
- [API Reference](https://developers.mtn.com/products/document-managment)
- [OpenAPI](openapi/mtn-group-document-managment.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN TMF Document Management - TMF667

This is Swagger UI environment generated for the TMF Document Management specification.

- **Human URL:** [https://developers.mtn.com/products/tmf-document-management-tmf667](https://developers.mtn.com/products/tmf-document-management-tmf667)
- **Base URL:** `https://mtn.com/tmf-api/documentManagement`

#### Tags

- TM Forum
- TMF667
- Côte d'Ivoire
- South Sudan
- Eswatini
- Zambia

#### Properties

- [Documentation](https://developers.mtn.com/products/tmf-document-management-tmf667)
- [API Reference](https://developers.mtn.com/products/tmf-document-management-tmf667)
- [OpenAPI](openapi/mtn-group-tmf-document-management-tmf667.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN TMF688 - Event Management

The Event Management API provides a standardized client interface to the enterprise event management system.

- **Human URL:** [https://developers.mtn.com/products/tmf688-event-management](https://developers.mtn.com/products/tmf688-event-management)

#### Tags

- TM Forum
- TMF688
- South Africa

#### Properties

- [Documentation](https://developers.mtn.com/products/tmf688-event-management)
- [API Reference](https://developers.mtn.com/products/tmf688-event-management)
- [OpenAPI](openapi/mtn-group-tmf688-event-management.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN EEC Token Management

This API provides EEC Token Management.

- **Human URL:** [https://developers.mtn.com/products/eec-token-management](https://developers.mtn.com/products/eec-token-management)
- **Base URL:** `https://api.mtn.com/v1/eec/`

#### Tags

- Customer
- Eswatini

#### Properties

- [Documentation](https://developers.mtn.com/products/eec-token-management)
- [API Reference](https://developers.mtn.com/products/eec-token-management)
- [OpenAPI](openapi/mtn-group-eec-token-management.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN Insurance

List of services to integrate with insurance service provider to manage insurance policies and policy related information. It provides the ability for channel applications to request for quote, submit application, manage application and fetch list of policies.

- **Human URL:** [https://developers.mtn.com/products/insurance](https://developers.mtn.com/products/insurance)
- **Base URL:** `https://za.api.mtn.com/insurance`

#### Tags

- Customer
- South Africa

#### Properties

- [Documentation](https://developers.mtn.com/products/insurance)
- [API Reference](https://developers.mtn.com/products/insurance)
- [OpenAPI](openapi/mtn-group-insurance.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN IoT Device Management

This service provides comprehensive IoT device management capabilities for TMF908 operations including device information retrieval, device management operations, and lifecycle management. The service integrates with various IoT platforms and provides standardized APIs for device operations across the MTN ecosystem.

- **Human URL:** [https://developers.mtn.com/products/iot-device-management](https://developers.mtn.com/products/iot-device-management)
- **Base URL:** `https://api.mtn.com/v1`

#### Tags

- Customer
- Congo
- Ghana
- Nigeria
- Eswatini

#### Properties

- [Documentation](https://developers.mtn.com/products/iot-device-management)
- [API Reference](https://developers.mtn.com/products/iot-device-management)
- [OpenAPI](openapi/mtn-group-iot-device-management.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN HCM V1

Api Documentation.

- **Human URL:** [https://developers.mtn.com/products/hcm-v1](https://developers.mtn.com/products/hcm-v1)
- **Base URL:** `https://za.api.mtn.com/v1`

#### Tags

- Customer
- South Africa

#### Properties

- [Documentation](https://developers.mtn.com/products/hcm-v1)
- [API Reference](https://developers.mtn.com/products/hcm-v1)
- [OpenAPI](openapi/mtn-group-hcm-v1.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN LogBack V1

Facility to query failed transactions.

- **Human URL:** [https://developers.mtn.com/products/logback-v1](https://developers.mtn.com/products/logback-v1)
- **Base URL:** `https://api.mtn.com/v1`

#### Tags

- Analytics
- South Africa
- Nigeria
- Ghana
- Côte d'Ivoire

#### Properties

- [Documentation](https://developers.mtn.com/products/logback-v1)
- [API Reference](https://developers.mtn.com/products/logback-v1)
- [OpenAPI](openapi/mtn-group-logback-v1.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN TMF Loyalty Management - TMF658

The TMForum Loyalty API Specification as developed by Globetom.

- **Human URL:** [https://developers.mtn.com/products/tmf-loyalty-management-tmf658](https://developers.mtn.com/products/tmf-loyalty-management-tmf658)
- **Base URL:** `http://api.mtn.com/tmf-api/loyaltyManagement/v1`

#### Tags

- TM Forum
- TMF658
- Benin
- Côte d'Ivoire
- South Sudan
- Eswatini

#### Properties

- [Documentation](https://developers.mtn.com/products/tmf-loyalty-management-tmf658)
- [API Reference](https://developers.mtn.com/products/tmf-loyalty-management-tmf658)
- [OpenAPI](openapi/mtn-group-tmf-loyalty-management-tmf658.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN RCS Capability

This API provides ability to check the capability of an MSISDN to receive RCS mesages.

- **Human URL:** [https://developers.mtn.com/products/rcs-capability](https://developers.mtn.com/products/rcs-capability)
- **Base URL:** `https://api.mtn.com/v1`

#### Tags

- Customer
- Nigeria

#### Properties

- [Documentation](https://developers.mtn.com/products/rcs-capability)
- [API Reference](https://developers.mtn.com/products/rcs-capability)
- [OpenAPI](openapi/mtn-group-rcs-capability.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN Medallia SMS V2

Provides a RESTful API to expose SMS capability.

- **Human URL:** [https://developers.mtn.com/products/medallia-sms-v2](https://developers.mtn.com/products/medallia-sms-v2)
- **Base URL:** `https://api.mtn.com/v2m/`

#### Tags

- Messaging
- Congo
- Côte d'Ivoire
- Cameroon
- Guinea

#### Properties

- [Documentation](https://developers.mtn.com/products/medallia-sms-v2)
- [API Reference](https://developers.mtn.com/products/medallia-sms-v2)
- [OpenAPI](openapi/mtn-group-medallia-sms-v2.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN Advertising V2

This service provides comprehensive mobile advertisement management capabilities for MTN operations including ad targeting, content delivery, campaign management, and performance analytics. The service integrates with various advertising platforms to provide personalized ad experiences across the MTN ecosystem.

- **Human URL:** [https://developers.mtn.com/products/advertising-v2](https://developers.mtn.com/products/advertising-v2)
- **Base URL:** `https://api.mtn.com/v1`

#### Tags

- Advertising
- Eswatini

#### Properties

- [Documentation](https://developers.mtn.com/products/advertising-v2)
- [API Reference](https://developers.mtn.com/products/advertising-v2)
- [OpenAPI](openapi/mtn-group-advertising-v2.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN Advertising

A brief description of the API. It can be multiple lines.

- **Human URL:** [https://developers.mtn.com/products/mtn-advertising-api-v1](https://developers.mtn.com/products/mtn-advertising-api-v1)
- **Base URL:** `https://api.mtn.com`

#### Tags

- Advertising
- South Africa
- Nigeria
- Ghana
- Uganda

#### Properties

- [Documentation](https://developers.mtn.com/products/mtn-advertising-api-v1)
- [API Reference](https://developers.mtn.com/products/mtn-advertising-api-v1)
- [OpenAPI](openapi/mtn-group-mtn-advertising-api-v1.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN Mobile Customer Information

The mobile info API provides network related data. Supported Operations 1. Get last SIM Swap date of an MSISDN. 2. Get last SIM Swap date indicator of a MSISDN **Supported OpCo's:** MTN Uganda, MTN Ghana, MTN SA.

- **Human URL:** [https://developers.mtn.com/products/mobile-customer-information](https://developers.mtn.com/products/mobile-customer-information)
- **Base URL:** `https://api.mtn.com/v1/mobile`

#### Tags

- Customer
- Ghana
- Uganda
- South Africa

#### Properties

- [Documentation](https://developers.mtn.com/products/mobile-customer-information)
- [API Reference](https://developers.mtn.com/products/mobile-customer-information)
- [OpenAPI](openapi/mtn-group-mobile-customer-information.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN MoMo Withdrawals V1

To facilitate the capability for consumers to realize withdrawals via MADAPI. The callback (i.. Completed) will be handled via MADAPI's callback API.

- **Human URL:** [https://developers.mtn.com/products/withdrawals-v1](https://developers.mtn.com/products/withdrawals-v1)
- **Base URL:** `https://preprod.mtn.com/v1`

#### Tags

- Payments
- Benin
- Congo
- Cameroon
- Ghana

#### Properties

- [Documentation](https://developers.mtn.com/products/withdrawals-v1)
- [API Reference](https://developers.mtn.com/products/withdrawals-v1)
- [OpenAPI](openapi/mtn-group-withdrawals-v1.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN MoMo Verification V1-ToBeDeleted

A suite of apis for customer validation.

- **Human URL:** [https://developers.mtn.com/products/momo-verification](https://developers.mtn.com/products/momo-verification)
- **Base URL:** `https://api.mtn.com/v1`

#### Tags

- Payments
- Cameroon
- South Africa

#### Properties

- [Documentation](https://developers.mtn.com/products/momo-verification)
- [API Reference](https://developers.mtn.com/products/momo-verification)
- [OpenAPI](openapi/mtn-group-momo-verification.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN AccountHolders V1

The Accountholders API returns basic information of the Accountholder including MTN Mobile Money account status. i.e. ACTIVE, SUSPENDED, BLOCKED etc. It also support validation of a MoMo accountholder, as well as the verification of financial resourceinformation.

- **Human URL:** [https://developers.mtn.com/products/ayoaccountholderinfo](https://developers.mtn.com/products/ayoaccountholderinfo)
- **Base URL:** `https://api.mtn.com/v1`

#### Tags

- Customer
- Benin
- Congo
- Côte d'Ivoire
- Cameroon

#### Properties

- [Documentation](https://developers.mtn.com/products/ayoaccountholderinfo)
- [API Reference](https://developers.mtn.com/products/ayoaccountholderinfo)
- [OpenAPI](openapi/mtn-group-ayoaccountholderinfo.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN Agent Profile

An API to retrieve the profile of an MTN field agent. Please refer to the reference guides https://developers.mtn.com/getting-started and Response and Error Codes documents https://developers.mtn.com/getting-started/response-and-error-codes.

- **Human URL:** [https://developers.mtn.com/products/agent-profile](https://developers.mtn.com/products/agent-profile)
- **Base URL:** `https://api.mtn.com/v1/agents`

#### Tags

- Agent
- Ghana
- Uganda
- Eswatini
- Nigeria

#### Properties

- [Documentation](https://developers.mtn.com/products/agent-profile)
- [API Reference](https://developers.mtn.com/products/agent-profile)
- [OpenAPI](openapi/mtn-group-agent-profile.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN Customer Account Management V1

This API manages tasks for an MTN customer.

- **Human URL:** [https://developers.mtn.com/products/customer-account-management-v1](https://developers.mtn.com/products/customer-account-management-v1)
- **Base URL:** `https://api.mtn.com/v1`

#### Tags

- Customer
- South Africa

#### Properties

- [Documentation](https://developers.mtn.com/products/customer-account-management-v1)
- [API Reference](https://developers.mtn.com/products/customer-account-management-v1)
- [OpenAPI](openapi/mtn-group-customer-account-management-v1.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN KYC v1

MTN Customer KYC API allows clients to view the KYC (Know Your Customer) details of an MTN customer. The KYC API is a subset of the Customer Profile API.

- **Human URL:** [https://developers.mtn.com/products/mtn-customer-kyc-api-v1-product](https://developers.mtn.com/products/mtn-customer-kyc-api-v1-product)
- **Base URL:** `https://api.mtn.com/v1/customers`

#### Tags

- Customer
- Côte d'Ivoire
- Congo
- Cameroon
- Ghana

#### Properties

- [Documentation](https://developers.mtn.com/products/mtn-customer-kyc-api-v1-product)
- [API Reference](https://developers.mtn.com/products/mtn-customer-kyc-api-v1-product)
- [OpenAPI](openapi/mtn-group-mtn-customer-kyc-api-v1-product.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN Customer KYC Verification

The Customer KYC(Know Your Client) Verification API will validate the 3PP Customer KYC information with MTN Customer KYC information.

- **Human URL:** [https://developers.mtn.com/products/customer-kyc-verification](https://developers.mtn.com/products/customer-kyc-verification)
- **Base URL:** `https://api.mtn.com/v1/kycVerification/`

#### Tags

- Customer
- Benin
- Côte d'Ivoire
- Cameroon
- Ghana

#### Properties

- [Documentation](https://developers.mtn.com/products/customer-kyc-verification)
- [API Reference](https://developers.mtn.com/products/customer-kyc-verification)
- [OpenAPI](openapi/mtn-group-customer-kyc-verification.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN Loans v2

This API facilitate loan in advance for an MTN customer.

- **Human URL:** [https://developers.mtn.com/products/loans-v2](https://developers.mtn.com/products/loans-v2)
- **Base URL:** `https://api.mtn.com/v2`

#### Tags

- Customer
- Benin
- Congo
- Côte d'Ivoire
- Cameroon

#### Properties

- [Documentation](https://developers.mtn.com/products/loans-v2)
- [API Reference](https://developers.mtn.com/products/loans-v2)
- [OpenAPI](openapi/mtn-group-loans-v2.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN Locations

An API to retrieve the Location details of an MTN customer. Please refer to the Response and Error Codes documents https://developers.mtn.com/insights/response-codes.

- **Human URL:** [https://developers.mtn.com/products/mtn-customer-locations-api-v1](https://developers.mtn.com/products/mtn-customer-locations-api-v1)
- **Base URL:** `https://api.mtn.com/v1`

#### Tags

- Customer
- South Africa
- Nigeria
- Ghana
- Côte d'Ivoire

#### Properties

- [Documentation](https://developers.mtn.com/products/mtn-customer-locations-api-v1)
- [API Reference](https://developers.mtn.com/products/mtn-customer-locations-api-v1)
- [OpenAPI](openapi/mtn-group-mtn-customer-locations-api-v1.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN Customer Management

An API to register MoMo on Tier 0 for BSS. Please refer to the reference guides https://developers.mtn.com/API-Reference-Guides and Response and Error Codes documents https://developers.mtn.com/ResponseCodes.

- **Human URL:** [https://developers.mtn.com/products/customer-management](https://developers.mtn.com/products/customer-management)
- **Base URL:** `https://api.mtn.com/v1/customerManagement`

#### Tags

- Customer
- Uganda
- Ghana

#### Properties

- [Documentation](https://developers.mtn.com/products/customer-management)
- [API Reference](https://developers.mtn.com/products/customer-management)
- [OpenAPI](openapi/mtn-group-customer-management.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN Plans v2

An API to retrieve the Plan details of an MTN customer and calculate aYo premiums. Can also be used by 3rd-party partners (3PP) for airtime recharge of a prepaid subscriber **24-June-21: ChangeID: c835ca3** - Added an optional channel parameter on the /customers/{customerId}/plans/refill endpoint **09-August-21: ChangeID: 87f0b10** -...

- **Human URL:** [https://developers.mtn.com/products/mtn-customer-plans-api-v2](https://developers.mtn.com/products/mtn-customer-plans-api-v2)
- **Base URL:** `https://api.mtn.com/v2`

#### Tags

- Customer
- Benin
- Cameroon
- Congo
- Côte d'Ivoire

#### Properties

- [Documentation](https://developers.mtn.com/products/mtn-customer-plans-api-v2)
- [API Reference](https://developers.mtn.com/products/mtn-customer-plans-api-v2)
- [OpenAPI](openapi/mtn-group-mtn-customer-plans-api-v2.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN Profiles V2

An API to retrieve the profile of an MTN customer. Please refer to the reference guides https://developers.mtn.com/API-Reference-Guides and Response and Error Codes documents https://developers.mtn.com/ResponseCodes.

- **Human URL:** [https://developers.mtn.com/products/mtn-customer-profiles-api-v2-product](https://developers.mtn.com/products/mtn-customer-profiles-api-v2-product)
- **Base URL:** `https://api.mtn.com/v2`

#### Tags

- Customer
- Benin
- Congo
- Côte d'Ivoire
- Cameroon

#### Properties

- [Documentation](https://developers.mtn.com/products/mtn-customer-profiles-api-v2-product)
- [API Reference](https://developers.mtn.com/products/mtn-customer-profiles-api-v2-product)
- [OpenAPI](openapi/mtn-group-mtn-customer-profiles-api-v2-product.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN Risk Management

This API assesses risks for an MTN customer as well as creates applications.

- **Human URL:** [https://developers.mtn.com/products/risk-management](https://developers.mtn.com/products/risk-management)
- **Base URL:** `https://za.api.mtn.com/v1/riskManagement`

#### Tags

- Customer
- South Africa

#### Properties

- [Documentation](https://developers.mtn.com/products/risk-management)
- [API Reference](https://developers.mtn.com/products/risk-management)
- [OpenAPI](openapi/mtn-group-risk-management.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN Customer Score V1

This API is used to determine the customer's score through an activities performed within a period of time.

- **Human URL:** [https://developers.mtn.com/products/mtn-customer-score](https://developers.mtn.com/products/mtn-customer-score)
- **Base URL:** `https://api.mtn.com/v1`

#### Tags

- Customer
- Cameroon
- Nigeria

#### Properties

- [Documentation](https://developers.mtn.com/products/mtn-customer-score)
- [API Reference](https://developers.mtn.com/products/mtn-customer-score)
- [OpenAPI](openapi/mtn-group-mtn-customer-score.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN SIM Verification

This API is used to verify/validate SIM Swap status, SIM Activation status and SIM Recycle status of a customer's msisdn. - **'/simSwap/verifyStatus'** capability is used to verify sim swap status as true or false. - **'/simActivation/verifyStatus'** capability is used to verify sim activation status as true or false. -...

- **Human URL:** [https://developers.mtn.com/products/simverification](https://developers.mtn.com/products/simverification)
- **Base URL:** `https://api.mtn.com/v1/simVerification`

#### Tags

- Customer
- Nigeria

#### Properties

- [Documentation](https://developers.mtn.com/products/simverification)
- [API Reference](https://developers.mtn.com/products/simverification)
- [OpenAPI](openapi/mtn-group-simverification.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN Subscriptions v2

MTN Customer Subscription Management API — an MTN Group API product published on the MTN Developer Platform (MADAPI) with a downloadable machine-readable definition covering 6 path(s).

- **Human URL:** [https://developers.mtn.com/products/mtn-subscription-api-v2](https://developers.mtn.com/products/mtn-subscription-api-v2)
- **Base URL:** `https://api.mtn.com/v2`

#### Tags

- Customer
- Benin
- Cameroon
- Congo
- Côte d'Ivoire

#### Properties

- [Documentation](https://developers.mtn.com/products/mtn-subscription-api-v2)
- [API Reference](https://developers.mtn.com/products/mtn-subscription-api-v2)
- [OpenAPI](openapi/mtn-group-mtn-subscription-api-v2.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN G2M

API to provide capability to manage Offering specification of products.

- **Human URL:** [https://developers.mtn.com/products/g2m](https://developers.mtn.com/products/g2m)
- **Base URL:** `https://api.mtn.com/v1/g2m`

#### Tags

- Customer
- South Africa

#### Properties

- [Documentation](https://developers.mtn.com/products/g2m)
- [API Reference](https://developers.mtn.com/products/g2m)
- [OpenAPI](openapi/mtn-group-g2m.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN OAuth V1

Generates an access token based on username and password.

- **Human URL:** [https://developers.mtn.com/products/oauth-v1](https://developers.mtn.com/products/oauth-v1)
- **Base URL:** `https://api.mtn.com/v1/oauth`

#### Tags

- Identity
- Benin
- Congo
- Côte d'Ivoire
- Cameroon

#### Properties

- [Documentation](https://developers.mtn.com/products/oauth-v1)
- [API Reference](https://developers.mtn.com/products/oauth-v1)
- [OpenAPI](openapi/mtn-group-oauth-v1.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN Merchant Provisioning V1

To enable merchants to manage purchases of subscribers.

- **Human URL:** [https://developers.mtn.com/products/merchant-provisioning-v1](https://developers.mtn.com/products/merchant-provisioning-v1)
- **Base URL:** `https://api.mtn.com/v1/merchant`

#### Tags

- Customer
- South Africa

#### Properties

- [Documentation](https://developers.mtn.com/products/merchant-provisioning-v1)
- [API Reference](https://developers.mtn.com/products/merchant-provisioning-v1)
- [OpenAPI](openapi/mtn-group-merchant-provisioning-v1.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN SMS

MTN SMS Messaging API allowing developers to include SMS messaging in their applications.

- **Human URL:** [https://developers.mtn.com/products/mtn-sms-api-v1](https://developers.mtn.com/products/mtn-sms-api-v1)
- **Base URL:** `https://api.mtn.com/v1/messages/`

#### Tags

- Messaging
- Nigeria

#### Properties

- [Documentation](https://developers.mtn.com/products/mtn-sms-api-v1)
- [API Reference](https://developers.mtn.com/products/mtn-sms-api-v1)
- [OpenAPI](openapi/mtn-group-mtn-sms-api-v1.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN USSD interface

Provides a RESTful API to expose USSD capability.

- **Human URL:** [https://developers.mtn.com/products/ussd](https://developers.mtn.com/products/ussd)
- **Base URL:** `https://api.mtn.com/v1/`

#### Tags

- Messaging
- Benin
- Congo
- Côte d'Ivoire
- Cameroon

#### Properties

- [Documentation](https://developers.mtn.com/products/ussd)
- [API Reference](https://developers.mtn.com/products/ussd)
- [OpenAPI](openapi/mtn-group-ussd.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN Product Offering v2

A MTN API that controls the display of the catalog of Products available for a customer to purchase.

- **Human URL:** [https://developers.mtn.com/products/mtn-product-offering-api-v2](https://developers.mtn.com/products/mtn-product-offering-api-v2)
- **Base URL:** `https://www.api.mtn.com`

#### Tags

- Customer
- Rwanda

#### Properties

- [Documentation](https://developers.mtn.com/products/mtn-product-offering-api-v2)
- [API Reference](https://developers.mtn.com/products/mtn-product-offering-api-v2)
- [OpenAPI](openapi/mtn-group-mtn-product-offering-api-v2.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN Product Offering v3

A MTN API that controls the display of the catalog of Products available for a customer to purchase.

- **Human URL:** [https://developers.mtn.com/products/mtn-product-offering-api-v3](https://developers.mtn.com/products/mtn-product-offering-api-v3)
- **Base URL:** `https://api.mtn.com/v3`

#### Tags

- Customer
- Benin
- Congo
- Côte d'Ivoire
- Cameroon

#### Properties

- [Documentation](https://developers.mtn.com/products/mtn-product-offering-api-v3)
- [API Reference](https://developers.mtn.com/products/mtn-product-offering-api-v3)
- [OpenAPI](openapi/mtn-group-mtn-product-offering-api-v3.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN Retailer Productivity Tracking v1

An API to enable MTN retailers track their productivity KPI's over a period of time. Please refer to the reference guides https://developers.mtn.com/API-Reference-Guides and Response and Error Codes documents https://developers.mtn.com/ResponseCodes.

- **Human URL:** [https://developers.mtn.com/products/mtn-ng-retailer-productivity-tracking-v1](https://developers.mtn.com/products/mtn-ng-retailer-productivity-tracking-v1)
- **Base URL:** `https://api.mtn.com/v1`

#### Tags

- Analytics
- Nigeria

#### Properties

- [Documentation](https://developers.mtn.com/products/mtn-ng-retailer-productivity-tracking-v1)
- [API Reference](https://developers.mtn.com/products/mtn-ng-retailer-productivity-tracking-v1)
- [OpenAPI](openapi/mtn-group-mtn-ng-retailer-productivity-tracking-v1.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN TMF633 - Shopping Cart Management

The Shopping Cart API provides a standardized mechanism for the management of shopping carts. Including creation, update, retrieval.

- **Human URL:** [https://developers.mtn.com/products/tmf633-shopping-cart-management](https://developers.mtn.com/products/tmf633-shopping-cart-management)
- **Base URL:** `https://api.mtn.com/tmf-api/shoppingCart/v1/`

#### Tags

- Customer
- TMF633
- TM Forum
- South Africa

#### Properties

- [Documentation](https://developers.mtn.com/products/tmf633-shopping-cart-management)
- [API Reference](https://developers.mtn.com/products/tmf633-shopping-cart-management)
- [OpenAPI](openapi/mtn-group-tmf633-shopping-cart-management.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN Siebel

This API assesses risks for an MTN customer as well as creates applications.

- **Human URL:** [https://developers.mtn.com/products/siebel](https://developers.mtn.com/products/siebel)
- **Base URL:** `https://api.mtn.com/v1`

#### Tags

- Customer
- South Africa

#### Properties

- [Documentation](https://developers.mtn.com/products/siebel)
- [API Reference](https://developers.mtn.com/products/siebel)
- [OpenAPI](openapi/mtn-group-siebel.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN TMF Party Management - TMF632

This service provides comprehensive party management capabilities for MTN customers including individual and organization management, credit information, and partner services. It serves as the aggregator layer for all TMF632 party-related operations across the MTN ecosystem.

- **Human URL:** [https://developers.mtn.com/products/tmf-party-management](https://developers.mtn.com/products/tmf-party-management)
- **Base URL:** `https://api.mtn.com/v1`

#### Tags

- TM Forum
- TMF632
- Benin
- Congo
- Côte d'Ivoire
- South Sudan

#### Properties

- [Documentation](https://developers.mtn.com/products/tmf-party-management)
- [API Reference](https://developers.mtn.com/products/tmf-party-management)
- [OpenAPI](openapi/mtn-group-tmf-party-management.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN TMF Usage Management - TMF635

This service provides comprehensive usage management capabilities for MTN operations including data usage tracking, subscription management, balance inquiries, and usage analytics. The service integrates with various billing and usage systems to provide real-time usage information across the MTN ecosystem.

- **Human URL:** [https://developers.mtn.com/products/tmf-usage-management-tmf635](https://developers.mtn.com/products/tmf-usage-management-tmf635)
- **Base URL:** `https://api.mtn.com/v1`

#### Tags

- TM Forum
- TMF635
- Côte d'Ivoire
- South Sudan

#### Properties

- [Documentation](https://developers.mtn.com/products/tmf-usage-management-tmf635)
- [API Reference](https://developers.mtn.com/products/tmf-usage-management-tmf635)
- [OpenAPI](openapi/mtn-group-tmf-usage-management-tmf635.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN Usage Management

This service provides comprehensive usage management capabilities for MTN operations including data usage tracking, subscription management, balance inquiries, and usage analytics. The service integrates with various billing and usage systems to provide real-time usage information across the MTN ecosystem.

- **Human URL:** [https://developers.mtn.com/products/usage-management](https://developers.mtn.com/products/usage-management)
- **Base URL:** `https://api.mtn.com/v1`

#### Tags

- Customer
- Benin
- Côte d'Ivoire
- Congo
- Cameroon

#### Properties

- [Documentation](https://developers.mtn.com/products/usage-management)
- [API Reference](https://developers.mtn.com/products/usage-management)
- [OpenAPI](openapi/mtn-group-usage-management.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN MTNID-getInfo

Interface to the Apigee Cloud MTN-ID userinfo function.

- **Human URL:** [https://developers.mtn.com/products/mtnid-getinfo](https://developers.mtn.com/products/mtnid-getinfo)
- **Base URL:** `https://api.mtn.com/mtn-id`

#### Tags

- Identity
- South Africa

#### Properties

- [Documentation](https://developers.mtn.com/products/mtnid-getinfo)
- [API Reference](https://developers.mtn.com/products/mtnid-getinfo)
- [OpenAPI](openapi/mtn-group-mtnid-getinfo.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN Notification V1

To facilitate notifications. Allows 3PPs to register and have notifications processed to them from the applicable backends.

- **Human URL:** [https://developers.mtn.com/products/notification-production](https://developers.mtn.com/products/notification-production)
- **Base URL:** `https://api.mtn.com/v1`

#### Tags

- Messaging
- Congo
- Côte d'Ivoire
- Cameroon
- Ghana

#### Properties

- [Documentation](https://developers.mtn.com/products/notification-production)
- [API Reference](https://developers.mtn.com/products/notification-production)
- [OpenAPI](openapi/mtn-group-notification-production.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN Notification v2

To facilitate notifications. Allows 3PPs to register and have notifications processed to them from the applicable backends.

- **Human URL:** [https://developers.mtn.com/products/notification-v2](https://developers.mtn.com/products/notification-v2)
- **Base URL:** `https://api.mtn.com/v2`

#### Tags

- Messaging
- Congo
- Côte d'Ivoire
- Cameroon
- Ghana

#### Properties

- [Documentation](https://developers.mtn.com/products/notification-v2)
- [API Reference](https://developers.mtn.com/products/notification-v2)
- [OpenAPI](openapi/mtn-group-notification-v2.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN Order Fulfillment

This API provides ability to digital channel to purchase different offers and make payment through Netbanking or Card Payments.

- **Human URL:** [https://developers.mtn.com/products/order-fulfillment](https://developers.mtn.com/products/order-fulfillment)
- **Base URL:** `https://api.mtn.com/v1`

#### Tags

- Customer
- Nigeria

#### Properties

- [Documentation](https://developers.mtn.com/products/order-fulfillment)
- [API Reference](https://developers.mtn.com/products/order-fulfillment)
- [OpenAPI](openapi/mtn-group-order-fulfillment.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN TMF Party Interaction - TMF683

**TMF API Reference : TMF - 683 Party Interaction** **Release : 19.5 - Oct 2019** The Party Interaction Management API provides a mechanism to manage party interactions. Creation, update and retrieval. Including creation, update, retrieval, deletion and notification of event. A Party Interaction captures information about past...

- **Human URL:** [https://developers.mtn.com/products/tmf-party-interaction-tmf683](https://developers.mtn.com/products/tmf-party-interaction-tmf683)
- **Base URL:** `https://api.mtn.com/partyInteraction/v1`

#### Tags

- TM Forum
- TMF683
- Cameroon
- South Africa

#### Properties

- [Documentation](https://developers.mtn.com/products/tmf-party-interaction-tmf683)
- [API Reference](https://developers.mtn.com/products/tmf-party-interaction-tmf683)
- [OpenAPI](openapi/mtn-group-tmf-party-interaction-tmf683.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN Party Management

This API provides standardized mechanism for party management such as creation, update, retrieval and deletion of a party. Party can be an individual or an organization that has any kind of relation with the enterprise.

- **Human URL:** [https://developers.mtn.com/products/mtn-party-management](https://developers.mtn.com/products/mtn-party-management)
- **Base URL:** `https://api.mtn.com/party/v1`

#### Tags

- Customer
- Nigeria
- Ghana

#### Properties

- [Documentation](https://developers.mtn.com/products/mtn-party-management)
- [API Reference](https://developers.mtn.com/products/mtn-party-management)
- [OpenAPI](openapi/mtn-group-mtn-party-management.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN Rwanda Party Management

This API provides standardized mechanism for party management such as creation, update, retrieval and deletion of a party. Party can be an individual or an organization that has any kind of relation with the enterprise.

- **Human URL:** [https://developers.mtn.com/products/rwanda-party-management](https://developers.mtn.com/products/rwanda-party-management)
- **Base URL:** `https://api.mtn.com/party/v1`

#### Tags

- Customer
- Rwanda

#### Properties

- [Documentation](https://developers.mtn.com/products/rwanda-party-management)
- [API Reference](https://developers.mtn.com/products/rwanda-party-management)
- [OpenAPI](openapi/mtn-group-rwanda-party-management.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN Payment Methods V1

A suite of apis for customer payment method details and its data type. **07-July-21: ChangeID: 00000** - Updated the response body for the /paymentMethod endpoint **06-December-21:** - Added a new method for updating the payment method details, as below: PUT /paymentMethod.

- **Human URL:** [https://developers.mtn.com/products/payment-methods-management-sa](https://developers.mtn.com/products/payment-methods-management-sa)
- **Base URL:** `https://api.mtn.com/v1`

#### Tags

- Payments
- South Africa

#### Properties

- [Documentation](https://developers.mtn.com/products/payment-methods-management-sa)
- [API Reference](https://developers.mtn.com/products/payment-methods-management-sa)
- [OpenAPI](openapi/mtn-group-payment-methods-management-sa.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN Payments V1

This is the Payment API for MADAPI. Handles payment use cases such as spTransfer, Debit request, Payment request, and related financial transactions. Provides comprehensive payment processing capabilities including merchant payments, customer payments, transaction status queries, payment history, and reverse payment operations.

- **Human URL:** [https://developers.mtn.com/products/payments-v1](https://developers.mtn.com/products/payments-v1)
- **Base URL:** `https://api.mtn.com/v1`

#### Tags

- Payments
- Benin
- Cameroon
- Congo
- Côte d'Ivoire

#### Properties

- [Documentation](https://developers.mtn.com/products/payments-v1)
- [API Reference](https://developers.mtn.com/products/payments-v1)
- [OpenAPI](openapi/mtn-group-payments-v1.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN TMF Prepay Balance Management - TMF654

This is a sample representation of the Prepay Balance Management TMForum API. It is important to bear in mind that swagger 2.0 does not properly support polymorphism, so the link between the payment method details and its data types should be looked up in the API specification pdf file.

- **Human URL:** [https://developers.mtn.com/products/tmf-prepay-balance-management-tmf654](https://developers.mtn.com/products/tmf-prepay-balance-management-tmf654)
- **Base URL:** `https://api.mtn.com/tmf-api/prepaybalancemanagement/v1/`

#### Tags

- TM Forum
- TMF654
- South Sudan
- Eswatini

#### Properties

- [Documentation](https://developers.mtn.com/products/tmf-prepay-balance-management-tmf654)
- [API Reference](https://developers.mtn.com/products/tmf-prepay-balance-management-tmf654)
- [OpenAPI](openapi/mtn-group-tmf-prepay-balance-management-tmf654.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN Product Catalog - COE

API to provide capability to manage catalog, category, Offerings, Offering price and specification of products.

- **Human URL:** [https://developers.mtn.com/products/product-catalog-coe](https://developers.mtn.com/products/product-catalog-coe)
- **Base URL:** `https://api.mtn.com/tmf-api/productcatalog/v1`

#### Tags

- Customer
- South Africa

#### Properties

- [Documentation](https://developers.mtn.com/products/product-catalog-coe)
- [API Reference](https://developers.mtn.com/products/product-catalog-coe)
- [OpenAPI](openapi/mtn-group-product-catalog-coe.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN Product Catalog Management V1

API to provide capability to manage catalog, category, Offerings, Offering price and specification of products.

- **Human URL:** [https://developers.mtn.com/products/product-catalog-management-v1](https://developers.mtn.com/products/product-catalog-management-v1)
- **Base URL:** `https://api.mtn.com/productCatalogManagement/v1/`

#### Tags

- Customer
- Rwanda
- South Africa

#### Properties

- [Documentation](https://developers.mtn.com/products/product-catalog-management-v1)
- [API Reference](https://developers.mtn.com/products/product-catalog-management-v1)
- [OpenAPI](openapi/mtn-group-product-catalog-management-v1.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN Product Catalogue Management

API to provide capability to manage catalog, category, Offerings, Offering price and specification of products.

- **Human URL:** [https://developers.mtn.com/products/product-catalogue-management](https://developers.mtn.com/products/product-catalogue-management)
- **Base URL:** `https://api.mtn.com/productCatalogManagement/v1/`

#### Tags

- Customer
- Nigeria

#### Properties

- [Documentation](https://developers.mtn.com/products/product-catalogue-management)
- [API Reference](https://developers.mtn.com/products/product-catalogue-management)
- [OpenAPI](openapi/mtn-group-product-catalogue-management.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN TMF Product Catalog - TMF620

API to provide capability to manage catalog, category, Offerings, Offering price and specification of products.

- **Human URL:** [https://developers.mtn.com/products/tmf-product-catalog-tmf620](https://developers.mtn.com/products/tmf-product-catalog-tmf620)
- **Base URL:** `https://api.mtn.com/tmf-api/productcatalog/v1`

#### Tags

- TM Forum
- TMF620
- Benin
- Côte d'Ivoire
- South Sudan
- South Africa

#### Properties

- [Documentation](https://developers.mtn.com/products/tmf-product-catalog-tmf620)
- [API Reference](https://developers.mtn.com/products/tmf-product-catalog-tmf620)
- [OpenAPI](openapi/mtn-group-tmf-product-catalog-tmf620.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN Product Ordering - COE

A Product Order is a type of order which can be used to place an order between a customer and a service provider or between a service provider and a partner and vice versa. Main Product Order attributes are its identifier, state, priority category (mass market, Enterprise, etc.) related dates (start, completion, etc.), related billing...

- **Human URL:** [https://developers.mtn.com/products/product-ordering-coe](https://developers.mtn.com/products/product-ordering-coe)
- **Base URL:** `https://api.mtn.com/tmf-api/productordering/v1`

#### Tags

- Customer
- South Africa

#### Properties

- [Documentation](https://developers.mtn.com/products/product-ordering-coe)
- [API Reference](https://developers.mtn.com/products/product-ordering-coe)
- [OpenAPI](openapi/mtn-group-product-ordering-coe.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN TMF Product Ordering - TMF622

A Product Order is a type of order which can be used to place an order between a customer and a service provider or between a service provider and a partner and vice versa. Main Product Order attributes are its identifier, state, priority category (mass market, Enterprise, etc.) related dates (start, completion, etc.), related billing...

- **Human URL:** [https://developers.mtn.com/products/tmf-product-ordering-tmf622](https://developers.mtn.com/products/tmf-product-ordering-tmf622)
- **Base URL:** `https://api.mtn.com/tmf-api/productordering/v1`

#### Tags

- TM Forum
- TMF622
- Benin
- Côte d'Ivoire
- South Sudan
- Eswatini

#### Properties

- [Documentation](https://developers.mtn.com/products/tmf-product-ordering-tmf622)
- [API Reference](https://developers.mtn.com/products/tmf-product-ordering-tmf622)
- [OpenAPI](openapi/mtn-group-tmf-product-ordering-tmf622.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN Resource Configuration V1

API to provision,configure and activate Resource Functions.

- **Human URL:** [https://developers.mtn.com/products/resource-config-v1](https://developers.mtn.com/products/resource-config-v1)
- **Base URL:** `https://api.mtn.com/v1`

#### Tags

- Customer
- Rwanda

#### Properties

- [Documentation](https://developers.mtn.com/products/resource-config-v1)
- [API Reference](https://developers.mtn.com/products/resource-config-v1)
- [OpenAPI](openapi/mtn-group-resource-config-v1.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN TMF Resource Ordering - TMF652

This is Swagger UI environment generated for the TMF Resource Ordering Management specification.

- **Human URL:** [https://developers.mtn.com/products/tmf-resource-ordering-tmf652](https://developers.mtn.com/products/tmf-resource-ordering-tmf652)
- **Base URL:** `https://api.mtn.com/tmf-api/resourceOrderingManagement/v4/`

#### Tags

- TM Forum
- TMF652
- Benin
- Côte d'Ivoire
- Eswatini
- Zambia

#### Properties

- [Documentation](https://developers.mtn.com/products/tmf-resource-ordering-tmf652)
- [API Reference](https://developers.mtn.com/products/tmf-resource-ordering-tmf652)
- [OpenAPI](openapi/mtn-group-tmf-resource-ordering-tmf652.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN TMF Service Activation - TMF640

Service Activation and Configuration API goal is to provide the ability to activate and configure Service. This API features Monitor pattern allowing to manage service configuration/activation asynchronous request (server side will provide monitor as POST/PATCH response).

- **Human URL:** [https://developers.mtn.com/products/tmf-service-activation-tmf678](https://developers.mtn.com/products/tmf-service-activation-tmf678)
- **Base URL:** `https://api.mtn.com/`

#### Tags

- TM Forum
- TMF640
- Benin
- Eswatini
- Zambia
- Liberia

#### Properties

- [Documentation](https://developers.mtn.com/products/tmf-service-activation-tmf678)
- [API Reference](https://developers.mtn.com/products/tmf-service-activation-tmf678)
- [OpenAPI](openapi/mtn-group-tmf-service-activation-tmf678.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN Job Card Management

An API to share an incident tickets between Remedy and ServiceNow.

- **Human URL:** [https://developers.mtn.com/products/job-card-management](https://developers.mtn.com/products/job-card-management)

#### Tags

- Customer
- Nigeria

#### Properties

- [Documentation](https://developers.mtn.com/products/job-card-management)
- [API Reference](https://developers.mtn.com/products/job-card-management)
- [OpenAPI](openapi/mtn-group-job-card-management.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN Incident API

An API to share an incident tickets between Remedy and ServiceNow.

- **Human URL:** [https://developers.mtn.com/products/ticket](https://developers.mtn.com/products/ticket)
- **Base URL:** `https://api.mtn.com/`

#### Tags

- Ticketing
- Benin
- Cameroon
- Congo
- Côte d'Ivoire

#### Properties

- [Documentation](https://developers.mtn.com/products/ticket)
- [API Reference](https://developers.mtn.com/products/ticket)
- [OpenAPI](openapi/mtn-group-ticket.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN SMS V2

Provides a RESTful API to expose SMS capability.

- **Human URL:** [https://developers.mtn.com/products/mtn-sms-interface](https://developers.mtn.com/products/mtn-sms-interface)
- **Base URL:** `https://api.mtn.com/v2/`

#### Tags

- Messaging
- Côte d'Ivoire
- Congo
- Cameroon
- Ghana

#### Properties

- [Documentation](https://developers.mtn.com/products/mtn-sms-interface)
- [API Reference](https://developers.mtn.com/products/mtn-sms-interface)
- [OpenAPI](openapi/mtn-group-mtn-sms-interface.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN SMS v3 API

Provides a Restful API to expose SMS capability for sending of messages , Mobile originating messages and Delivery Receipts.

- **Human URL:** [https://developers.mtn.com/products/sms-v3-api](https://developers.mtn.com/products/sms-v3-api)
- **Base URL:** `https://api.mtn.com/v3/sms/`

#### Tags

- Messaging
- Benin
- Congo
- Côte d'Ivoire
- Cameroon

#### Properties

- [Documentation](https://developers.mtn.com/products/sms-v3-api)
- [API Reference](https://developers.mtn.com/products/sms-v3-api)
- [OpenAPI](openapi/mtn-group-sms-v3-api.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN SIM Management V1

This API provides a comprehensive suite of services for managing SIM-related operations, including SIM swap initiation, status tracking, eligibility checks, and resource management. It ensures secure and efficient handling of customer SIM lifecycle events.

- **Human URL:** [https://developers.mtn.com/products/sim-management-staging](https://developers.mtn.com/products/sim-management-staging)
- **Base URL:** `https://api.mtn.com/v1`

#### Tags

- Customer
- Benin
- Côte d'Ivoire
- Cameroon
- Congo

#### Properties

- [Documentation](https://developers.mtn.com/products/sim-management-staging)
- [API Reference](https://developers.mtn.com/products/sim-management-staging)
- [OpenAPI](openapi/mtn-group-sim-management-staging.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN SIM Swap Verification V1

The SIM Swap Verification API provides information about an MSISDN's sim-swap details. Supported Operations 1. Get last SIM Swap date of a phone Number.

- **Human URL:** [https://developers.mtn.com/products/sim-swap-verification-v1](https://developers.mtn.com/products/sim-swap-verification-v1)
- **Base URL:** `https://api.mtn.com/v1/mobile/phoneNumbers`

#### Tags

- Customer
- Benin
- Cameroon
- South Sudan

#### Properties

- [Documentation](https://developers.mtn.com/products/sim-swap-verification-v1)
- [API Reference](https://developers.mtn.com/products/sim-swap-verification-v1)
- [OpenAPI](openapi/mtn-group-sim-swap-verification-v1.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN Subscriber Management

This API to be used to manage a Subscriber information.

- **Human URL:** [https://developers.mtn.com/products/subscriber-management](https://developers.mtn.com/products/subscriber-management)
- **Base URL:** `https://api.mtn.com/v1`

#### Tags

- Customer
- Rwanda

#### Properties

- [Documentation](https://developers.mtn.com/products/subscriber-management)
- [API Reference](https://developers.mtn.com/products/subscriber-management)
- [OpenAPI](openapi/mtn-group-subscriber-management.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN Taxation V1

This service provides comprehensive taxation management capabilities for MTN operations including tax calculation, validation, reporting, and compliance. It handles various taxation scenarios including service tax, VAT, and regulatory tax requirements, integrating with multiple tax systems across the MTN ecosystem.

- **Human URL:** [https://developers.mtn.com/products/taxation-v1](https://developers.mtn.com/products/taxation-v1)
- **Base URL:** `https://api.mtn.com/v1`

#### Tags

- Customer
- Ghana

#### Properties

- [Documentation](https://developers.mtn.com/products/taxation-v1)
- [API Reference](https://developers.mtn.com/products/taxation-v1)
- [OpenAPI](openapi/mtn-group-taxation-v1.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN TMF Trouble Ticket - TMF621

TMF621 Trouble Ticket Management Aggregator This service provides endpoint to fetch the ticket details with ticket id, create ticket, fetch list of tickets by customer id and update the existing tickets.

- **Human URL:** [https://developers.mtn.com/products/tmf-trouble-ticket-tmf621](https://developers.mtn.com/products/tmf-trouble-ticket-tmf621)

#### Tags

- TM Forum
- TMF621
- Benin
- Congo
- Cameroon
- Liberia

#### Properties

- [Documentation](https://developers.mtn.com/products/tmf-trouble-ticket-tmf621)
- [API Reference](https://developers.mtn.com/products/tmf-trouble-ticket-tmf621)
- [OpenAPI](openapi/mtn-group-tmf-trouble-ticket-tmf621.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN TMF629 - Customer Management

This is Swagger UI environment generated for the TMF Customer Management specification.

- **Human URL:** [https://developers.mtn.com/products/tmf629-customer-management](https://developers.mtn.com/products/tmf629-customer-management)

#### Tags

- TM Forum
- TMF629
- South Africa
- Ghana

#### Properties

- [Documentation](https://developers.mtn.com/products/tmf629-customer-management)
- [API Reference](https://developers.mtn.com/products/tmf629-customer-management)
- [OpenAPI](openapi/mtn-group-tmf629-customer-management.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN TMF637 Product Inventory

**TMF API Reference : TMF 637 - Product Inventory Management**.

- **Human URL:** [https://developers.mtn.com/products/tmf637-product-inventory](https://developers.mtn.com/products/tmf637-product-inventory)

#### Tags

- TM Forum
- TMF637
- South Africa

#### Properties

- [Documentation](https://developers.mtn.com/products/tmf637-product-inventory)
- [API Reference](https://developers.mtn.com/products/tmf637-product-inventory)
- [OpenAPI](openapi/mtn-group-tmf637-product-inventory.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN Account Management - COE

TMF666 Account Management API with MTN extensions to retrieve financial account transactions, transaction details, outstanding balances, account balances.

- **Human URL:** [https://developers.mtn.com/products/account-management-coe](https://developers.mtn.com/products/account-management-coe)
- **Base URL:** `https://api.mtn.com/tmf-api/financialProfile/v1`

#### Tags

- Customer
- TMF666
- TM Forum
- South Africa

#### Properties

- [Documentation](https://developers.mtn.com/products/account-management-coe)
- [API Reference](https://developers.mtn.com/products/account-management-coe)
- [OpenAPI](openapi/mtn-group-account-management-coe.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN TMF Payment Management - TMF676

TMF676 Payment Management Aggregator API provides comprehensive payment management capabilities following TM Forum TMF676 standards. This service enables payment processing, payment method management, payment status tracking, and payment reconciliation operations. It serves as the central aggregator for all payment-related operations,...

- **Human URL:** [https://developers.mtn.com/products/tmf-payment-management-tmf676](https://developers.mtn.com/products/tmf-payment-management-tmf676)
- **Base URL:** `https://api.mtn.com/v1`

#### Tags

- TM Forum
- TMF676
- Benin

#### Properties

- [Documentation](https://developers.mtn.com/products/tmf-payment-management-tmf676)
- [API Reference](https://developers.mtn.com/products/tmf-payment-management-tmf676)
- [OpenAPI](openapi/mtn-group-tmf-payment-management-tmf676.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN TMF Resource Pool Management - TMF685

This API provides the option to reserver MSISDN for registration and also validate starter pack pairing.

- **Human URL:** [https://developers.mtn.com/products/resource-pool-management](https://developers.mtn.com/products/resource-pool-management)

#### Tags

- TM Forum
- TMF685
- Benin
- Côte d'Ivoire
- Eswatini
- Zambia

#### Properties

- [Documentation](https://developers.mtn.com/products/resource-pool-management)
- [API Reference](https://developers.mtn.com/products/resource-pool-management)
- [OpenAPI](openapi/mtn-group-resource-pool-management.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN TMF Usage Consumption - TMF677

API to fetch Airtime, Currency, Voice, Data and SMS balance details for a subscriber.

- **Human URL:** [https://developers.mtn.com/products/tmf-usage-consumption-tmf677](https://developers.mtn.com/products/tmf-usage-consumption-tmf677)
- **Base URL:** `https://api.mtn.com/usageConsumption/v1/`

#### Tags

- TM Forum
- TMF677
- Côte d'Ivoire
- South Sudan

#### Properties

- [Documentation](https://developers.mtn.com/products/tmf-usage-consumption-tmf677)
- [API Reference](https://developers.mtn.com/products/tmf-usage-consumption-tmf677)
- [OpenAPI](openapi/mtn-group-tmf-usage-consumption-tmf677.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN Usage Consumption V1

API to fetch Airtime, Currency, Voice, Data and SMS balance details for a subscriber.

- **Human URL:** [https://developers.mtn.com/products/usage-consumption](https://developers.mtn.com/products/usage-consumption)
- **Base URL:** `https://api.mtn.com/usageConsumption/v1/`

#### Tags

- Customer
- Rwanda

#### Properties

- [Documentation](https://developers.mtn.com/products/usage-consumption)
- [API Reference](https://developers.mtn.com/products/usage-consumption)
- [OpenAPI](openapi/mtn-group-usage-consumption.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### MTN MoMo Collection API

Enable remote collection of bills, fees or taxes from consumer and business MoMo wallets. Operations include RequestToPay, invoices, pre-approvals, delivery notification, account balance and account holder validation, plus a bc-authorize backchannel consent flow.

- **Human URL:** [https://momodeveloper.mtn.com/api-documentation](https://momodeveloper.mtn.com/api-documentation)
- **Base URL:** `https://sandbox.momodeveloper.mtn.com/collection`

#### Tags

- Mobile Money
- Payments
- Collections

#### Properties

- [Documentation](https://momodeveloper.mtn.com/api-documentation)
- [API Reference](https://momodeveloper.mtn.com/apis)

### MTN MoMo Disbursements API

Disburse payments from a business MoMo wallet to consumers or other businesses — salary payments, benefits disbursement and supplier payouts — with deposit, refund, transfer and transaction-status operations.

- **Human URL:** [https://momodeveloper.mtn.com/api-documentation](https://momodeveloper.mtn.com/api-documentation)
- **Base URL:** `https://sandbox.momodeveloper.mtn.com/disbursement`

#### Tags

- Mobile Money
- Payments
- Disbursements

#### Properties

- [Documentation](https://momodeveloper.mtn.com/api-documentation)
- [API Reference](https://momodeveloper.mtn.com/apis)

### MTN MoMo Remittance API

Transfer funds into MTN MoMo wallets from remittance originators, including cash transfer, transfer, account balance and account holder validation operations.

- **Human URL:** [https://momodeveloper.mtn.com/api-documentation](https://momodeveloper.mtn.com/api-documentation)
- **Base URL:** `https://sandbox.momodeveloper.mtn.com/remittance`

#### Tags

- Mobile Money
- Remittance
- Payments

#### Properties

- [Documentation](https://momodeveloper.mtn.com/api-documentation)
- [API Reference](https://momodeveloper.mtn.com/apis)

### MTN MoMo Sandbox User Provisioning API

Provision sandbox API users and API keys for the MTN MoMo Open API test environment, the self-serve step that lets a developer obtain credentials before calling Collection, Disbursements or Remittance.

- **Human URL:** [https://momodeveloper.mtn.com/api-documentation](https://momodeveloper.mtn.com/api-documentation)
- **Base URL:** `https://sandbox.momodeveloper.mtn.com`

#### Tags

- Mobile Money
- Sandbox
- Onboarding

#### Properties

- [Documentation](https://momodeveloper.mtn.com/api-documentation)
- [API Reference](https://momodeveloper.mtn.com/apis)

## Common Properties

- [Website](https://www.mtn.com/)
- [DeveloperPortal](https://developers.mtn.com/)
- [Documentation](https://developers.mtn.com/getting-started)
- [APIReference](https://developers.mtn.com/products)
- [DeveloperPortal](https://momodeveloper.mtn.com/)
- [Documentation](https://momodeveloper.mtn.com/api-documentation)
- [SignUp](https://developers.mtn.com/register)
- [SignUp](https://momodeveloper.mtn.com/signup)
- [Authentication](https://developers.mtn.com/getting-started)
- [FAQ](https://developers.mtn.com/faq)
- [Support](https://developers.mtn.com/contact)
- [TermsOfService](https://developers.mtn.com/terms-and-conditions)
- [PrivacyPolicy](https://developers.mtn.com/privacy-policy)
- [GitHubOrganization](https://github.com/MTN-Group)
- [LinkedIn](https://www.linkedin.com/company/mtn/)
- [Twitter](https://twitter.com/MTNGroup)
- [YouTube](https://www.youtube.com/user/TheMTNGroup)

## Maintainers

- Kin Lane — kin@apievangelist.com
