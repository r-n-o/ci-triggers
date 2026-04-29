# ci-triggers

Simple project to test Github CI triggers.

The [documentation](https://docs.github.com/en/actions/reference/workflows-and-actions/events-that-trigger-workflows) is lengthy and confusing.

Questions we want to answer:
* when triggering on `push` with `branches: main` (but no explicit `tags` trigger), does the workflow trigger on tags? And does it trigger on tags which aren't on main branches? **Answer seems to be no**. See [`build-on-push`](./.github/workflows/build-on-push.yml), it didn't trigger again when [`v2026.4.1`](https://github.com/r-n-o/ci-triggers/releases/tag/v2026.4.1) was pushed. The only workflow that triggered is the workflow which triggered when the commit was first pushed to main.
* when triggering on both `push` and `tags`, but restricting branches to main: does the workflow correctly trigger for tags on main and on non-main branches?