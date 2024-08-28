# GitLab TruffleHog Scanner with Post-Processing for Direct URL to Commit Hashes

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

- **Docker**: To get started with Docker:

  1. **Install Docker**: Visit the [Docker website](https://www.docker.com/products/docker-desktop) and download Docker Desktop for your operating system. Follow the installation instructions provided for macOS, Windows, or Linux.
  
  2. **Run Docker**: Once installed, ensure Docker is running on your machine. You can check this by opening a terminal or command prompt and running `docker --version` to verify the installation.

  3. **Pull the TruffleHog Container**: Before running the script, you'll need to pull the TruffleHog Docker image. You can do this by executing the following command in your terminal:
     ```bash
     docker pull trufflesecurity/trufflehog
     ```
     This command downloads the latest TruffleHog container, ensuring you have all the necessary tools to perform the scan.

- **1Password CLI**: The script uses the 1Password CLI to securely retrieve your GitLab access token, keeping your secrets safe. To set up the 1Password CLI:

  1. **Install the 1Password CLI**: Follow the instructions in the [1Password CLI documentation](https://developer.1password.com/docs/cli/get-started/) to install the CLI for your operating system.
  
  2. **Configure the 1Password CLI**: Once installed, you’ll need to authenticate the CLI with your 1Password account and set up access to the vault containing your GitLab access token. The documentation provides detailed steps on how to securely configure and use the CLI.


## Contributions

Contributions are welcome! If you have any suggestions or improvements, feel free to submit a pull request or open an issue.

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.

