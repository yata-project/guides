# Contributing

Follows these steps to contribute to any yata project. Also keep in mind any
project-specific contribution guide specified in the project's README.

## One time

1. Fork the repo into your own GitHub account.
1. Clone the project locally. Ensure two remotes are setup:
   1. `origin` - the project's main repo.
   1. `fork` - your forked repo.

## Every change

1. Pull down the latest: `git pull origin`.
1. Checkout a new branch for your change with `git checkout -b <name>`. The
   `<name>` should be prefixed with one of ["feature", "chore", "bugfix",
   "other"]. Examples:
   1. `feature-add-logging`.
   1. `chore-cleanup-feature-gate`.
   1. `bugfix-handle-malformed-requests`.
   1. `other-do-something-interesting`.
1. Make your change. Reference the appropriate **Style Guide** for the project.
1. Add tests (optional but strongly suggested).
1. Test your change.
1. Format, vet, test, and build your changes:
   1. Go project: run `make`.
   1. Node project: run `npm run release`.
1. Push to your fork.
1. Create a pull request.
1. Get your changes merged in.
1. Checkout the `main` branch (`git checkout main`) and pull (`git pull origin`)
   down the latest.
1. Delete your new branch:
   1. Locally: `git branch -d <name>`.
   1. Remotely: `git push <fork name> --delete <name>`.
1. Update your fork: `git push <fork name>`.
