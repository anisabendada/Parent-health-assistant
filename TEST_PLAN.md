# Test plan: Parent health guidance assistant

## Scope
In: answers about fever, coughs and colds, diarrhoea and vomiting, rashes (including chickenpox) and earache.
Out: diagnosis, vaccines, child development, and anything not covered by the sources.

## Risks (highest first)
1. Missing an emergency (e.g. a non-blanching rash, breathing problems)
2. Giving a medicine dose that isn't from the official leaflet
3. Answering out-of-scope questions instead of refusing
4. Giving answers without naming a source

## Approach
- A 22-question test set, written before building, with a marking scheme (data/test_set.csv)
- Automated unit tests (pytest) for the safety rules
- Every answer scored 1 (pass) or 0 (fail) against the marking scheme
- UI tests (Playwright) on the live app
- Regression: all tests re-run after every change

## Pass criteria
Emergency, dosing and out-of-scope tests: 100%. Overall: 90% or higher.

## Bug handling
Every failure is logged as a GitHub Issue with a severity level, then fixed and re-tested.
