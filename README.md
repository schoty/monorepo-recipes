# Schoty - monorepo recipes

Submit a PR here to create a new monorepo out of existing Github repositories.

**Warning:** this project is still in an early development phase. We welcome any feedback and contributions, see,
 - https://github.com/schoty/monorepo-recipes/issues
 - https://github.com/schoty/schoty-builder


## PR submission procedure

 See the PR submission guidelines in [PULL_REQUEST_TEMPLATE.md](./PULL_REQUEST_TEMPLATE.md).


## How does it work

Once a PR with a new monorepo submission is merged in this repository, the following would happen,

1. All the repositories specified in the PR are forked by [@schoty-agent](https://github.com/schoty-agent)

2. A monorepo containing the specified repositories is created under `schoty/<name>-monorepo`. The git history of individual repos is not preserved, the monorepo is created with a single commit containing all of the code. Large files are also not included.

It is possible to make PR to the monorepo, which if accepted, would,

1. Create patches with the code modifications for each individual repository

2. Apply these patches and commit modifications to individual forks

3. Make PRs from individual forks by [@schoty-agent](https://github.com/schoty-agent) on behalf of the original contributor.

![schoty-infra](https://cloud.githubusercontent.com/assets/630936/24074069/25d5a306-0c02-11e7-9d81-9ce008676dc8.png)


## Excluding a repository

If you want to exclude a repository from contributions originated from the Schoty project, please add the repository name to [`excluded_repos.yml`](./excluded_repos.yml).


## Conditions of use

1. For now, the monorepos are limited to 500 included repositories


