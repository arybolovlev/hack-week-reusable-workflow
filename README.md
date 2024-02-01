# hack-week-reusable-workflow

```console
act workflow_call \
  --input kindVersion=0.20.0 \
  --input terraformVersion=1.7.1 \
  --container-architecture linux/arm64 \
  -P linux=catthehacker/ubuntu:act-latest \
  -W .github/workflows/acceptance_tests_kind.yaml


act workflow_dispatch \
  --input kindVersion=0.20.0 \
  --input terraformVersion=1.7.1 \
  --container-architecture linux/arm64 \
  -P linux=catthehacker/ubuntu:act-latest \
  -W .github/workflows/acceptance_tests_kind.yaml

act pull_request \
  --var KIND_VERSION=0.20.0 \
  --var TERRAFORM_VERSION=1.7.1 \
  --container-architecture linux/arm64 \
  -P linux=catthehacker/ubuntu:act-latest \
  -W .github/workflows/acceptance_tests_kind.yaml

act schedule \
  --var KIND_VERSION=0.20.0 \
  --var TERRAFORM_VERSION=1.7.1 \
  --container-architecture linux/arm64 \
  -P linux=catthehacker/ubuntu:act-latest \
  -W .github/workflows/acceptance_tests_nightly.yaml
```
