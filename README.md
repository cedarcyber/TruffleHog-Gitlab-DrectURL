# GitLab TruffleHog Scanner with Post-Processing

This script is a straightforward tool designed to help you scan your GitLab repositories for sensitive information using TruffleHog and perform post-processing to generate direct URLs to the files in GitLab. This feature is especially useful given that TruffleHog scans all layers of a code repository, providing comprehensive coverage compared to tools that may only scan a limited depth.

## Features

- **Automated Scanning**: Utilizes TruffleHog to scan GitLab repositories for sensitive information, such as secrets and API keys, in all layers of the repository.
- **Secure Secret Management**: Leverages 1Password CLI to securely retrieve your GitLab access token, avoiding hardcoding sensitive information directly into the script.
- **Post-Processing for Direct URLs**: After scanning, the script processes the TruffleHog output to extract commit hashes and file paths, constructing direct URLs to the affected files in GitLab. This feature simplifies the process of reviewing and remediating findings by allowing you to quickly navigate to the exact location of potential issues.

## Why This Script?

While TruffleHog is a powerful tool for identifying sensitive information in code repositories, it can be challenging to quickly pinpoint the exact location of findings, especially when dealing with large repositories with deep commit histories. This script addresses this by:

- **Generating Direct Links**: Creates direct URLs to the specific files and commits where sensitive information was found, saving you time and effort in locating and addressing issues.
- **Full Repository Coverage**: Unlike some tools that may only scan a limited depth, TruffleHog scans all layers of a repository. This script makes full use of TruffleHog's comprehensive scanning capabilities and complements it with easy navigation features.
- **Simple and Effective**: While not overly complex, this script provides practical functionality that fills a gap not currently covered by TruffleHog itself, as discussed in [this GitHub issue](https://github.com/trufflesecurity/trufflehog/issues/781).

## Prerequisites

- **Docker**: Ensure Docker is installed and running on your machine.
- **1Password CLI**: Install and configure the 1Password CLI to securely access your GitLab access token. Refer to the [1Password CLI documentation](https://developer.1password.com/docs/cli/get-started/) for setup instructions.

## Usage

1. **Clone the Repository**: 
   ```bash
   git clone https://github.com/your-repo/your-script.git
   cd your-script
   ```

2. **Configure Your Environment**: Ensure you have your 1Password CLI configured and your GitLab access token stored securely.

3. **Run the Script**: 
   ```bash
   python your_script.py
   ```
   Replace `your_script.py` with the actual script filename.

4. **Review the Output**: After the script completes, it will output direct URLs to the files in GitLab where sensitive information was detected. Use these links to quickly navigate and review the findings.

## Contributions

Contributions are welcome! If you have any suggestions or improvements, feel free to submit a pull request or open an issue.

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.

---

This README provides a clear overview of the script's purpose, features, and usage instructions, emphasizing its practical benefits without overcomplicating the explanation.
