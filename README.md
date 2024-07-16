# PawKit

PawKit is a streamlined macOS application installer framework that simplifies the installation process for developers and users. By leveraging `.Paw` packages, PawKit provides a user-friendly and efficient method for distributing and installing macOS applications.

## Features

- **Simple Installation Process**: PawKit automates the installation of files to their correct locations, reducing manual setup steps.
- **Dynamic Path Mapping**: The framework dynamically maps installation paths, ensuring files are placed in the appropriate directories (e.g., `~/Documents`, `~/Library/Application Support`).
- **Flexible Package Format**: Uses `.Paw` packages, which are simply renamed `.zip` files containing the necessary application files and metadata.
- **User-Friendly**: Designed to provide a seamless experience for both developers and end-users.

## How It Works

PawKit operates using `.Paw` packages that contain:

- **Metadata**: Includes information such as icons, backgrounds, and other relevant data.
- **Files**: The actual files to be installed, organized in a directory structure that mirrors the destination paths on the user's system.

When a `.Paw` package is executed, PawKit extracts the files and places them in the specified directories based on the dynamic path mappings.

## Installation

To use PawKit, follow these simple steps:

1. **Create a `.Paw` Package**:
    - Organize your application files and metadata into a directory structure.
    - Compress the directory into a `.zip` file.
    - Rename the `.zip` file to have a `.Paw` extension.

2. **Distribute the Package**:
    - Share the `.Paw` package with your users.

3. **Run the Installer**:
    - Users can execute the installer script provided by PawKit to install the application.

## Example

Here is an example of how to structure your `.Paw` package:

```
MyApp.Paw
├── metadata
│   ├── data.json
│   ├── icon.png
│   └── bg.jpg
└── files
    ├── @Documents
    │   └── example.txt
    └── @ApplicationSupport/MyApp
        └── config.json
```

## Contributing

We welcome contributions to PawKit! If you have suggestions for improvements or have found bugs, please open an issue or submit a pull request.

## ToDo
- **Move to C**

## Ideas
- **Repos**

