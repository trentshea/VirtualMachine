# VirtualMachine

A macOS application utilizing Apple’s Virtualization Framework to create and manage virtual machines.

## Table of Contents
- [About the Project](#about-the-project)
- [Built With](#built-with)
- [Getting Started](#getting-started)
  - [Configuration](#configuration)

## About the Project
A personal project focused on developing a functional macOS application using Xcode and Swift for setting up and managing virtual machines.

## Built With
- [Xcode](https://developer.apple.com/xcode/)
- [Apple Virtualization Framework](https://developer.apple.com/documentation/virtualization)

## Getting Started

### Configuration

This project supports optional local configuration overrides using a layered configuration approach.

#### Base Configuration

- `Config.xcconfig` is committed to the repository and contains shared project settings.
- It is already configured to include a local override file (`Config.local.xcconfig`) if one exists.

#### Local Overrides

To customize settings for your local environment:

1. Open the project in Xcode
2. Create a new **Configuration Settings File** named:
   ```
   Config.local.xcconfig
   ```
3. Add any overrides you need, for example:

```xcconfig
PRODUCT_BUNDLE_IDENTIFIER = com.yourname.VirtualMachine
DEVELOPMENT_TEAM = YOUR_TEAM_ID
```

> ⚠️ Note:
> `Config.local.xcconfig` is ignored by Git and should not be committed.

#### Notes

- Values in `Config.local.xcconfig` override those in `Config.xcconfig`
- If the local file does not exist, the project will still build normally
- Only include values that need to differ locally; do not duplicate the entire config
- This approach avoids per-developer Git configuration and keeps the project fully shareable
