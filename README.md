# WinTakeOwnership

WinTakeOwnership is a Windows registry script designed to add a "Take Ownership" option to the right-click context menu for files, folders, and drives. This utility streamlines permission management by allowing users to quickly assume ownership of objects without navigating through multiple system dialogs.

## Features

- **Quick Access:** Right-click on files, directories, or drives to instantly take ownership.
- **Optimized Commands:** Uses built-in Windows tools (`takeown` and `icacls`) with streamlined commands.
- **System Protection:** Excludes critical system directories (e.g., `C:\Windows`, `C:\Program Files`) to prevent accidental modifications.
- **PowerShell Integration:** Utilizes hidden PowerShell commands for a seamless user experience.

## Prerequisites

- Windows operating system (Windows 10 or later recommended)
- Administrative privileges to apply registry changes

## Installation

1. **Backup Your Registry:**  
   Always create a system restore point or back up your registry before making changes.

2. **Apply the Script:**  
   - Double-click the `.reg` file to merge it into your registry.
   - Alternatively, right-click the file and select "Merge" from the context menu.

3. **Usage:**  
   After applying the script, right-click on any file, folder, or drive (except for excluded system directories) and select **Take Ownership**. The script will execute the necessary commands to change the ownership and update permissions.

## How It Works

- **For Files:**  
  The script launches a hidden PowerShell window that executes a command to change ownership (`takeown`) and updates permissions (`icacls`).

- **For Directories:**  
  Similar to files, but with recursive commands ensuring all subdirectories and files are updated.

- **For Drives:**  
  Uses a similar approach to update the entire drive, excluding the root drive (`C:\`) for safety.

## Disclaimer

This script makes changes to your Windows registry. While it has been optimized for safety and ease of use, incorrect usage may result in system instability or unintended changes. **Always back up your registry and create a system restore point before proceeding.**

## Contributing

Contributions, improvements, and suggestions are welcome! Feel free to open issues or submit pull requests to enhance the functionality or documentation.

## License

This project is licensed under the [MIT License](LICENSE).

## References

- [TenForums Tutorial](https://www.tenforums.com/tutorials/3841-add-take-ownership-context-menu-windows-10-a.html) – Original tutorial used as a reference for this script.

---

Feel free to customize the content as needed before uploading to GitHub. This structure provides clear instructions, safety warnings, and contribution guidelines to help users understand and safely use your utility.
