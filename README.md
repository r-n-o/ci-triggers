# ci-triggers

Simple project to test Github CI triggers.

The [documentation](https://docs.github.com/en/actions/reference/workflows-and-actions/events-that-trigger-workflows) is lengthy and confusing.

Questions we want to answer:
* when triggering on `push` with `branches: main` (but no explicit `tags` trigger), does the workflow trigger on tags? And does it trigger on tags which aren't on main branches?