# Install Entando CLI

The Install Entando CLI is a command-line tool for simplifying the installation of Entando, a modern, micro front-end platform. This tool streamlines the installation process and provides a guided experience to set up Entando in your Kubernetes cluster. All the flags are optional and only serve to bypass the provided guided inputs.

## Installation

Before using the Entando CLI, make sure you have Node.js and npm (Node Package Manager) installed on your system. You can download them from the official [Node.js website](https://nodejs.org/).

Once Node.js and npm are installed, you can install the Install Entando CLI globally using npm:

```bash

npm  install  -g  install-entando

```

## Usage

The Install Entando CLI is designed to simplify the installation of Entando in a Kubernetes cluster. You can use it with or without command-line flags to customize the installation process.

### Installation Command

To start the installation process, simply run the following command:

```bash

install-entando

```

This command will interactively prompt you for various configuration options required for the Entando installation.

### Command Flags

Alternatively, you can use command-line flags to provide the inputs requested by the CLI in advance. Here are the available flags:

-  `-v, --entandoversion`: Specify the version of Entando to install.

-  `-n, --namespace`: Define the Kubernetes namespace in which to install Entando.

-  `-p, --project`: Set the name of the project to deploy.

-  `-h, --hostname`: Specify the hostname to use for the Entando app.

-  `-t, --tls`: Enable TLS (Transport Layer Security) for the installation.

-  `-l, --local`: Choose whether you want to install Entando in a local environment (e.g., minikube, k3s).

#### Example
In this example, we specify the version, namespace, project name, hostname, enable TLS, and specify we're going to install Entando in a local environment:
```bash

install-entando  --entandoversion 7.2.2  --namespace  my-namespace  --project  my-entando-project  --hostname  my-entando-host.nip.io --tls --local

```

**Note:** You have the flexibility to provide some of the flags for configuration while leaving others unspecified. When you execute the Install Entando CLI with a mix of flags and unspecified options, the CLI will seamlessly combine your provided inputs with interactive prompts for any remaining configuration details. This allows you to customize your installation as needed while maintaining the convenience of interactive guidance.

## Configuration

The Install Entando CLI uses your Kubernetes configuration to interact with your cluster. Ensure that your `kubectl` is properly configured with the desired context and permissions before running the installation.

## Additional Information

- [Entando Official Website](https://www.entando.com/)
- [Entando GitHub Repository](https://github.com/entando)

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- The Install Entando CLI is built using [oclif](https://oclif.io/), an open-source framework for building command-line tools in Node.js.
