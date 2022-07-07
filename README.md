# Package development

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