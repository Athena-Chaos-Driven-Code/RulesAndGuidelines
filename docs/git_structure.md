# Git Repo Structure:
## Branch names
The master branch of the repository is always named : `core`
Branch names should not include a version number, as this will result in the branch being cluttered with multiple features. This would become messy to understand what the branch is about. Branch names should include a name of the feature or fix (or collection of fixes) that is being worked on.

## Commit Messages and notes
Commit messages should follow a strict format, to ease looking up certain changes to the code and keep a consistent track record.
Different changes, should be reflected in different commits, meaning that a single git commit should, for example, not contain multiple feature additions.

### Git commit message format:
| Subject                                                             | Git Title          |
| ------------------------------------------------------------------- | ------------------ |
| Feature addition                                                    | `Feat: ...`       |
| Documentation                                                       | `Docs: ...`       |
| Bug fix                                                             | `Fix: ...`        |
| Neither a fix or a feature addition, but a rework of a given system | `Refactor: ...`   |
| Performance improvements                                            | `Perfomance: ...` |
| Version Bump                                                        | `Bump: ...`       |
| Update to the .gitignore file                                       | `GitIgnore: ...`  |

### Git commit note format:
Notes are to be used to give more relevant information about the commit

Notes are also used for twitch redeemable on Andreas's Twitch account. The following formats are to be used:
- Twitch redeemable for "*make Andreas save and/or commit*":
```
This commit was made possible by: ...
```

- Twitch redeemable for "*make Andreas save and/or commit, with custom message*":
```
This commit was made possible by: ...
With the following message : "..."
```
