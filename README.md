# BootSkin for Reborn XP

This repository contains the official **BootSkin** application, a utility for customizing the boot screen of the [Reborn XP simulator](https://xp.quenq.com).

It allows users to select from a list of built-in boot screens or add their own custom media (GIFs, videos, or static images). This repository is the central place for the community to contribute new, high-quality boot skins for everyone to enjoy.

## Features

*   **Apply Built-in Skins:** Includes classic boot screens like Windows XP Professional, Home, Tablet PC, Whistler, and x64 Edition.
*   **Add Custom Media:** Users can add their own boot screens from any supported media file on their virtual drives (`.gif`, `.mp4`, `.jpg`, etc.).
*   **Customize Properties:** Edit the properties of any skin, including its name, display style (`contain`, `cover`, `stretch`, `center`), background color, and boot duration.
*   **Live Preview:** Instantly preview any boot screen in a full-screen, interactive overlay.
*   **Reset to Default:** A one-click option to remove all customizations and restore the original set of boot screens.

## How to Submit a New Skin

We welcome community contributions! To get your boot screen included as a built-in option, please follow these steps:

1.  **Prepare Your Media File**
    *   Create your boot screen as a high-quality `.gif`, `.mp4`, or other supported format.
    *   Please optimize the file size to ensure a smooth loading experience for all users.

2.  **Fork This Repository**
    *   Create a fork of the `Quenq-Systems/boot-skin` repository on your own GitHub account.

3.  **Add Your File**
    *   Place your media file (e.g., `my-cool-skin.gif`) inside the `/skins` directory.

4.  **Update the Application Code**
    *   Open `bootskin.js` in a text editor.
    *   Locate the `defaultSkins` array near the top of the file.
    *   Add a new JavaScript object to the end of the array for your skin. Use the template below:

    ```javascript
    // Example entry to add to the defaultSkins array
    { 
        id: 'my-cool-skin', // A unique, lowercase, hyphenated ID
        name: 'My Cool Skin', // The display name shown in the app
        author: 'Your Name', // Your name or alias
        description: 'A brief, fun description of the skin.',
        type: 'gif', // 'gif', 'video', or 'image'
        path: 'skins/my-cool-skin.gif', // The path to your file inside the /skins folder
        style: 'contain', // 'contain', 'cover', 'stretch', or 'center'
        bgColor: '#000000', // The hex code for the background color
        delay: 4000 // The boot duration in milliseconds
    }
    ```

5.  **Submit a Pull Request**
    *   Commit your changes and push them to your forked repository.
    *   Open a Pull Request back to the main `Quenq-Systems/boot-skin` repository.
    *   Please provide a clear title and a brief description of your submission. We'll review it, and once approved, your skin will be part of the next official release!

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.