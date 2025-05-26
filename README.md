# Nix Flake Structure

## Directory Structure

### Apps

```
app.nix

apps
  ├─ {name}.nix
  └─ {name}
    └─ default.nix
```

### Configurations

```
configuration
  ├─ {darwin|hjem|home|nixos|system}.nix
  └─ {darwin|hjem|home|nixos|system}
    └─ default.nix

configurations
  └─ {darwin|hjem|home|nixos|system}
    ├─ {name}.nix
    └─ {name}
      └─ default.nix
```

### Derivations

```
{check|legacyPackage|package|shell}.nix 

{checks|legacyPackages|packages|shell}
  ├─ {name}.nix
  └─ {name}
    └─ default.nix
```

### Modules

```
module
  ├─ {darwin|flake|hjem|home|nixos|system}.nix
  └─ {darwin|flake|hjem|home|nixos|system}
    └─ default.nix

modules
  └─ {darwin|flake|hjem|home|nixos|system}
    ├─ {name}.nix
    └─ {name}
      └─ default.nix
```

### Templates

```
templates
  ├─ templates.nix
  └─ {name}
```
