# MTN Group

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

**Areas:** Telecommunications · South Africa · Africa · Mobile Network Operator · Network APIs · Open Gateway · TM Forum · BSS · Mobile Money · Messaging · SMS · USSD

## MTN Group on APIs.io

Everything profiled for MTN Group is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/mtn-group/](https://apis.io/providers/mtn-group/)** — or go straight to one of the APIs or properties below.

### APIs (145)

- [MTN MoMo Collection API](https://apis.io/apis/mtn-group/momo-collection/) — Enable remote collection of bills, fees or taxes from consumer and business MoMo wallets. Operations include RequestToPay, invoices, pre-approvals, delivery…
- [MTN MoMo Disbursements API](https://apis.io/apis/mtn-group/momo-disbursement/) — Disburse payments from a business MoMo wallet to consumers or other businesses — salary payments, benefits disbursement and supplier payouts — with deposit,…
- [MTN MoMo Remittance API](https://apis.io/apis/mtn-group/momo-remittance/) — Transfer funds into MTN MoMo wallets from remittance originators, including cash transfer, transfer, account balance and account holder validation operations.
- [MTN MoMo Sandbox User Provisioning API](https://apis.io/apis/mtn-group/momo-sandbox-user-provisioning/) — Provision sandbox API users and API keys for the MTN MoMo Open API test environment, the self-serve step that lets a developer obtain credentials before…
- [MTN Group Accessible to 3PP API](https://apis.io/apis/mtn-group/mtn-group-accessible-to-3pp-api/) — Accessible to Client APP (3PP) - ApiKeyAuth, to subscribe (MO/MT), unsubscribe and push/send message.
- [MTN Group Accessible to USSD Gateway API](https://apis.io/apis/mtn-group/mtn-group-accessible-to-ussd-gateway-api/) — Used by USSDGW - using ApiKeyAuth, to send MO generated messages to 3PP through MADAPI.
- [MTN Group Activation API](https://apis.io/apis/mtn-group/mtn-group-activation-api/) — The Activation API from MTN Group — 1 operation(s) for activation.
- [MTN Group Add User API](https://apis.io/apis/mtn-group/mtn-group-add-user-api/) — The Add User API from MTN Group — 1 operation(s) for add user.
- [MTN Group Admin Suspend API](https://apis.io/apis/mtn-group/mtn-group-admin-suspend-api/) — The Admin Suspend API from MTN Group — 1 operation(s) for admin suspend.
- [MTN Group Adverts API](https://apis.io/apis/mtn-group/mtn-group-adverts-api/) — The Adverts API from MTN Group — 3 operation(s) for adverts.
- [MTN Group Advice Reconcile API](https://apis.io/apis/mtn-group/mtn-group-advice-reconcile-api/) — The Advice Reconcile API from MTN Group — 1 operation(s) for advice reconcile.
- [MTN Group Agents API](https://apis.io/apis/mtn-group/mtn-group-agents-api/) — The agents API from MTN Group — 4 operation(s) for agents.
- [MTN Group Applied Customer Billing Rate API](https://apis.io/apis/mtn-group/mtn-group-appliedcustomerbillingrate-api/) — The appliedCustomerBillingRate API from MTN Group — 2 operation(s) for appliedcustomerbillingrate.
- [MTN Group Auth API](https://apis.io/apis/mtn-group/mtn-group-auth-api/) — The auth API from MTN Group — 1 operation(s) for auth.
- [MTN Group Balance Buckets Methods API](https://apis.io/apis/mtn-group/mtn-group-balance-buckets-methods-api/) — The Balance Buckets Methods API from MTN Group — 1 operation(s) for balance buckets methods.
- [MTN Group Balance Management API](https://apis.io/apis/mtn-group/mtn-group-balance-management-api/) — The Balance Management API from MTN Group — 1 operation(s) for balance management.
- [MTN Group Balance Transfer API](https://apis.io/apis/mtn-group/mtn-group-balancetransfer-api/) — The BalanceTransfer API from MTN Group — 1 operation(s) for balancetransfer.
- [MTN Group Banktech API](https://apis.io/apis/mtn-group/mtn-group-banktech-api/) — The banktech API from MTN Group — 1 operation(s) for banktech.
- [MTN Group Callback API](https://apis.io/apis/mtn-group/mtn-group-callback-api/) — The Callback API from MTN Group — 2 operation(s) for callback.
- [MTN Group Callmeback API](https://apis.io/apis/mtn-group/mtn-group-callmeback-api/) — The Callmeback API from MTN Group — 1 operation(s) for callmeback.
- [MTN Group callmeback with geographicLocation API](https://apis.io/apis/mtn-group/mtn-group-callmeback-with-geographiclocation-api/) — The callmeback with geographicLocation API from MTN Group — 1 operation(s) for callmeback with geographiclocation.
- [MTN Group Cancel Customer PreApproval API](https://apis.io/apis/mtn-group/mtn-group-cancel-customer-preapproval-api/) — The Cancel Customer PreApproval API from MTN Group — 1 operation(s) for cancel customer preapproval.
- [MTN Group Capability Check API](https://apis.io/apis/mtn-group/mtn-group-capabilitycheck-api/) — The capabilityCheck API from MTN Group — 1 operation(s) for capabilitycheck.
- [MTN Group Catalog API](https://apis.io/apis/mtn-group/mtn-group-catalog-api/) — The catalog API from MTN Group — 2 operation(s) for catalog.
- [MTN Group Category API](https://apis.io/apis/mtn-group/mtn-group-category-api/) — The category API from MTN Group — 1 operation(s) for category.
- [MTN Group Channel Vas Controller API](https://apis.io/apis/mtn-group/mtn-group-channel-vas-controller-api/) — Channel VAS Controller
- [MTN Group Communication API](https://apis.io/apis/mtn-group/mtn-group-communication-api/) — The Communication API from MTN Group — 4 operation(s) for communication.
- [MTN Group Communication Message API](https://apis.io/apis/mtn-group/mtn-group-communicationmessage-api/) — The communicationMessage API from MTN Group — 4 operation(s) for communicationmessage.
- [MTN Group Consent API](https://apis.io/apis/mtn-group/mtn-group-consent-api/) — The Consent API from MTN Group — 2 operation(s) for consent.
- [MTN Group Consent Validation API](https://apis.io/apis/mtn-group/mtn-group-consent-validation-api/) — Consent Validation Implementation to confirm user consent
- [MTN Group Content Push API](https://apis.io/apis/mtn-group/mtn-group-content-push-api/) — The Content Push API from MTN Group — 2 operation(s) for content push.
- [MTN Group Create Customer API](https://apis.io/apis/mtn-group/mtn-group-create-customer-api/) — The Create Customer API from MTN Group — 1 operation(s) for create customer.
- [MTN Group Create Customer PreApproval API](https://apis.io/apis/mtn-group/mtn-group-create-customer-preapproval-api/) — The Create Customer PreApproval API from MTN Group — 1 operation(s) for create customer preapproval.
- [MTN Group Customer API](https://apis.io/apis/mtn-group/mtn-group-customer-api/) — The Customer API from MTN Group — 10 operation(s) for customer.
- [MTN Group Customer Attribute API](https://apis.io/apis/mtn-group/mtn-group-customer-attribute-api/) — The Customer Attribute API from MTN Group — 1 operation(s) for customer attribute.
- [MTN Group Customer Characteristics API](https://apis.io/apis/mtn-group/mtn-group-customer-characteristics-api/) — The Customer Characteristics API from MTN Group — 1 operation(s) for customer characteristics.
- [MTN Group Customer KYC API](https://apis.io/apis/mtn-group/mtn-group-customer-kyc-api/) — The Customer KYC API from MTN Group — 7 operation(s) for customer kyc.
- [MTN Group Customer Mobile Carrier Data API](https://apis.io/apis/mtn-group/mtn-group-customer-mobile-carrier-data-api/) — The Customer Mobile Carrier Data API from MTN Group — 2 operation(s) for customer mobile carrier data.
- [MTN Group Customer Promotion API](https://apis.io/apis/mtn-group/mtn-group-customer-promotion-api/) — The Customer Promotion API from MTN Group — 3 operation(s) for customer promotion.
- [MTN Group Customer Bill On Demand API](https://apis.io/apis/mtn-group/mtn-group-customerbillondemand-api/) — The customerBillOnDemand API from MTN Group — 2 operation(s) for customerbillondemand.
- [MTN Group Customers API](https://apis.io/apis/mtn-group/mtn-group-customers-api/) — The Customers API from MTN Group — 21 operation(s) for customers.
- [MTN Group Customer Transfer Service API](https://apis.io/apis/mtn-group/mtn-group-customertransferservice-api/) — The CustomerTransferService API from MTN Group — 3 operation(s) for customertransferservice.
- [MTN Group Deactivation API](https://apis.io/apis/mtn-group/mtn-group-deactivation-api/) — The Deactivation API from MTN Group — 1 operation(s) for deactivation.
- [MTN Group Debit API](https://apis.io/apis/mtn-group/mtn-group-debit-api/) — The Debit API from MTN Group — 1 operation(s) for debit.
- [MTN Group Device Information API](https://apis.io/apis/mtn-group/mtn-group-device-information-api/) — The Device Information API from MTN Group — 1 operation(s) for device information.
- [MTN Group Device Swap API](https://apis.io/apis/mtn-group/mtn-group-device-swap-api-api/) — The Device Swap API API from MTN Group — 2 operation(s) for device swap api.
- [MTN Group Document API](https://apis.io/apis/mtn-group/mtn-group-document-api/) — The document API from MTN Group — 2 operation(s) for document.
- [MTN Group Employee Leaves API](https://apis.io/apis/mtn-group/mtn-group-employee-leaves-api/) — The Employee Leaves API from MTN Group — 1 operation(s) for employee leaves.
- [MTN Group Event API](https://apis.io/apis/mtn-group/mtn-group-event-api/) — The event API from MTN Group — 2 operation(s) for event.
- [MTN Group events subscription API](https://apis.io/apis/mtn-group/mtn-group-events-subscription-api/) — The events subscription API from MTN Group — 2 operation(s) for events subscription.
- [MTN Group GENEYSIS EEC TOKENS API](https://apis.io/apis/mtn-group/mtn-group-geneysis-eec-tokens-api/) — The GENEYSIS-EEC-TOKENS API from MTN Group — 1 operation(s) for geneysis-eec-tokens.
- [MTN Group Get access token API](https://apis.io/apis/mtn-group/mtn-group-get-access-token-api/) — The Get access token API from MTN Group — 1 operation(s) for get access token.
- [MTN Group Hub API](https://apis.io/apis/mtn-group/mtn-group-hub-api/) — The hub API from MTN Group — 2 operation(s) for hub.
- [MTN Group Incident ticket API](https://apis.io/apis/mtn-group/mtn-group-incident-ticket-api/) — The Incident ticket API from MTN Group — 1 operation(s) for incident ticket.
- [MTN Group Individual API](https://apis.io/apis/mtn-group/mtn-group-individual-api/) — The individual API from MTN Group — 2 operation(s) for individual.
- [MTN Group Kyc API](https://apis.io/apis/mtn-group/mtn-group-kyc-api/) — The Kyc API from MTN Group — 2 operation(s) for kyc.
- [MTN Group License Aggregator Controller API](https://apis.io/apis/mtn-group/mtn-group-license-aggregator-controller-api/) — The license-aggregator-controller API from MTN Group — 2 operation(s) for license-aggregator-controller.
- [MTN Group Link Accounts API](https://apis.io/apis/mtn-group/mtn-group-link-accounts-api/) — The Link Accounts API from MTN Group — 1 operation(s) for link accounts.
- [MTN Group Loyalty Balance API](https://apis.io/apis/mtn-group/mtn-group-loyalty-balance-api/) — The Loyalty Balance API from MTN Group — 1 operation(s) for loyalty balance.
- [MTN Group Loyalty Burn API](https://apis.io/apis/mtn-group/mtn-group-loyalty-burn-api/) — The Loyalty Burn API from MTN Group — 1 operation(s) for loyalty burn.
- [MTN Group Loyalty Member API](https://apis.io/apis/mtn-group/mtn-group-loyalty-member-api/) — The Loyalty Member API from MTN Group — 2 operation(s) for loyalty member.
- [MTN Group Loyalty Program Product API](https://apis.io/apis/mtn-group/mtn-group-loyalty-program-product-api/) — The Loyalty Program Product API from MTN Group — 2 operation(s) for loyalty program product.
- [MTN Group Member Summary API](https://apis.io/apis/mtn-group/mtn-group-member-summary-api/) — The Member Summary API from MTN Group — 1 operation(s) for member summary.
- [MTN Group Mo Mo API](https://apis.io/apis/mtn-group/mtn-group-momo-api/) — The MoMo API from MTN Group — 1 operation(s) for momo.
- [MTN Group Monitor API](https://apis.io/apis/mtn-group/mtn-group-monitor-api/) — The monitor API from MTN Group — 2 operation(s) for monitor.
- [MTN Group Netflix Integration Controller API](https://apis.io/apis/mtn-group/mtn-group-netflix-integration-controller-api/) — The netflix-integration-controller API from MTN Group — 4 operation(s) for netflix-integration-controller.
- [MTN Group notification listeners (client side) API](https://apis.io/apis/mtn-group/mtn-group-notification-listeners-client-side-api/) — The notification listeners (client side) API from MTN Group — 15 operation(s) for notification listeners (client side).
- [MTN Group Notifications API](https://apis.io/apis/mtn-group/mtn-group-notifications-api/) — Send Notifications
- [MTN Group Number Recycle Service API](https://apis.io/apis/mtn-group/mtn-group-numberrecycleservice-api/) — The NumberRecycleService API from MTN Group — 1 operation(s) for numberrecycleservice.
- [MTN Group Organization API](https://apis.io/apis/mtn-group/mtn-group-organization-api/) — The organization API from MTN Group — 2 operation(s) for organization.
- [MTN Group Organizations API](https://apis.io/apis/mtn-group/mtn-group-organizations-api/) — The Organizations API from MTN Group — 3 operation(s) for organizations.
- [MTN Group OTP API](https://apis.io/apis/mtn-group/mtn-group-otp-api/) — The OTP API from MTN Group — 2 operation(s) for otp.
- [MTN Group Partners API](https://apis.io/apis/mtn-group/mtn-group-partners-api/) — The partners API from MTN Group — 2 operation(s) for partners.
- [MTN Group Party Account API](https://apis.io/apis/mtn-group/mtn-group-partyaccount-api/) — The partyAccount API from MTN Group — 1 operation(s) for partyaccount.
- [MTN Group Party Interaction API](https://apis.io/apis/mtn-group/mtn-group-partyinteraction-api/) — The partyInteraction API from MTN Group — 1 operation(s) for partyinteraction.
- [MTN Group Party Role Risk Assessment API](https://apis.io/apis/mtn-group/mtn-group-partyroleriskassessment-api/) — The partyRoleRiskAssessment API from MTN Group — 8 operation(s) for partyroleriskassessment.
- [MTN Group Payment API](https://apis.io/apis/mtn-group/mtn-group-payment-api/) — The Payment API from MTN Group — 13 operation(s) for payment.
- [MTN Group payment methods API](https://apis.io/apis/mtn-group/mtn-group-payment-methods-api/) — The payment methods API from MTN Group — 2 operation(s) for payment methods.
- [MTN Group PIN API](https://apis.io/apis/mtn-group/mtn-group-pin-api/) — The PIN API from MTN Group — 2 operation(s) for pin.
- [MTN Group Policy API](https://apis.io/apis/mtn-group/mtn-group-policy-api/) — The Policy API from MTN Group — 1 operation(s) for policy.
- [MTN Group Premiums API](https://apis.io/apis/mtn-group/mtn-group-premiums-api/) — The Premiums API from MTN Group — 1 operation(s) for premiums.
- [MTN Group Process Operations API](https://apis.io/apis/mtn-group/mtn-group-process-operations-api/) — The Process Operations API from MTN Group — 6 operation(s) for process operations.
- [MTN Group Product API](https://apis.io/apis/mtn-group/mtn-group-product-api/) — The product API from MTN Group — 2 operation(s) for product.
- [MTN Group Productivity Report API](https://apis.io/apis/mtn-group/mtn-group-productivity-report-api/) — The Productivity Report API from MTN Group — 1 operation(s) for productivity report.
- [MTN Group Product Offering API](https://apis.io/apis/mtn-group/mtn-group-productoffering-api/) — The productOffering API from MTN Group — 1 operation(s) for productoffering.
- [MTN Group Product Order API](https://apis.io/apis/mtn-group/mtn-group-productorder-api/) — The productOrder API from MTN Group — 2 operation(s) for productorder.
- [MTN Group Products API](https://apis.io/apis/mtn-group/mtn-group-products-api/) — The products API from MTN Group — 13 operation(s) for products.
- [MTN Group Provider API](https://apis.io/apis/mtn-group/mtn-group-provider-api/) — The Provider API from MTN Group — 3 operation(s) for provider.
- [MTN Group Purchase API](https://apis.io/apis/mtn-group/mtn-group-purchase-api/) — The Purchase API from MTN Group — 1 operation(s) for purchase.
- [MTN Group Query By Data API](https://apis.io/apis/mtn-group/mtn-group-query-by-data-api/) — The Query By Data API from MTN Group — 1 operation(s) for query by data.
- [MTN Group Query By Transaction ID API](https://apis.io/apis/mtn-group/mtn-group-query-by-transaction-id-api/) — The Query By Transaction ID API from MTN Group — 1 operation(s) for query by transaction id.
- [MTN Group Query logback by targetURL and country code API](https://apis.io/apis/mtn-group/mtn-group-query-logback-by-targeturl-and-country-code-api/) — The Query logback by targetURL and country code API from MTN Group — 1 operation(s) for query logback by targeturl and country code.
- [MTN Group Quotation API](https://apis.io/apis/mtn-group/mtn-group-quotation-api/) — The Quotation API from MTN Group — 1 operation(s) for quotation.
- [MTN Group Receiving SMS API](https://apis.io/apis/mtn-group/mtn-group-receiving-sms-api/) — The Receiving SMS API from MTN Group — 1 operation(s) for receiving sms.
- [MTN Group Reference Data Operations API](https://apis.io/apis/mtn-group/mtn-group-reference-data-operations-api/) — The Reference Data Operations API from MTN Group — 3 operation(s) for reference data operations.
- [MTN Group Refund API](https://apis.io/apis/mtn-group/mtn-group-refund-api/) — The Refund API from MTN Group — 1 operation(s) for refund.
- [MTN Group Registration API](https://apis.io/apis/mtn-group/mtn-group-registration-api/) — The Registration API from MTN Group — 7 operation(s) for registration.
- [MTN Group Reporting API](https://apis.io/apis/mtn-group/mtn-group-reporting-api/) — The Reporting API from MTN Group — 1 operation(s) for reporting.
- [MTN Group Resource API](https://apis.io/apis/mtn-group/mtn-group-resource-api/) — The resource API from MTN Group — 2 operation(s) for resource.
- [MTN Group Resource Function API](https://apis.io/apis/mtn-group/mtn-group-resourcefunction-api/) — The ResourceFunction API from MTN Group — 1 operation(s) for resourcefunction.
- [MTN Group Resource Order API](https://apis.io/apis/mtn-group/mtn-group-resourceorder-api/) — The resourceOrder API from MTN Group — 2 operation(s) for resourceorder.
- [MTN Group Sales Lead API](https://apis.io/apis/mtn-group/mtn-group-saleslead-api/) — The salesLead API from MTN Group — 1 operation(s) for saleslead.
- [MTN Group Sending SMS API](https://apis.io/apis/mtn-group/mtn-group-sending-sms-api/) — The Sending SMS API from MTN Group — 4 operation(s) for sending sms.
- [MTN Group Service Activation Controller API](https://apis.io/apis/mtn-group/mtn-group-service-activation-controller-api/) — The service-activation-controller API from MTN Group — 1 operation(s) for service-activation-controller.
- [MTN Group Service API](https://apis.io/apis/mtn-group/mtn-group-service-api/) — The service API from MTN Group — 2 operation(s) for service.
- [MTN Group Siebel API](https://apis.io/apis/mtn-group/mtn-group-siebel-api/) — The siebel API from MTN Group — 3 operation(s) for siebel.
- [MTN Group Sim Activation API](https://apis.io/apis/mtn-group/mtn-group-sim-activation-api/) — The Sim Activation API from MTN Group — 2 operation(s) for sim activation.
- [MTN Group SIM & MSISDN Availability APIs API](https://apis.io/apis/mtn-group/mtn-group-sim-msisdn-availability-apis-api/) — The SIM & MSISDN Availability APIs API from MTN Group — 3 operation(s) for sim & msisdn availability apis.
- [MTN Group Sim Recycle API](https://apis.io/apis/mtn-group/mtn-group-sim-recycle-api/) — The Sim Recycle API from MTN Group — 1 operation(s) for sim recycle.
- [MTN Group SIM Swap API](https://apis.io/apis/mtn-group/mtn-group-sim-swap-api-api/) — The SIM Swap API API from MTN Group — 1 operation(s) for sim swap api.
- [MTN Group Sim Swap API](https://apis.io/apis/mtn-group/mtn-group-sim-swap-api/) — The Sim Swap API from MTN Group — 2 operation(s) for sim swap.
- [MTN Group Sim Management Service API](https://apis.io/apis/mtn-group/mtn-group-simmanagementservice-api/) — The SimManagementService API from MTN Group — 11 operation(s) for simmanagementservice.
- [MTN Group Status API](https://apis.io/apis/mtn-group/mtn-group-status-api/) — The status API from MTN Group — 3 operation(s) for status.
- [MTN Group Submit Withdrawal Request API](https://apis.io/apis/mtn-group/mtn-group-submit-withdrawal-request-api/) — The Submit Withdrawal Request API from MTN Group — 1 operation(s) for submit withdrawal request.
- [MTN Group Subscriber Attributes Controller API](https://apis.io/apis/mtn-group/mtn-group-subscriber-attributes-controller-api/) — Subscriber Attributes Controller
- [MTN Group Subscriber Type API](https://apis.io/apis/mtn-group/mtn-group-subscriber-type-api/) — The Subscriber Type API from MTN Group — 1 operation(s) for subscriber type.
- [MTN Group Subscriberinfo API](https://apis.io/apis/mtn-group/mtn-group-subscriberinfo-api/) — The subscriberinfo API from MTN Group — 2 operation(s) for subscriberinfo.
- [MTN Group Subscribing for Mobile Originating and Delivery Receipts API](https://apis.io/apis/mtn-group/mtn-group-subscribing-for-mobile-originating-and-delivery-receipts-api/) — The Subscribing for Mobile Originating and Delivery Receipts API from MTN Group — 2 operation(s) for subscribing for mobile originating and delivery receipts.
- [MTN Group Taxation API](https://apis.io/apis/mtn-group/mtn-group-taxation-api/) — The Taxation API from MTN Group — 1 operation(s) for taxation.
- [MTN Group TMF632 Party Management API](https://apis.io/apis/mtn-group/mtn-group-tmf632-party-management-api/) — The TMF632 Party Management API from MTN Group — 5 operation(s) for tmf632 party management.
- [MTN Group TMF676 Payment Management Aggregator API](https://apis.io/apis/mtn-group/mtn-group-tmf676-payment-management-aggregator-api/) — The TMF676 Payment Management Aggregator API from MTN Group — 2 operation(s) for tmf676 payment management aggregator.
- [MTN Group TMF908 IoT Device Management API](https://apis.io/apis/mtn-group/mtn-group-tmf908-iot-device-management-api/) — The TMF908 IoT Device Management API from MTN Group — 3 operation(s) for tmf908 iot device management.
- [MTN Group Topic API](https://apis.io/apis/mtn-group/mtn-group-topic-api/) — The topic API from MTN Group — 2 operation(s) for topic.
- [MTN Group Track ticket API](https://apis.io/apis/mtn-group/mtn-group-track-ticket-api/) — The Track ticket API from MTN Group — 2 operation(s) for track ticket.
- [MTN Group Trouble Ticket Aggregator Controller API](https://apis.io/apis/mtn-group/mtn-group-trouble-ticket-aggregator-controller-api/) — The trouble-ticket-aggregator-controller API from MTN Group — 5 operation(s) for trouble-ticket-aggregator-controller.
- [MTN Group Unified Balance Enquiry API](https://apis.io/apis/mtn-group/mtn-group-unified-balance-enquiry-api/) — The Unified Balance Enquiry API from MTN Group — 1 operation(s) for unified balance enquiry.
- [MTN Group URL Create API](https://apis.io/apis/mtn-group/mtn-group-urlcreate-api/) — The urlCreate API from MTN Group — 1 operation(s) for urlcreate.
- [MTN Group Usage Limit Adjust API](https://apis.io/apis/mtn-group/mtn-group-usage-limit-adjust-api/) — The Usage Limit Adjust API from MTN Group — 1 operation(s) for usage limit adjust.
- [MTN Group Usage Consumption Report API](https://apis.io/apis/mtn-group/mtn-group-usageconsumptionreport-api/) — The usageConsumptionReport API from MTN Group — 2 operation(s) for usageconsumptionreport.
- [MTN Group Usage Management API](https://apis.io/apis/mtn-group/mtn-group-usagemanagement-api/) — The UsageManagement API from MTN Group — 12 operation(s) for usagemanagement.
- [MTN Group Usage Managements S Sd API](https://apis.io/apis/mtn-group/mtn-group-usagemanagementsssd-api/) — The UsageManagementsSSd API from MTN Group — 3 operation(s) for usagemanagementsssd.
- [MTN Group Users API](https://apis.io/apis/mtn-group/mtn-group-users-api/) — The Users API from MTN Group — 3 operation(s) for users.
- [MTN Group Validate an Individual's Account Status API](https://apis.io/apis/mtn-group/mtn-group-validate-an-individual-s-account-status-api/) — The Validate an Individual's Account Status API from MTN Group — 1 operation(s) for validate an individual's account status.
- [MTN Group Validate Customer API](https://apis.io/apis/mtn-group/mtn-group-validate-customer-api/) — The Validate Customer API from MTN Group — 1 operation(s) for validate customer.
- [MTN Group Validate using QnA API](https://apis.io/apis/mtn-group/mtn-group-validate-using-qna-api/) — The Validate using QnA API from MTN Group — 2 operation(s) for validate using qna.
- [MTN Group VAS Services API](https://apis.io/apis/mtn-group/mtn-group-vas-services-api/) — The VAS Services API from MTN Group — 5 operation(s) for vas services.
- [MTN Group Verify a Partner's FInancial Resources API](https://apis.io/apis/mtn-group/mtn-group-verify-a-partner-s-financial-resources-api/) — The Verify a Partner's FInancial Resources API from MTN Group — 1 operation(s) for verify a partner's financial resources.
- [MTN Group Channel Service API](https://apis.io/apis/mtn-group/mtn-group-channel-service-api/) — The Channel Service API from MTN Group — 1 operation(s) for channel service.
- [MTN Group Customer Bill API](https://apis.io/apis/mtn-group/mtn-group-customer-bill-api/) — The Customer Bill API from MTN Group — 2 operation(s) for customer bill.
- [MTN Group Financial Account API](https://apis.io/apis/mtn-group/mtn-group-financial-account-api/) — The Financial Account API from MTN Group — 4 operation(s) for financial account.
- [MTN Group Fraud Management API](https://apis.io/apis/mtn-group/mtn-group-fraud-management-api/) — The Fraud Management API from MTN Group — 2 operation(s) for fraud management.
- [MTN Group Get Info API](https://apis.io/apis/mtn-group/mtn-group-get-info-api/) — The Get Info API from MTN Group — 1 operation(s) for get info.
- [MTN Group Order Fulfillment API](https://apis.io/apis/mtn-group/mtn-group-order-fulfillment-api/) — The Order Fulfillment API from MTN Group — 1 operation(s) for order fulfillment.
- [MTN Group Service Order API](https://apis.io/apis/mtn-group/mtn-group-service-order-api/) — The Service Order API from MTN Group — 2 operation(s) for service order.
- [MTN Group Shopping Cart API](https://apis.io/apis/mtn-group/mtn-group-shopping-cart-api/) — The Shopping Cart API from MTN Group — 6 operation(s) for shopping cart.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [Mtn Group Webhooks](https://apis.io/asyncapis/mtn-group/mtn-group-webhooks/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [mtn-group](https://apis.io/servers/mtn-group/mtn-group/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Mtn Group Agentic Access](https://apis.io/agentic-access/mtn-group/mtn-group-agentic-access/)

#### Collections (107)

Postman and Open Collection request collections.

- [Account Decisioning API](https://apis.io/collections/mtn-group/open-mtn-group-account-decisioning/)
- [TMF666 Account Management API](https://apis.io/collections/mtn-group/open-mtn-group-account-management-coe/)
- [Mobile Advertisement](https://apis.io/collections/mtn-group/open-mtn-group-advertising-v2/)
- [MTN Agent Profile API](https://apis.io/collections/mtn-group/open-mtn-group-agent-profile/)
- [Consent Validation API](https://apis.io/collections/mtn-group/open-mtn-group-ayo-preapproval/)
- [MTN Accountholders API](https://apis.io/collections/mtn-group/open-mtn-group-ayoaccountholderinfo/)
- [Balance Management V1](https://apis.io/collections/mtn-group/open-mtn-group-balance-management-v1/)
- [Authentication APIs](https://apis.io/collections/mtn-group/open-mtn-group-bss-tt-oauth-v1/)
- [Callmeback V1](https://apis.io/collections/mtn-group/open-mtn-group-callmeback-v1/)
- [Callmeback V2](https://apis.io/collections/mtn-group/open-mtn-group-callmeback-v2/)
- [Communication Management API](https://apis.io/collections/mtn-group/open-mtn-group-communication-management-v1/)
- [Content Push API](https://apis.io/collections/mtn-group/open-mtn-group-content-push/)
- [MTN Customer Account Management API](https://apis.io/collections/mtn-group/open-mtn-group-customer-account-management-v1/)
- [Customer Billing Token API](https://apis.io/collections/mtn-group/open-mtn-group-customer-billing-token-v1/)
- [Customer Transfer](https://apis.io/collections/mtn-group/open-mtn-group-customer-data-transfer-ng-prod/)
- [Customer Delivery Booking API](https://apis.io/collections/mtn-group/open-mtn-group-customer-delivery-booking/)
- [Customer Identification API](https://apis.io/collections/mtn-group/open-mtn-group-customer-identification-v1/)
- [MTN Customer KYC Verification API](https://apis.io/collections/mtn-group/open-mtn-group-customer-kyc-verification/)
- [Customer Loyalty Management API](https://apis.io/collections/mtn-group/open-mtn-group-customer-loyalty-management/)
- [MTN Customer Management API](https://apis.io/collections/mtn-group/open-mtn-group-customer-management/)
- [Customer Management - COE](https://apis.io/collections/mtn-group/open-mtn-group-customer-management-coe-za-preprod/)
- [Customer PIN Management API](https://apis.io/collections/mtn-group/open-mtn-group-customer-pin-management-v2/)
- [Customer Promotion Placeholder](https://apis.io/collections/mtn-group/open-mtn-group-customer-promotion/)
- [Device Swap API](https://apis.io/collections/mtn-group/open-mtn-group-device-swap-v1/)
- [Digital Partners Management API](https://apis.io/collections/mtn-group/open-mtn-group-digital-partner-management/)
- …and 82 more published on APIs.io

#### Overlays (115)

OpenAPI overlays, including conversational phrasing for each operation.

- [Mtn Group Account Decisioning Overlay](https://apis.io/overlays/mtn-group/mtn-group-account-decisioning-overlay/)
- [Mtn Group Account Management Coe Overlay](https://apis.io/overlays/mtn-group/mtn-group-account-management-coe-overlay/)
- [Mtn Group Advertising V2 Overlay](https://apis.io/overlays/mtn-group/mtn-group-advertising-v2-overlay/)
- [Mtn Group Agent Profile Overlay](https://apis.io/overlays/mtn-group/mtn-group-agent-profile-overlay/)
- [Mtn Group Ayo Preapproval Overlay](https://apis.io/overlays/mtn-group/mtn-group-ayo-preapproval-overlay/)
- [Mtn Group Ayoaccountholderinfo Overlay](https://apis.io/overlays/mtn-group/mtn-group-ayoaccountholderinfo-overlay/)
- [Mtn Group Balance Management V1 Overlay](https://apis.io/overlays/mtn-group/mtn-group-balance-management-v1-overlay/)
- [Mtn Group Bss Tt Oauth V1 Overlay](https://apis.io/overlays/mtn-group/mtn-group-bss-tt-oauth-v1-overlay/)
- [Mtn Group Callmeback V1 Overlay](https://apis.io/overlays/mtn-group/mtn-group-callmeback-v1-overlay/)
- [Mtn Group Callmeback V2 Overlay](https://apis.io/overlays/mtn-group/mtn-group-callmeback-v2-overlay/)
- [Mtn Group Communication Management V1 Overlay](https://apis.io/overlays/mtn-group/mtn-group-communication-management-v1-overlay/)
- [Mtn Group Content Push Overlay](https://apis.io/overlays/mtn-group/mtn-group-content-push-overlay/)
- [Mtn Group Customer Account Management V1 Overlay](https://apis.io/overlays/mtn-group/mtn-group-customer-account-management-v1-overlay/)
- [Mtn Group Customer Billing Token V1 Overlay](https://apis.io/overlays/mtn-group/mtn-group-customer-billing-token-v1-overlay/)
- [Mtn Group Customer Data Transfer Ng Prod Overlay](https://apis.io/overlays/mtn-group/mtn-group-customer-data-transfer-ng-prod-overlay/)
- [Mtn Group Customer Delivery Booking Overlay](https://apis.io/overlays/mtn-group/mtn-group-customer-delivery-booking-overlay/)
- [Mtn Group Customer Identification V1 Overlay](https://apis.io/overlays/mtn-group/mtn-group-customer-identification-v1-overlay/)
- [Mtn Group Customer Kyc Verification Overlay](https://apis.io/overlays/mtn-group/mtn-group-customer-kyc-verification-overlay/)
- [Mtn Group Customer Loyalty Management Overlay](https://apis.io/overlays/mtn-group/mtn-group-customer-loyalty-management-overlay/)
- [Mtn Group Customer Management Coe Za Preprod Overlay](https://apis.io/overlays/mtn-group/mtn-group-customer-management-coe-za-preprod-overlay/)
- [Mtn Group Customer Management Overlay](https://apis.io/overlays/mtn-group/mtn-group-customer-management-overlay/)
- [Mtn Group Customer Pin Management V2 Overlay](https://apis.io/overlays/mtn-group/mtn-group-customer-pin-management-v2-overlay/)
- [Mtn Group Customer Promotion Overlay](https://apis.io/overlays/mtn-group/mtn-group-customer-promotion-overlay/)
- [Mtn Group Customer Survey Overlay](https://apis.io/overlays/mtn-group/mtn-group-customer-survey-overlay/)
- [Mtn Group Device Swap V1 Overlay](https://apis.io/overlays/mtn-group/mtn-group-device-swap-v1-overlay/)
- …and 90 more published on APIs.io

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Mtn Group Authentication](https://apis.io/security/mtn-group/mtn-group-authentication/)
- [Mtn Group Domain Security](https://apis.io/security/mtn-group/mtn-group-domain-security/)

#### OAuth scopes (1)

The permissions the API asks for.

- [Mtn Group Scopes](https://apis.io/scopes/mtn-group/mtn-group-scopes/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.mtn.com/)
- [Documentation](https://developers.mtn.com/getting-started)
- [Getting started](https://developers.mtn.com/getting-started)
- [API reference](https://developers.mtn.com/products)
- [Sign up](https://developers.mtn.com/register)
- [Support](https://developers.mtn.com/contact)
- [Blog](https://www.mtn.com/newsroom/)
- [Terms of service](https://developers.mtn.com/terms-and-conditions)
- [Privacy policy](https://developers.mtn.com/privacy-policy)
- [GitHub](https://github.com/MTN-Group)

## API Evangelist rating

**Kin Score 52.1** — developing · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 78.6 |
| Contract quality | 54.0 |
| Contract governance | 18.2 |
| Operational transparency | 18.4 |
| Developer ergonomics | 66.1 |
| Access clarity | 34.2 |

**Agent readiness 36.5** — agent-ready

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | documented (partial credit) |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | documented (partial credit) |
| Error Semantics | verified |
| OpenAPI Examples | partial |
| Rate Limit Signal | — |
| Event Surface Described | yes |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | partial |
| Operation Distinctiveness | mostly |

**Regulatory alignment 40.0** — Telecommunications

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/mtn-group/](https://apis.io/providers/mtn-group/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for MTN Group: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/mtn-group/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
