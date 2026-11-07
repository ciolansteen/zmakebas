# Maintained downstream

Upstream is https://github.com/z00m128/zmakebas. Its branches and tags remain
unchanged in the pristine pull mirror:
https://git.ciolan.net/github-mirrors/zmakebas

Development happens on branch `iAdrian` in the canonical working repository:
https://git.ciolan.net/iAdrian/zmakebas

A native push mirror copies the canonical branches and tags to the real GitHub
fork https://github.com/ciolansteen/zmakebas. GitHub Actions are disabled there;
the Gitea source-dispatch workflow triggers the maintained Arch package:
https://git.ciolan.net/archRepo/zmakebas-git

The package follows `iAdrian`, not upstream `master`. Verified downstream fixes
can therefore ship independently of upstream acceptance. There are no program
behavior changes in the initial downstream setup, only this note and CI wiring.

For an upstream contribution, fetch the pristine upstream and create a focused
feature branch based on its current default branch. Keep downstream CI and this
note out of the PR. Push the feature branch to canonical Gitea; after native
mirror synchronization it is available in the GitHub fork for an explicit PR.
A Git mirror does not open or copy pull requests. Reconcile accepted changes
only after the upstream merge and subsequent package verification.
