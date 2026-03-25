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

This project supports optional local configuration overrides using a layered approach.

#### Base Configuration

- `Config.xcconfig` (committed) contains shared project settings.
- It conditionally includes a local override file (`Config.local.xcconfig`) if present.

#### Local Overrides

To customize settings for your local environment:

1. Create a file at the project root named `Config.local.xcconfig`.
2. Add only the values you need to override, for example:

   ```xcconfig
   PRODUCT_BUNDLE_IDENTIFIER = com.yourname.VirtualMachine
   DEVELOPMENT_TEAM = YOUR_TEAM_ID
