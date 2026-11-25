# awl

Roslyn semantic analysis for coding agents. This repository holds release archives of the awl Claude Code plugin; install it from the [toolchest](https://github.com/futurenanigans/toolchest) marketplace:

```
/plugin marketplace add futurenanigans/toolchest
/plugin install awl@toolchest
```

Alpha builds. The plugin carries awl as a framework-dependent `awl.dll` under `bin/` and runs it with `dotnet`, so the only prerequisite is the .NET 10 runtime (or SDK) on PATH. Nothing is installed globally.

Each release lists the SHA-256 of its archive in `SHA256SUMS`; the toolchest entry pins the same hash, and Claude Code refuses an archive that does not match.

A repository opts in with `.awl/awl.json` at its root; the `awl-enable` skill sets it up.
