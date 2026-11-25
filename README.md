# awl

Roslyn semantic analysis for coding agents, as a .NET global tool. This repository holds release packages only; the Claude Code plugin is in the [toolchest](https://github.com/futurenanigans/toolchest) marketplace.

Alpha builds. Requires the .NET 10 SDK and the [GitHub CLI](https://cli.github.com/).

Install or update to the latest release:

```sh
gh release download -R futurenanigans/awl-dist -p '*.nupkg' -D ~/.awl-feed --clobber
dotnet tool update -g Awl --add-source ~/.awl-feed --prerelease
```

`dotnet tool update` installs when awl is missing. On linux-x64 it picks the native build; elsewhere the portable build, which runs on the dotnet runtime. Each release lists the SHA-256 of its packages in `SHA256SUMS`.

Then add the plugin in Claude Code:

```
/plugin marketplace add futurenanigans/toolchest
/plugin install awl@toolchest
```

A repository opts in with `.awl/awl.json` at its root; the `awl-enable` skill sets it up.
