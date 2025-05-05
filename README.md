# Hummanta Registry

**Hummanta Registry** is the central index repository of the Hummanta compiler ecosystem. It maintains the manifest URL list for all language frontends, backends, and project detectors.

It serves as a unified entry point for the `hummanta` CLI to discover toolchains, enabling automatic download and installation of compiler components across multiple languages, platforms, and target architectures.

## Directory Structure

### `toolchains/`

Contains configuration files for different programming languages supported by Hummanta.

- `solidity.toml`: Toolchain configuration for Solidity.
- `toy.toml`: Toolchain configuration for Toy.

For more information on the toolchain concept, please refer to the [toolchain documentation](https://hummanta.github.io/docs/concepts/toolchain.html).

### `targets/`

Contains configuration files for different virtual machine targets supported by Hummanta.

- `native.toml`: Configuration for the native machine code (e.g., x86, RISC-V, ARM64).

For more information on the target concept, please refer to the [target documentation](https://hummanta.github.io/docs/concepts/target.html).

## Usage

### Adding a New Toolchain

1. Create a new `.toml` file for the toolchain inside the `toolchains/` folder.
2. Add the necessary configuration details for the toolchain, including package names, binaries, and other relevant information.
3. Update the `index.toml` file to include the new toolchain.

### Adding a New Target

1. Update the appropriate `.toml` file inside the `targets/` folder (e.g., `evm.toml`, `move-vm.toml`, etc.).
2. Specify the relevant platform information, such as the URL for downloading the package, hash, and any platform-specific details.
