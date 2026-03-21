# fakey

**Status: scaffold only. No source code exists yet.**

`fakey` is a nascent project under the [portal-co](https://github.com/portal-co) GitHub organization (package name `@portal-solutions/fakey`). The description in both `Cargo.toml` and `package.json` reads "Fake keyboards for compliant encryption", but no implementation exists as of the initial commit.

## Repository structure

```
fakey/
├── Cargo.toml       # Virtual Cargo workspace (resolver = "3", no members)
├── package.json     # npm workspace (no members)
├── crates/          # Empty; placeholder file only
├── packages/        # Empty; placeholder file only
└── README.md
```

The repository has a single commit ("Initial scaffold"). Both workspace manifests declare empty member lists:

- `Cargo.toml` — virtual workspace with `resolver = "3"` and `[workspace.package]` metadata but no crate members. Cargo refuses to build it: `"The manifest is virtual, and the workspace has no members."`
- `package.json` — ESM package (`"type": "module"`) with a single dev-dependency on `zshy ^0.7.0` and an empty `workspaces` array.

## What is not here

- No Rust source files (`crates/` contains only a git-tracking placeholder).
- No JavaScript/TypeScript packages (`packages/` contains only a git-tracking placeholder).
- No library API, no binary, no tests, no build scripts.

## Development environment (observed)

The `target/.rustc_info.json` indicates the developer's toolchain at the time of scaffolding:

- **Rust**: 1.93.1 (stable, `aarch64-apple-darwin`, LLVM 21.1.8)
- **Host**: macOS, Apple Silicon (aarch64)

## Remote

```
git@github.com:portal-co/fakey.git
```
