# Bifrost Ops — ACI Fabric

Day 0 Cisco ACI fabric/access configuration using declarative YAML and Cisco Network as Code (NAC) Terraform modules.

## Status
Documentation-first scaffold; **not deployment-ready**. No controller credentials or fabric-specific topology are configured.

## Planned structure
- `config/`: documented environment YAML
- `terraform/`: pinned NAC module integration and providers
- `docs/`: prerequisites, plan/apply, rollback, recovery, validation

## Safety contract
1. Read [the central runbooks](https://github.com/Bifrost-Ops/docs).
2. Inventory existing ACI objects before introducing management by Terraform.
3. Confirm module/provider versions and compatibility with the target APIC.
4. Run formatting, validation and a reviewed plan.
5. Apply only through an explicitly approved deployment workflow.
6. Reverting a Git commit is **not** automatically a safe fabric rollback; inspect the resulting plan for deletes/replacements.

## Boundaries
Fabric Day 0 ownership must be distinct from tenant Day 1 ownership to avoid conflicting Terraform state.
