# Nix Flake Structure

## Apps

```shell
# Flake output: apps.default
app.nix
app
  └─ default.nix

# Flake output: apps.{name}
apps
  ├─ {name}.nix
  └─ {name}
    └─ default.nix
```

## Clusters

```shell
clutsers
  └─ {cluster-name}
    ├─ default.nix
    ├─ configurations # Same as #Configurations.
    └─ modules # Same as #Modules.
```

## Configurations

> "type": `darwinConfigurations`, `homeConfigurations`, `nixosConfigurations` or `systemConfigs`.

<sub>System-Manager, why deviate from the pattern? 😢 </sub> 

```shell
# Flake output: {type}.default
configuration
  ├─ {darwin|home|nixos|system}.nix
  └─ {darwin|home|nixos|system}
    └─ default.nix

# Flake output: {type}.{name}
configurations
  └─ {darwin|home|nixos|system}
    ├─ {name}.nix
    └─ {name}
      └─ default.nix
```

## Derivations

```shell
# Flake output: {type}.default
{check|legacyPackage|package|shell}.nix 
{check|legacyPackage|package|shell}
  └─ default.nix

# Flake output: {type}.{name}
{checks|legacyPackages|packages|shell}
  ├─ {name}.nix
  └─ {name}
    └─ default.nix
```

## Modules

> "type": `darwinModules`, `flakeModules`, `hjemModules`, `homeModules`, `nixosModules` or `systemModules`.

```shell
# Flake output: {type}.default
module
  ├─ {darwin|flake|hjem|home|nixos|system}.nix
  └─ {darwin|flake|hjem|home|nixos|system}
    └─ default.nix

# Flake output: {type}.{name}
modules
  └─ {darwin|flake|hjem|home|nixos|system}
    ├─ {name}.nix
    └─ {name}
      └─ default.nix
```

## Templates

```shell
# Flake output: templates.{name}
templates
  ├─ templates.nix
  └─ {name}
```
