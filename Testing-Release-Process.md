## Testing
- Push a commit or #PR to the default branch to trigger the Github actions Test Workflows.

## kitura-cli Release Process

The following instructions are for releasing a new version of kitura-cli:

- Tag the release using the format `*.*.*` e.g. `1.0.3`, which will trigger a build.
  - Github actions `build_release` workflow will then execute `build-release.sh <TAG>`, building and packaging the binaries.
  - Artifacts containing the `kitura-cli_0.0.17_amd64.deb`, `kitura-cli_0.0.17_darwin.tar.gz` and `kitura.rb` files will be generated. This can be then downloaded and added to the release.

### Updating homebrew

- Clone https://github.com/Kitura-Next/homebrew-kitura and create a new branch.
- Replace the `kitura.rb` file with the one that is attached to the release.
- Push your changes, then raise and merge the PR.
- Update your version of the cli by running `brew upgrade kitura` and do a final check to make sure your updates are running as expected.
