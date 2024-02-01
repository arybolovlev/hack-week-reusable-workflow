# hack-week-reusable-workflow

```console
act schedule \
  --var KIND_VERSION=0.20.0 \
  --var TERRAFORM_VERSION=1.7.1 \
  --container-architecture linux/arm64 \
  -P linux=catthehacker/ubuntu:act-latest \
  -W .github/workflows/acceptance_tests_nightly.yaml
```
