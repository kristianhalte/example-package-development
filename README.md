# Example: Package development

[![Conventional Commits](https://img.shields.io/badge/Conventional%20Commits-1.0.0-%23FE5196?logo=conventionalcommits&logoColor=white)](https://conventionalcommits.org)

## Getting Started: Semantic Versioning
Website: https://semver.org/

NPM Commands: https://docs.npmjs.com/cli/v8/commands/npm-version


- [x] initiate the npm package with `npm init -y`
- [x] bump pre-patch version with `npm version prepatch`
- [x] bump patch version with `npm version patch`
- [x] bump pre-minor version with `npm version preminor`
- [x] bump minor version with `npm version minor`
- [x] bump pre-major version with `npm version premajor`
- [x] bump major version with `npm version major`
- [x] manually bump version with `npm version x.x.x-x`
- [x] bump pre-release version with `npm version prerelease`

#### Learnings
- `npm version` creates a commit
- `major`: major change + breaks the API
- `minor`: minor changes + does not break the API
- `patch`: bug fixes
- `[major].[minor].[patch]`
    - `premajor`: `[major]-[premajor].[minor].[patch]`
    - `preminor`: `[major].[minor]-[preminor].[patch]`
    - `prepatch`: `[major].[minor].[patch]-[prepatch]`
    - `prerelease`: `[major].[minor].[patch]-[prerelease]`

## Getting Started: Conventional Commits
Website: https://www.conventionalcommits.org/en/v1.0.0/

conventional-changelog-action: https://github.com/TriPSs/conventional-changelog-action

create-release: https://github.com/actions/create-release

Use the `math.js` file as a math library

- [x] add the `addition()` function and do a regular commit
- [x] add the `subtraction()` function and do a `feat` commit
- [x] add the `multiplication()` function and do a `feat` commit
- [x] install the `standard-version` package
- [x] update the `README.md` and do a `doc` commit
- [x] run the `npm run release` command
- [x] raise issue for the `multiplication()` function in the github UI
- [x] update the `multiplication()` function and do a `fix` commit
- [x] add the `division()` function and do a `feat` commit
- [x] run the `npm run release` command
- [x] run the `git push --follow-tags origin master` command to see tags in github UI
- [x] raise issue for the `multiplication()` and `division()` functions in the github UI
- [x] update the `multiplication()` and `division()` functions and do a `fix` commit
- [x] run the `npm run release` command
- [x] add the `triplication()` function and do a `feat` commit
- [x] update the `triplication()` function and do a `fix` commit
- [x] add the conventional-changelog-action workflow to `.github/workflows/conventional-changelog.yml` file and do a `chore` commit
- [x] add the `quadruplication()` function and do a `feat` commit
- [x] update the `quadruplication()` function and do a `fix` commit
- [x] add the create-release workflow to `.github/workflows/release.yml` file and do a `chore` commit

#### Learnings
- using conventional commits as a standard is good practice, even if you won't be making changelogs, automated workflows etc.
- conventional commits can be done manually (no requirements or dependencies needed) or with a VS Code extension
- it's good to start out with `fix`, `doc`, `feat` and `chore`
- you can use husky to force commit conventions
- once cenventional commits are being used for each commit, you can use packages like `standard-version` to generate `CHANGELOG.md` and bump package version
- you can also use the `conventional-changelog-action` workflow to automate this, based on code pushes (just don't do both)
- `fix` should bump `[patch]` version
- `feat` should bump `[minor]` version
- you can configure which conventional commit types will be included in the `CHANGELOG.md` https://github.com/conventional-changelog/conventional-changelog-config-spec/blob/master/versions/2.2.0/README.md
    ```json
    "types": [
        {"type": "feat", "section": "Features"},
        {"type": "fix", "section": "Bug Fixes"},
        {"type": "chore", "hidden": true},
        {"type": "docs", "hidden": true},
        {"type": "style", "hidden": true},
        {"type": "refactor", "hidden": true},
        {"type": "perf", "hidden": true},
        {"type": "test", "hidden": true}
    ]
    ```
