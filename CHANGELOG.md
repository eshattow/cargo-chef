# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [0.1.79](https://github.com/eshattow/cargo-chef/compare/v0.1.78...v0.1.79) - 2026-10-03

### Added

- toml v1.1 support
- Minimize recipe to increase cache hit ratio
- Publish a prebuilt cargo-chef image for every upstream rust tag. Broaden architecture support to include , and
- Support the --jobs flags.
- add --no-build to cook ([#260](https://github.com/eshattow/cargo-chef/pull/260))
- add frozen and locked ([#198](https://github.com/eshattow/cargo-chef/pull/198))
- support passing multiple `--package` arguments ([#199](https://github.com/eshattow/cargo-chef/pull/199))

### Fixed

- Remove lints from manifests in recipe.json
- clippy warnings ([#318](https://github.com/eshattow/cargo-chef/pull/318))
- Assign `CHEF_IMAGE_TAG` before it is used in `CHEF_IMAGE` env ([#306](https://github.com/eshattow/cargo-chef/pull/306))
- typo in README.md `cargo cook` should be `cargo chef cook` ([#269](https://github.com/eshattow/cargo-chef/pull/269))
- Run `cargo metadata` with no-deps flag ([#211](https://github.com/eshattow/cargo-chef/pull/211))

### Other

- release v0.1.78
- add OCI annotations
- release v0.1.77
- Mention preiter93 in the CHANGELOG for recipe minimization
- release v0.1.76
- Upgrade to latest versions of dependencies
- Use HashSet rather than Vec for contains check
- Use 'cargo metadata --no-deps' when prepare wasn't given a --bin option
- Allow cargo-chef to fetch dependencies when computing the package graph
- Don't use fetch to get tags
- release v0.1.75 ([#333](https://github.com/eshattow/cargo-chef/pull/333))
- Disable semver check. We version based on the CLI interface, not the library one
- Bump rustsec/audit-check from 1.4.1 to 2.0.0 ([#278](https://github.com/eshattow/cargo-chef/pull/278))
- Use a PAT to allow release-plz's job to trigger other workflows
- Don't pass an empty crates.io token, we're using trusted publishing
- release v0.1.74
- Only build Docker images on a schedule and on tags
- Don't build twice for PRs
- Modernize publishing pipeline
- Minimize read API calls ([#329](https://github.com/eshattow/cargo-chef/pull/329))
- Fix Docker publishing workflow ([#328](https://github.com/eshattow/cargo-chef/pull/328))
- Start testing caching behaviour with real builds ([#327](https://github.com/eshattow/cargo-chef/pull/327))
- Use latest debian stablee release, trixie.
- Release cargo-chef version 0.1.73
- add release for aarch64-unknown-linux-gnu ([#317](https://github.com/eshattow/cargo-chef/pull/317))
- Release cargo-chef version 0.1.72
- Set `RUST_IMAGE_TAG` from matrix when determining duplicate ([#311](https://github.com/eshattow/cargo-chef/pull/311))
- Release cargo-chef version 0.1.71
- Upgrade dependencies
- Release cargo-chef version 0.1.70
- Update cargo-manifest to 0.18.1. Fixes crate-type for binaries ([#292](https://github.com/eshattow/cargo-chef/pull/292))
- Release cargo-chef version 0.1.69
- Bump cargo-manifest to 0.18 ([#289](https://github.com/eshattow/cargo-chef/pull/289))
- Fix clippy lint
- Release cargo-chef version 0.1.68
- Improve support for bench/dev/test profiles ([#277](https://github.com/eshattow/cargo-chef/pull/277))
- Release cargo-chef version 0.1.67
- Update cargo-manifest to 0.14
- Update `cargo-manifest` and `toml` ([#264](https://github.com/eshattow/cargo-chef/pull/264))
- Do not mask dependencies without `path` set ([#263](https://github.com/eshattow/cargo-chef/pull/263))
- resolve clap 4 deprecated api ([#258](https://github.com/eshattow/cargo-chef/pull/258))
- Release cargo-chef version 0.1.66
- use the manifest path instead of just the member name when using `prepare --bin` ([#255](https://github.com/eshattow/cargo-chef/pull/255))
- Release cargo-chef version 0.1.65
- Replace atty crate with std::io::IsTerminal ([#257](https://github.com/eshattow/cargo-chef/pull/257))
- Release cargo-chef version 0.1.64
- Add rust-toolchain.toml to skeleton ([#254](https://github.com/eshattow/cargo-chef/pull/254))
- Add `--bins` and allow `--bin` to be called multiple times ([#241](https://github.com/eshattow/cargo-chef/pull/241))
- Do not mask workspace dependencies with a source attribute - they are transitive and not sourced from the workspace ([#247](https://github.com/eshattow/cargo-chef/pull/247))
- Release cargo-chef version 0.1.63
- remove default-members from recipe ([#253](https://github.com/eshattow/cargo-chef/pull/253))
- Update dependencies
- Update README.md
- Bump docker/login-action from 2 to 3 ([#243](https://github.com/eshattow/cargo-chef/pull/243))
- Bump docker/setup-buildx-action from 2 to 3 ([#244](https://github.com/eshattow/cargo-chef/pull/244))
- Bump docker/setup-qemu-action from 2 to 3 ([#245](https://github.com/eshattow/cargo-chef/pull/245))
- Bump actions/checkout from 3 to 4 ([#240](https://github.com/eshattow/cargo-chef/pull/240))
- (cargo-release) version 0.1.62
- Best practies for github actions: permissions and dependabot ([#223](https://github.com/eshattow/cargo-chef/pull/223))
- Solve CI warnings replacing outdated actions ([#221](https://github.com/eshattow/cargo-chef/pull/221))
- (cargo-release) version 0.1.61
- Use `cargo metadata` to resolve targets ([#214](https://github.com/eshattow/cargo-chef/pull/214))
- (cargo-release) version 0.1.60
- Update cargo-manifest to pick up 'strip' configuration
- fix example to use recommended absolute paths for `WORKDIR` ([#170](https://github.com/eshattow/cargo-chef/pull/170))
- (cargo-release) version 0.1.59
- (cargo-release) version 0.1.58
- Masking should take into account package renames. ([#209](https://github.com/eshattow/cargo-chef/pull/209))
- (cargo-release) version 0.1.57
- We should keep all manifests, even if they are not mentioned in the list of workspace members ([#207](https://github.com/eshattow/cargo-chef/pull/207))
- (cargo-release) version 0.1.56
- Use `cargo metadata` to find workspace manifests ([#204](https://github.com/eshattow/cargo-chef/pull/204))
- (cargo-release) version 0.1.55
- Build linux-gnu binaries on ubuntu 20.04 ([#202](https://github.com/eshattow/cargo-chef/pull/202))
- Update README.md
- (cargo-release) version 0.1.54
- Upgrade all dependencies to their latest version. ([#200](https://github.com/eshattow/cargo-chef/pull/200))
- (cargo-release) version 0.1.53
- rm duplicate cargo ([#197](https://github.com/eshattow/cargo-chef/pull/197))
- (cargo-release) version 0.1.52
- add all-features as a flag ([#1](https://github.com/eshattow/cargo-chef/pull/1)) ([#196](https://github.com/eshattow/cargo-chef/pull/196))
- Use sparse protocol to speed up builds ([#193](https://github.com/eshattow/cargo-chef/pull/193))
- Fix failing builds (again) ([#190](https://github.com/eshattow/cargo-chef/pull/190))
- (cargo-release) version 0.1.51
- Fix linter error
- Support for custom target files ([#178](https://github.com/eshattow/cargo-chef/pull/178))
- (cargo-release) version 0.1.50
- Update lockfile
- Update cargo-manifest to add support for `cargo-features` in Cargo.toml. Closes #173
- Update lock file
- Fix erroneous version bump

## [0.1.78](https://github.com/LukeMathWalker/cargo-chef/compare/v0.1.77...v0.1.78) - 2026-04-13

### Added

- toml v1.1 support

### Other

- add OCI annotations

## [0.1.77](https://github.com/LukeMathWalker/cargo-chef/compare/v0.1.76...v0.1.77) - 2026-03-03

### Fixed

- Remove lints from manifests in recipe.json

## [0.1.76](https://github.com/LukeMathWalker/cargo-chef/compare/v0.1.75...v0.1.76) - 2026-03-03

### Added

- Minimize generated recipe to increase cache hit ratio when `cargo chef prepare` is invoked with a `--bin` option (by [@preiter93](https://github.com/preiter93))
- Publish a prebuilt `cargo-chef` Docker image for every upstream Rust tag. 
- Broaden the set of supported architectures for Docker images to include `i386` and `arm32v7`

### Other

- Upgrade to latest versions of all dependencies
- Allow cargo-chef to fetch dependencies in `cargo chef prepare`, if either `--bin` was specified or
  the lockfile is missing.

## [0.1.75](https://github.com/LukeMathWalker/cargo-chef/compare/v0.1.74...v0.1.75) - 2026-02-28

### Added

- Support the --jobs flags.

### Other

- Disable semver check. We version based on the CLI interface, not the library one
- Bump rustsec/audit-check from 1.4.1 to 2.0.0 ([#278](https://github.com/LukeMathWalker/cargo-chef/pull/278))
- Use a PAT to allow release-plz's job to trigger other workflows

## [0.1.74](https://github.com/LukeMathWalker/cargo-chef/compare/v0.1.73...v0.1.74) - 2026-02-27

### Other

- Fix Docker publishing workflow ([#328](https://github.com/LukeMathWalker/cargo-chef/pull/328))
- Start testing caching behaviour with real builds ([#327](https://github.com/LukeMathWalker/cargo-chef/pull/327))
