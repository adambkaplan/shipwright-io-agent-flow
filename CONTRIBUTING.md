# Contributing to Shipwright Agent Flow

Thank you for your interest in contributing to the Shipwright Agent Flow repository. This project
coordinates AI-assisted, cross-repository feature development across the Shipwright ecosystem by
providing skills and workflows for multi-repo agentic actions.

## Code of Conduct

All contributors are expected to adhere to the
[Shipwright Code of Conduct](https://github.com/shipwright-io/.github/blob/main/CODE_OF_CONDUCT.md).
By participating in this project, you agree to abide by its terms. Please report unacceptable
behavior to the project maintainers.

## Getting Started

1. **Fork** the repository on GitHub.
2. **Clone** your fork with submodules:
   ```bash
   git clone --recurse-submodules https://github.com/<your-username>/agent-flow.git
   cd agent-flow
   ```
3. **Create a feature branch** from `main`:
   ```bash
   git checkout -b my-feature
   ```
4. Make your changes, commit them (see below), and push to your fork.
5. Open a **pull request** against the `main` branch of this repository.

## Commit Messages

Well-formed commit messages make the project history easy to navigate and enable automated
changelog generation.

### Format

```
<type>(<scope>): <short summary>

[optional body]

[optional footers]
Signed-off-by: Your Name <your@email.com>
```

#### Subject line

- Keep the subject line at or under 50 characters
- Use the imperative mood: "add skill" not "added skill" or "adds skill"
- Do not end the subject line with a period

[Conventional commits](https://www.conventionalcommits.org/en/v1.0.0/#summary) or similar commit
message formats are encouraged, but not required.

#### Body

- Wrap at 72 characters
- Explain *what* changed and *why*, not *how* 

#### Developer Certificate of Origin (DCO)

All commits **must** include a `Signed-off-by` trailer that certifies you wrote or have the right
to submit the contribution under the project's [Apache 2.0 License](LICENSE). This is the
[Developer Certificate of Origin (DCO)](https://developercertificate.org/).

Add the sign-off automatically with the `-s` flag:

```bash
git commit -s -m "feat(skills): add cross-repo PR creation skill"
```

Or set it as the default by adding to your global Git config:

```bash
git config --global format.signOff true
```

Pull requests that contain unsigned commits will not be merged until all commits carry a
`Signed-off-by` line matching the author's name and email.

### Examples

#### Good

```
feat(skills): add cross-repo PR creation skill

Introduces a skill that opens coordinated pull requests across multiple
Shipwright submodule repositories in a single agent invocation.

Signed-off-by: Ada Lovelace <ada@example.com>
```

- Has a title less than 50 characters
- Includes a message body that explains _what_ changed, and _why_.

#### Bad

```
fix(workflows): correct submodule update order in setup-plan script

Signed-off-by: Ada Lovelace <ada@example.com>
```

- Subject line is too long
- Missing message body that explains _why_ the change was made.

```
Clarify submodule initialization steps in README

```

- Missing message body that explains _why_ the change was made.
- Missing DCO sign-off


## Pull Request Guidelines

- **One logical change per PR.** Split unrelated changes into separate pull requests.
- **Reference related issues** in the PR description (e.g., `Closes #42`).
- **Keep the diff focused.** Avoid unrelated formatting or whitespace changes.
- **Update documentation** if your change affects usage or behavior described in the README or
  other docs.
- **Rebase onto `main`** before requesting review to keep history linear:
  ```bash
  git fetch origin
  git rebase origin/main
  ```
- **Ensure all commits are signed off** before opening or updating your PR.

### PR Description Template

```
## Summary

<!-- What does this PR change and why? -->

## Related Issues

<!-- Closes #<issue-number> -->

## Testing

<!-- How was this change tested? -->
```

## Contribution Scope

This repository contains:

- **Skills** — reusable agent actions for cross-repository operations (`.claude/`, `.specify/`)
- **Workflows** — orchestration sequences that compose skills into end-to-end feature flows
- **Submodule configuration** — pointers to Shipwright project repositories under `repos/`

Contributions to the individual Shipwright projects (`build`, `cli`, `operator`, etc.) should be
submitted to those repositories directly. Changes to submodule pointers in this repository should
accompany a corresponding merged upstream commit.

## Getting Help

Open a [GitHub Issue](https://github.com/shipwright-io/agent-flow/issues) for bugs, feature
requests, or questions. For broader Shipwright community discussion, see the
[community repository](https://github.com/shipwright-io/community).
