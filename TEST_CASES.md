# Test matrix — EU Representative Compliance Navigator

The rules are tested automatically with **16 regression scenarios** in `test_engine.js` (requires Node.js). Example outcomes:

| Case | Input emphasis | Expected result |
| --- | --- | --- |
| Empty questionnaire | All inputs unresolved | All modules: further review |
| US SaaS processing customer data regularly | Non-EU, GDPR 3(2) offer; Article 27 exemption fails | GDPR: representative indicated |
| Truly occasional processing | GDPR occasional + no large-scale Article 9/10 + unlikely risk | GDPR: Article 27 exception indicated |
| No EU GDPR nexus | Neither offer nor behaviour monitoring | GDPR: not indicated |
| Public authority | GDPR Article 27(2)(b) applies | GDPR: not indicated |
| Large-scale special-category data | Occasional yes, but large-scale Article 9/10 yes | GDPR: representative indicated |
| US hosting service targeting EU | Intermediary + EU offering + no EU establishment | DSA: representative indicated |
| Service outside DSA intermediary definition | DSA intermediary=no | DSA: not indicated |
| Provider established in EU | Relevant EU establishment=yes | Non-EU representative pathway not indicated |
| Closed GPAI model entering EU market in 2026 | Third-country provider, non-qualifying open licence | AI Act: representative indicated |
| Qualifying open-source GPAI model without systemic risk | Licence + weights/public info + non-systemic | AI Act: exemption indicated |
| Open-source GPAI model with systemic risk | Open source yes but systemic risk yes | AI Act: representative indicated |
| Legacy GPAI model | First EU market placement before 2 Aug 2025 | AI Act: transition to 2 Aug 2027 |
| Unknown GPAI market placement | EU placement unknown | AI Act: further review |
| Licence open but weights unavailable | Fails one requirement for Article 54(6) | AI Act: representative indicated |
| Unclear EU establishment | Relevant establishment=unknown | Further review, not automatic requirement |

## Human-review situations deliberately not automated

- Whether marketing and targeting amount to an Article 3(2) territorial nexus.
- Correct attribution of controller/processor roles in complex groups.
- Whether processing is occasional or is likely to result in a risk to individuals.
- Classification of novel services as intermediary services under the DSA.
- Whether a model is GPAI and whether it has systemic risk.
- Whether model versions, fine-tuning or substantial changes affect placement and transitional status.

This is a traceable proof of concept, not a production-ready legal opinion engine.