# Hermes Profile Examples Gallery

Browse complete, ready-to-use Hermes profile distributions. Each example includes
a params file, generated profile files, and a README with install and validation commands.

You can validate any example by running `python3 scripts/validate_profile.py examples/<example-name>`
from the repository root.

---

## security-reviewer

**Use case:** Reviews code, architecture, and API surface for security vulnerabilities.

**Install command:**
```bash
hermes profile install github.com/YOUR_ORG/hermes-profile-template --name security-reviewer-local --subdir examples/security-reviewer --alias
security-reviewer chat
```

**Validation command:**
```bash
python3 scripts/validate_profile.py examples/security-reviewer
```

**Why this profile exists:** Security review is a recurring task that benefits from consistent methodology. This profile flags common vulnerability patterns (SQLi, XSS, auth bypass, secret exposure), reviews architecture for attack surface, and generates actionable remediation checklists — without requiring a human pentester for every code review.

---

## database-migration-reviewer

**Use case:** Inspects SQL diffs, flags destructive migrations, and generates rollback checklists.

**Install command:**
```bash
hermes profile install github.com/YOUR_ORG/hermes-profile-template --name db-migration-reviewer-local --subdir examples/database-migration-reviewer --alias
db-migration-reviewer chat
```

**Validation command:**
```bash
python3 scripts/validate_profile.py examples/database-migration-reviewer
```

**Why this profile exists:** Database migrations are high-risk operations where a single mistake can cause data loss. This profile reviews migration SQL diffs for destructive patterns (DROP, TRUNCATE, column type changes, index changes on large tables), validates forward/backward compatibility, and produces rollback checklists before any migration runs in production.

---

## release-manager

**Use case:** Automates release versioning, changelog generation, and release readiness checks.

**Install command:**
```bash
hermes profile install github.com/YOUR_ORG/hermes-profile-template --name release-manager-local --subdir examples/release-manager --alias
release-manager chat
```

**Validation command:**
```bash
python3 scripts/validate_profile.py examples/release-manager
```

**Why this profile exists:** Release management is tedious but critical. This profile handles semantic versioning, generates structured changelogs from git history, validates release artifacts, and ensures release discipline (version bumps, changelog entries, release notes) before any tag goes live. It reduces the cognitive load on maintainers who would otherwise track these steps manually.

---

## research-assistant

**Use case:** Conducts literature reviews, synthesizes evidence, and produces structured research briefs.

**Install command:**
```bash
hermes profile install github.com/YOUR_ORG/hermes-profile-template --name research-assistant-local --subdir examples/research-assistant --alias
research-assistant chat
```

**Validation command:**
```bash
python3 scripts/validate_profile.py examples/research-assistant
```

**Why this profile exists:** Research tasks require systematic source evaluation, evidence synthesis, and clear uncertainty communication. This profile structures literature reviews, tracks claims to sources, flags speculative statements, and produces durable research briefs with citations — useful for competitive analysis, technical deep-dives, and decision memos.
