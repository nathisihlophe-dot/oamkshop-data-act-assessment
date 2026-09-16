# Data-Driven Retail Strategy: GDPR and EU Data Act Assessment

OAMKShop is a European retail company operating physical stores and an online shop. It collects purchase data, tracks website and app behaviour, and runs a loyalty programme storing customer names, emails, purchase history, and preferences. It is planning four new uses of this data: selling aggregated regional sales insights to suppliers, using machine learning to recommend products to individual customers, sharing loyalty data with a logistics partner to optimise delivery routes, and letting customers export their purchase history to third-party budgeting apps. This assessment reviews that strategy against GDPR and the EU Data Act.

## Data classification

Most of what OAMKShop holds is personal data under GDPR: names, emails, purchase history, and preferences from the loyalty programme, along with browsing behaviour and cart activity once it is tied to an identifiable customer. Payment method details also count as personal data, though card numbers themselves would typically be held by a payment processor rather than OAMKShop directly.

None of the four planned uses appear to touch special category data under Article 9, there's no health, biometric, or similarly sensitive information described in the scenario. Worth flagging as a boundary case: purchase history could occasionally reveal sensitive inferences, dietary purchases suggesting a health condition, for instance, but this is a minor risk here, not a core issue.

The aggregated, regional-level sales insights OAMKShop wants to sell to suppliers are a different category. Once purchase data is aggregated to the point where no individual customer can be identified, it becomes non-personal, business data, which falls under the EU Data Act rather than GDPR. The distinction matters because it changes which framework governs each of the four planned uses.

## Lawful basis for each planned use

**Selling aggregated insights to suppliers.** If the aggregation is done properly, no individual is identifiable, this sits outside GDPR entirely and is governed by the Data Act instead. The real compliance question here isn't lawful basis, it's whether the anonymisation is genuinely irreversible. If small sample sizes in a region make re-identification possible, the data hasn't actually been anonymised, it's pseudonymised, and GDPR still applies. OAMKShop would need to test this properly, not just assume aggregation equals anonymisation.

**Machine learning product recommendations.** This is direct, identifiable processing of personal data, and legitimate interest is the most workable basis, recommending products based on someone's own purchase history is a reasonably expected part of using a loyalty programme. That said, legitimate interest requires a balancing test, and if the recommendation engine starts drawing on browsing behaviour or cross-referencing sensitive categories of products, the balance shifts and consent becomes the safer basis. Customers should also be able to opt out easily, which supports the legitimate interest argument by showing the processing isn't overreaching.

**Sharing loyalty data with a logistics partner.** This is more constrained. Delivery route optimisation only requires delivery addresses and possibly order size and timing, it does not need full loyalty programme data, purchase history, or preferences. The lawful basis here is contract, performing the delivery is part of fulfilling the sale, but only for the minimum data actually needed. Sharing the customer's full profile with a logistics partner would fail the data minimisation principle even if some legal basis technically existed.

**Exporting purchase history to third-party budgeting apps.** This is customer-initiated, so consent is the natural basis, the customer is actively choosing to share their own data with a tool of their choosing. This is also the clearest case of the right to data portability under GDPR Article 20, and it overlaps directly with Data Act obligations discussed below.

## EU Data Act obligations

The Data Act's portability and sharing obligations are most relevant to two of the four planned uses. For the budgeting app export, OAMKShop needs to provide the data in a structured, commonly used, machine-readable format, and do so without undue delay when the customer requests it. This is a technical and operational commitment, not just a legal one, it requires an actual export mechanism to exist, not just a policy statement that exports are permitted.

If suppliers or the logistics partner request access to data beyond what's already covered by the arrangements above, OAMKShop would need to assess each request against the Data Act's access conditions, considering whether the request is reasonable, whether trade secrets are protected, and whether the requesting party has a legitimate basis for access. The Data Act does not create an unlimited right for any third party to demand OAMKShop's data, access still needs to be justified and appropriately scoped.

## Risks and mitigation

The biggest risk is treating "aggregated" as automatically synonymous with "anonymised" for the supplier insights. If OAMKShop sells regional data that can be re-identified, this is a GDPR breach dressed up as a Data Act compliant business data sale. Mitigation: run a proper anonymisation assessment, including small-sample-size checks by region, before treating this data as non-personal.

The second risk sits with the logistics partner, over-sharing loyalty programme data when only delivery-relevant fields are needed. Mitigation: build a data-sharing agreement that specifies exactly which fields are shared, not a blanket handover of the loyalty database, and enforce this technically, not just contractually.

The third risk is the recommendation engine's legitimate interest basis becoming harder to defend if the system starts using data in ways customers wouldn't reasonably expect, cross-referencing highly personal inferences, for example. Mitigation: keep the recommendation logic auditable, document the balancing test, and give customers a genuine, easy opt-out, not just a link buried in settings.

## Recommendation

The overall strategy is workable under GDPR and the Data Act, but two of the four planned uses need tightening before rollout: the supplier data sale needs a real anonymisation test, not an assumption, and the logistics data share needs to be scoped down to delivery-relevant fields only. The recommendation engine and the budgeting app export are both reasonably sound as planned, provided the recommendation engine stays within a defensible legitimate interest balance and the export mechanism is actually built to Data Act portability standards, not just promised.
