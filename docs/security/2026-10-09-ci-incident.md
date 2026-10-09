# CI incident containment — 2026-10-09

Repository: `ThreeAndTwo/solana-go`
Branch: `main`
Inspected head: `6fa7b8e502a71db35078066436462e323bb05dd1`

Actions were disabled before this cleanup. Keep them disabled until the repository owner explicitly approves restoration.

The owner confirmed that this personal repository must not contain GitHub Actions workflows. This change removes every file under `.github/workflows` on this branch, regardless of its name.

Files removed in this change:

- `.github/workflows/tests.yml` — original Git object `ec8af93c35dfb2e3016b8aeaec1afec75d57e675`.

Evidence and limits

- Unauthorized workflows were observed attempting credential or repository-history disclosure. A successful workflow run alone does not prove data receipt or credential validity.
- Existing Git history is retained as evidence. No release, tag, force push, or history rewrite is part of this cleanup.
- Revoking a GitHub token does not rotate credentials issued by other services.
- The initial credential compromise and the authentication method used for the mass write remain under investigation.
- This record supersedes any earlier note suggesting that personal-repository workflows should be retained.
