# Websocat

Websocat is a command-line WebSocket client and server. This repository contains pre-built releases of websocat compiled for Linux environments.

## Features

✅ Built inside Ubuntu 22.04 runner  
✅ Includes WebSocket client/server features  
✅ Compatible with most modern Linux distributions  
✅ Easy-to-install binary distribution

## Installation

### Prerequisites

- Linux system (compatible with Ubuntu 22.04 and similar distributions)
- `wget` or `curl` to download the release
- `tar` to extract the archive
- `sudo` access to install to `/usr/local/bin`

### Installation Steps

Follow these commands to install websocat:

```bash
# Download the release
wget https://github.com/xiongli870110-hue/Websocat/releases/download/websocat-1.13.0/websocat-build.tar.gz

# Extract the archive
tar -xzf websocat-build.tar.gz

# Copy the binary to system PATH
sudo cp output/websocat /usr/local/bin/websocat

# Make the binary executable
sudo chmod +x /usr/local/bin/websocat

# Verify the installation
websocat --version
```

## Build Information

### Version
- **Version**: 1.13.0
- **Base OS**: Ubuntu 22.04
- **Build Date**: See release page for details

### Build Environment

The build process includes:

1. **System Dependencies**
   - `build-essential` - Essential build tools
   - `curl` and `git` - For downloading source and version control
   - `pkg-config` - For library configuration
   - `libssl-dev` - OpenSSL development files
   - `rustc` and `cargo` - Rust compiler and package manager

2. **Build Process**
   - Clones the original websocat repository from https://github.com/vi/websocat.git
   - Compiles with `cargo build --release`
   - Packages the binary into a distributable tarball

3. **Output**
   - Pre-built binary optimized for release
   - Ready-to-use executable with no compilation required on target systems

## Usage

Once installed, you can use websocat from any terminal:

```bash
# Check version
websocat --version

# Use as WebSocket client/server as needed
websocat [OPTIONS] [ARGUMENTS]
```

## Troubleshooting

### Permission Denied Error
If you get a "Permission denied" error when running websocat, ensure it has executable permissions:
```bash
sudo chmod +x /usr/local/bin/websocat
```

### Download Failures
If the download fails, verify:
- Your internet connection
- The release still exists at: https://github.com/xiongli870110-hue/Websocat/releases/download/websocat-1.13.0/websocat-build.tar.gz
- You have sufficient disk space

### Compatibility Issues
If websocat doesn't run on your system, ensure you're using a Linux distribution compatible with Ubuntu 22.04 (e.g., Debian, Ubuntu 20.04+, etc.).

## Related Links

- **Original Project**: https://github.com/vi/websocat
- **Release Page**: https://github.com/xiongli870110-hue/Websocat/releases
- **Build Workflow**: https://github.com/xiongli870110-hue/Websocat/actions

## License

Please refer to the original websocat project for license information: https://github.com/vi/websocat

## Support

For issues related to this build or installation, please open an issue on this repository.
For websocat itself, refer to the original project: https://github.com/vi/websocat
