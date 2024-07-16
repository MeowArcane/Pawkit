# PawKit

PawKit is a streamlined application and package installer framework that simplifies the installation process for developers and users. By leveraging `.Paw` packages, PawKit provides a user-friendly and efficient method for distributing and installing applications.

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
    - Compress the directory into a NeoAppleArchive file.
    - Rename the file to have a `.Paw` extension.

2. **Distribute the Package**:
    - Share the `.Paw` package with your users.

3. **Run the Installer**:
    - Users can execute the installer script provided by PawKit to install the application.

## Commands

PawKit provides a variety of commands to manage packages, applications and repositories.

- `install <path_to_paw>` - Install an package from a `.Paw` package.
- `install <name_of_paw>` - Install an package from a repo package.
- `delete <name of paw>` - Uninstall package using the cached metadata
- `addrepo <url_to_repo.json>` - Add a repository to the list of available repositories.
- `removerepo <repository_name>` - Remove a repository from the list.
- `update <app_name>` - Update a specific package to its latest version.
- `update <repo_name>` - Update a specific repo to its latest version.
- `update all` - Update all installed repos and packages to their latest versions.

## Example

Here is an example of how to structure your `.Paw` package:

```
MyApp.Paw
├── metadata
│   ├── data.json
│   ├── icon.png
│   └── bg.jpg
└── files
    └── @macos
        ├── @Documents
        │   └── example.txt
        └── @ApplicationSupport/MyApp
            └── config.json
```

## Contributing

We welcome contributions to PawKit! If you have suggestions for improvements or have found bugs, please open an issue or submit a pull request.
