# Dependabot.yml Capabilities

Capabilities surfaced by the `dependabot.yml` configuration format for managing automated dependency updates on GitHub.

## Configuration Capabilities

- **Schema versioning** via the `version: 2` declaration.
- **Multi-ecosystem coverage** for 20+ package managers (npm, pip, bundler, cargo, docker, gradle, maven, terraform, github-actions, and more).
- **Multi-directory targeting** through `directory` or `directories` for monorepos.
- **Private registry authentication** via the top-level `registries` block.
- **Beta ecosystem opt-in** via `enable-beta-ecosystems`.

## Scheduling Capabilities

- **Interval scheduling**: `daily`, `weekly`, `monthly`, `quarterly`, `semiannually`, `yearly`.
- **Cron scheduling** for fine-grained timing windows.
- **Day, time, and timezone** controls for predictable PR delivery.

## Pull Request Capabilities

- **Volume limits** via `open-pull-requests-limit`.
- **Reviewer and assignee routing**.
- **Label and milestone tagging**.
- **Branch naming conventions** via `pull-request-branch-name.separator`.
- **Commit message customization** with `prefix`, `prefix-development`, and scope inclusion.
- **Rebase strategy** selection.
- **Target branch override** for non-default branches.

## Dependency Selection Capabilities

- **Allow lists** by `dependency-name` or `dependency-type`.
- **Ignore lists** by `dependency-name`, `versions`, or `update-types`.
- **Versioning strategy** controls (`auto`, `increase`, `increase-if-necessary`, `lockfile-only`, `widen`).
- **Vendor directory** handling.
- **Insecure external code execution** opt-in/opt-out.

## Update Grouping Capabilities

- **Named groups** that bundle related dependencies into a single PR.
- **Group scoping** by `applies-to` (`version-updates` or `security-updates`).
- **Pattern matching** with `patterns` and `exclude-patterns`.
- **Update-type filtering** for `major`, `minor`, and `patch` updates.

## Cooldown Capabilities

- **Default cooldown** via `default-days`.
- **Severity-aware cooldowns** through `semver-major-days`, `semver-minor-days`, and `semver-patch-days`.
- **Per-dependency cooldown scoping** via `include` and `exclude` lists.
