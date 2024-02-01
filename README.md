# hack-week-reusable-workflow

```console
act pull_request \
  --container-architecture linux/arm64 \
  -P linux=catthehacker/ubuntu:act-latest \
  -W .github/workflows/acceptance_tests_kind.yaml
```
