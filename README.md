# VS Code Devcontainer

This repository contains the necessary files to set up a development environment using Visual Studio Code's devcontainer feature.

It installs the following tools:

- docker-outside-docker - to run the docker on the host machine from the container
- python Versions: 3.9, 3.10, 3.11, 3.12
- poetry - Python dependency management tool
- git-lfs - Git Large File Storage support for Git

The user is set to `vscode` with UID $(id -u) and GID $(id -u) of the user on the host machine. This is to ensure that the user has the same permissions inside the container as they do on the host machine.

The developers ~/.ssh directory is mounted into the container to allow for SSH key access to repositories.

## Prerequisites

Before getting started, make sure you have the following installed on your machine:

- [Docker](https://www.docker.com/get-started)
- [Visual Studio Code](https://code.visualstudio.com/download)
- [Remote - Containers extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)

## Getting Started

To get started with the devcontainer, follow these steps:

1. Clone this repository to your local machine in your workspace folder. where `*.code-workspace` is located. 
2. Open the workspace in Visual Studio Code.
3. When prompted, click on the "Reopen in Container" button in the bottom-right corner of the editor.
4. Visual Studio Code will automatically build the devcontainer using the Dockerfile and devcontainer.json files provided.
5. Once the devcontainer is built, you will be connected to the development environment inside the container.

## Customizing the Devcontainer

You can customize the devcontainer to fit your specific needs. Here are a few things you can do:

- Modify the Dockerfile to install additional dependencies or tools.
- Update the devcontainer.json file to configure VS Code extensions, settings, or environment variables.

## Contributing

If you find any issues or have suggestions for improvements, feel free to open an issue or submit a pull request.

## License

This project is licensed under the [Apache-2.0 License](LICENSE.md).