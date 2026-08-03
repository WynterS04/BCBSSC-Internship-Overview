# Mobile Apple Wallet

Similar to the AEM GUI project, the contents of this project are confidential. Therefore, instead of showcasing the codebase and final product, I will discuss the project's scope and my approach to it.

## Overview
The My Health Toolkit (MHTK) mobile app is introducing an 'Add to Apple Wallet' button, enabling users to save their ID card directly to their Apple Wallet. When tapped, the button prompts a download of a zip file containing necessary JSON files, images, and a digital signature for verification. My task was to transition the current zip files from a generic branding code to more specific site identifiers for different lines of businesses (LOBs). This involved creating folders named after each LOB that linked to the existing branding code.  

While the project was straightforward, setting up the environment proved challenging for both implementing and testing the code. This experience taught me the importance of perseverance in overcoming roadblocks and managing my time effectively while waiting for approvals.

## Notes
Most of this project was self-explanatory, but one aspect I was unfamiliar with was creating symlinks to ensure the new site ID folders pointed to their existing branding code. Therefore, I included the documentation I used to learn about symlinks, as well as some information I gathered on the complete process of adding IDs to the Apple Wallet.

**~ Key Definitions:**
- **Symlink**: shortcut/ pointer to another directory or file, doesn't contain actual data just stores path to it  
- **pkpass file**: a compressed zip file used to render digital passes through apple wallet. These budles contain json files, image assets, and a digital signature that verifies the pass is a trusted source

### Helpful Links
- [Creating Symlinks in Windows](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/mklink)
- [Pkpass File](https://walletwallet.alen.ro/blog/pkpass-file/)
- [Apple Developer](https://developer.apple.com/documentation/walletpasses/distributing-and-updating-a-pass)