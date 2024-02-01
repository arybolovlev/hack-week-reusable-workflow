# hack-week-reusable-workflow

```console
act pull_request \
  --var TERRAFORM_VERSION=1.7.1 \
  --var KIND_VERSION=0.20.0 \
  --container-architecture linux/arm64 \
  -P linux=catthehacker/ubuntu:act-latest \
  -W .github/workflows/acceptance_tests_kind.yaml

act workflow_dispatch \
  --input terraformVersion=1.7.1 \
  --input kindVersion=0.20.0 \
  --container-architecture linux/arm64 \
  -P linux=catthehacker/ubuntu:act-latest \
  -W .github/workflows/acceptance_tests_kind.yaml


act schedule \
  --var TERRAFORM_VERSION=1.7.1 \
  --container-architecture linux/arm64 \
  -P linux=catthehacker/ubuntu:act-latest \
  -W .github/workflows/acceptance_tests_eks.yaml

act schedule \
  --var TERRAFORM_VERSION=1.7.1 \
  --container-architecture linux/arm64 \
  -P linux=catthehacker/ubuntu:act-latest \
  -W .github/workflows/acceptance_tests_gke.yaml
```
