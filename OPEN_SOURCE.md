# Open-source exploration

These are upstream projects I am exploring for learning and possible future contributions. **Forking is not authorship or a contribution.** No completed upstream contribution is claimed, and the exploration forks have not received cosmetic commits.

My application work and genuine team projects remain in the [profile README](README.md).

## Focused collection

| Upstream → exploration fork | Why this fits | One realistic next opportunity |
| --- | --- | --- |
| [flutter/samples](https://github.com/flutter/samples) → [samples](https://github.com/aliosama990/samples) | Official examples of Flutter UI, architecture and tests; useful alongside Provider-based Malaz work. | Investigate test isolation in `testing_app/test/models/favorites_test.dart`, whose group shares a Favorites instance. Propose per-test setup with meaningful state/notification assertions if maintainers agree it improves the example. |
| [cfug/dio](https://github.com/cfug/dio) → [dio](https://github.com/aliosama990/dio) | HTTP clients, interceptors, cancellation and adapter behavior for mobile API integrations. | Reproduce one reported cancellation edge case against `dio/test/cancel_token_test.dart` and the shared cancellation suite; contribute a failing regression test and minimal fix only after confirming the gap. |
| [laravel/sanctum](https://github.com/laravel/sanctum) → [sanctum](https://github.com/aliosama990/sanctum) | Practical Laravel API authentication, tokens and ability checks. | Build a small local token-ability fixture, then investigate a reported middleware edge case using `tests/Unit/CheckAbilitiesTest.php`; submit coverage only for a verified missing behavior. |
| [pestphp/pest](https://github.com/pestphp/pest) → [pest](https://github.com/aliosama990/pest) | Readable PHP tests, assertions and regression-driven development. | Reproduce a reported dataset/filtering failure in a minimal Pest test, then add a regression test and narrowly scoped fix following the contribution guide. |
| [felangel/mason](https://github.com/felangel/mason) → [mason](https://github.com/aliosama990/mason) | Reusable Dart bricks and CLI automation for consistent project scaffolding. | Experiment locally with a Provider/service/test brick; if a reproducible CLI generation problem emerges, extend `packages/mason_cli/test/commands/make_test.dart` with a fixture and propose the smallest fix. |
| [laravel/mcp](https://github.com/laravel/mcp) → [mcp](https://github.com/aliosama990/mcp) | Connects Laravel development with MCP tools, validation and AI-client workflows. | Explore localized or nested validation errors around `tests/Unit/Support/ValidationMessagesTest.php`; propose a regression test only if a real tool-response inconsistency can be reproduced. |

The opportunities above are investigation directions, **not confirmed bugs, accepted issues or completed work**. Check current issues, existing tests and maintainer guidance before starting.

## First contribution workflow

1. Pick one repository and read its contribution instructions and any applicable agent guidance.
2. Sync the fork and reproduce a specific issue on the intended upstream branch.
3. Agree on scope with maintainers where required, then create a focused branch.
4. Add a test that fails for the reported problem; make the smallest relevant change.
5. Run the project's required checks and report exactly what ran.
6. Submit a clear upstream pull request only when the work is ready.

For Flutter Samples, discuss the change in an issue first; upstream also requires its contributor agreement before merging. Do not sign agreements on anyone else's behalf. Dio requires concrete motivation, regression tests and compatibility review; feature work needs prior discussion.

## Attribution and licensing

GitHub's upstream fork relationship, commit history and license files are preserved. Flutter Samples includes BSD-style code terms and additional font licensing; retain all applicable notices. Dio, Sanctum, Pest and Laravel MCP use MIT licenses. Mason's packages carry MIT license files. Check package/asset-specific notices before reuse.

No upstream repository was modified by this curation. No issues, pull requests or contribution claims were manufactured.
