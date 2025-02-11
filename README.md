# Google Photos Loader for ComfyUI

![Google Photos Loader Example Workflow](Google_photo_loader_example_workflow.svg)

## Tutorial

Check out this video tutorial to see the Google Photos Loader for ComfyUI in action:

[![Google Photos Loader for ComfyUI Tutorial](https://img.youtube.com/vi/vWg-WUrNKyE/0.jpg)](https://www.youtube.com/watch?v=vWg-WUrNKyE "Google Photos Loader for ComfyUI Tutorial")

# Google Photos Loader for ComfyUI

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python 3.7+](https://img.shields.io/badge/python-3.7+-blue.svg)](https://www.python.org/downloads/release/python-370/)
[![ComfyUI](https://img.shields.io/badge/ComfyUI-compatible-brightgreen)](https://github.com/comfyanonymous/ComfyUI)

## Table of Contents

- [Description](#description)
- [Features](#features)
- [Installation](#installation)
- [Setting up Google Photos API](#setting-up-google-photos-api)
- [Usage](#usage)
- [Node Types](#node-types)
- [Troubleshooting](#troubleshooting)
- [Dependencies and Licenses](#dependencies-and-licenses)
- [About the Creator](#about-the-creator)
- [License](#license)
- [Contributing](#contributing)
- [Support](#support)
- [To-Do List](#to-do-list)

## Description

The Google Photos Loader for ComfyUI is a custom node that allows users to seamlessly integrate Google Photos into their ComfyUI workflows. This powerful tool enables direct access to your Google Photos library, making it easy to list albums, load images from specific albums, and load images based on various criteria - all within your ComfyUI environment.

## Features

- 📁 List all Google Photos albums
- 🖼️ Load images from a specific album
- 🔍 Load images based on content categories, date, and other filters
- 🛠️ Customize image loading options (size, cropping, etc.)
- 🔄 Efficient caching mechanism for improved performance
- 🔐 Secure login and logout functionality
- 🧹 Cache management tools

## Installation

1. Ensure you have ComfyUI installed and set up.
2. Clone this repository into your ComfyUI's `custom_nodes` directory:
   ```bash
   cd /path/to/ComfyUI/custom_nodes
   git clone https://github.com/lazniak/comfyui-google-photos-loader.git
   ```
3. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Setting up Google Photos API

To use this node, you need to set up a Google Cloud project and enable the Google Photos Library API:

1. Go to the [Google Cloud Console](https://console.cloud.google.com/).
2. Create a new project or select an existing one.
3. Enable the Google Photos Library API for your project.
4. Create credentials (OAuth 2.0 Client ID) for a desktop application.
5. Download the client configuration and save it as `client_secrets.json` in the same directory as the custom node files.

## Usage

1. In ComfyUI, you'll find several new nodes related to Google Photos.
2. Drag and drop the desired node into your workflow canvas.
3. Connect the node to your workflow as needed.
4. Configure the node settings according to your requirements.
5. Run your workflow. The node will authenticate with Google Photos on first use.

## Node Types

### Google Photos Album Lister
- Lists all albums in your Google Photos library.
- Outputs album information including ID, title, and item count.

### Google Photos Album Selector
- Allows you to select a specific album from the list generated by the Album Lister.
- Outputs the selected album ID for use in other nodes.

### Google Photos Album Loader
- Loads images from a specified album.
- Customizable options for image size, count, and processing.

### Google Photos Images Loader
- Loads images from your entire Google Photos library.
- Supports advanced filtering options like content categories and date ranges.

### Google Photos Cache Manager
- Manages the local cache of downloaded images.
- Options to clear cache or limit cache size.

### Google Photos Login/Logout
- Handles authentication with Google Photos.
- Allows for secure login and logout functionality.

### Content Filter Node
- Allows you to specify content categories for filtering images.

### Date Picker Node
- Provides a simple interface for selecting dates, useful for date-based image filtering.

## Troubleshooting

- If you encounter authentication issues, use the Login/Logout node to reset your authentication.
- Ensure your `client_secrets.json` file is correctly placed and formatted. (IMPORTANT!!! NAME SHOULD HAVE "s" rather then original file was secret in this case use secrets)
- Check the ComfyUI console for detailed logs if you enable the "Advanced Logs" option in the nodes.
- If you're experiencing performance issues, try using the Cache Manager node to optimize your local cache.

## Dependencies and Licenses

This project uses the following main dependencies:

1. **aiohttp** (Apache 2.0 License) - Version: >=3.7.4
2. **google-auth-oauthlib** (Apache 2.0 License) - Version: >=0.4.1
3. **google-auth** (Apache 2.0 License) - Version: >=1.30.0
4. **Pillow** (HPND License) - Version: >=8.0.0
5. **torch** (BSD 3-Clause License) - Version: >=1.7.0
6. **termcolor** (MIT License) - Version: >=1.1.0
7. **numpy** (BSD 3-Clause License) - Version: >=1.19.0

For full license details, please refer to the individual package repositories.

## About the Creator

[The "About the Creator" section remains unchanged]

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## Support

If you encounter any issues or have questions, please file an issue on the GitHub repository. For more detailed support or custom development inquiries, you can reach out to Paul directly through his social media channels or website.

## To-Do List

- Implement more advanced sorting and filtering options
- Enhance error handling and user feedback
- Optimize performance for large image libraries
- Develop more integration options with other ComfyUI nodes

---

Enjoy using the Google Photos Loader in your ComfyUI workflows!
## About the Creator

This ComfyUI CustomNode was created by Paul Lazniak (Paweł Łaźniak), also known as PabloGFX. Paul is a multifaceted professional with extensive experience in software development, filmmaking, VFX artistry, and entrepreneurship.

### Professional Background

Paul began his career in the early 2000s, working on various projects for prominent Polish TV stations such as MTV, TVN, and TVP. His expertise spans compositing, editing, special effects, and software development.

As an innovator in virtual reality (VR), Paul co-founded the VR Visio Group, which later evolved into Ignibit S.A., one of Poland's leading companies focused on virtual reality and immersive technologies.

### Current Ventures

Paul is currently involved in developing new projects through his companies:

- [HexArt](https://www.hexart.pl/): Combining cinematography with advanced digital technologies
- [Overbuilt Games](https://overbuiltgames.com/): Game development studio
- [Green Cave Studio](https://greencavestudio.com/): Creative digital solutions

### Content Creation and Education

Paul is a Polish-speaking content creator focusing on technology and digital tools. He provides tutorials and guides, particularly on topics such as Stable Diffusion and other AI-based tools.

### Contributions to Film and VR

Paul's contributions to the Polish film industry are documented in the [Polish Film Database](https://filmpolski.pl/fp/index.php?osoba=1162919). He is also known for his thought leadership in digital and virtual realities.

### Connect with Paul

- Website: [hexart.pl](https://hexart.pl)
- YouTube: [@Lazniak](https://www.youtube.com/@Lazniak)
- Facebook: [PabloGFX](https://www.facebook.com/PabloGFX)
- Twitter: [@PabloGFX](https://x.com/PabloGFX)
- GitHub: [github.com/PabloGFX](https://github.com/PabloGFX)
- LinkedIn: [linkedin.com/in/paul-lazniak](https://www.linkedin.com/in/paul-lazniak)

To learn more about Paul's journey and work, check out his [bio video](https://www.youtube.com/watch?v=5KIcxuWEa4E).

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

Please ensure you follow our [Code of Conduct](CODE_OF_CONDUCT.md) and read our [Contributing Guidelines](CONTRIBUTING.md) before making a submission.

## Support

If you encounter any issues or have questions, please file an issue on the GitHub repository. For more detailed support or custom development inquiries, you can reach out to Paul directly through his social media channels or website.

## To-Do List

- Improve randomization feature
- Fully implement and enhance the Image Search feature with search query functionality

Note: The Image Search feature is currently under development. Contributions to improve this feature are welcome!

---

Enjoy using the Google Photos Loader in your ComfyUI workflows!
