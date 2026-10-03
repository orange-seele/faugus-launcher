# Faugus
This is a Nix Flake for Faugus [Launcher](https://github.com/Faugus/faugus-launcher).
For the project's features, usage, and general documentation, please refer to the upstream project.

# Installation
### Run directly
```
nix run github:Faugus/faugus-launcher
```
### Install
Add the following to your NixOS flake.nix:
```
inputs.faugus-launcher.url = "github:Faugus/faugus-launcher";
```
Then add the package to environment.systemPackages:
```
environment.systemPackages = [
  inputs.faugus-launcher.packages."${pkgs.stdenv.hostPlatform.system}".default
];
```

