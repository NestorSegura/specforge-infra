# specforge-infra

Terraform for the SpecForge platform on Azure. Platform infrastructure only: application workloads are deployed from [specforge-gitops](https://github.com/NestorSegura/specforge-gitops) by Argo CD.

## Layout

```
bootstrap/   # local state, applied once: creates the remote state storage
envs/dev/    # dev environment, remote state in Azure Storage (Entra ID auth)
modules/     # reusable, versioned modules
docs/adr/    # architecture decision records
```

## Usage

```sh
az login
cd envs/dev
terraform init
terraform plan
```

Decisions are documented in [docs/adr](docs/adr).
