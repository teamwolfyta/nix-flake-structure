# Nix Flake Structure

## Directory Structure

### Apps

```
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

### Configurations

```
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

### Derivations

```
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

### Modules

```
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

### Templates

```
# Flake output: templates.{name}
templates
  ├─ templates.nix
  └─ {name}
```
