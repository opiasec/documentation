---
sidebar_label: 'Install'
---

# Installation

Hello! Welcome to the installation guide for the *opiasec* Labs. This guide will help you set up the Labs environment on your local machine.

Please see the [Requirements](./01-requirements.md) page before proceeding with the installation.

## 1. Clone
Clone the [repository](https://github.com/opiasec/labs.git).

```bash
git clone https://github.com/opiasec/labs.git
```

## 2. Install Frontend Dependencies
After cloning the repository, navigate to the `front-end` directory and install the necessary dependencies using npm:

```bash
cd front-end
npm install
```

## 3. (Optional) Setup Kubernetes Cluster
You need a [Kubernetes](https://kubernetes.io/) cluster to run the Labs. The Labs are designed to run in a Kubernetes environment, which allows for better scalability and management of resources.

:::danger[Important]
Your Kubernetes cluster **must be accessible from the Docker container of Cluster API**. This is crucial for the Labs to function correctly.

Additionally, your Kubernetes cluster must have a ingress nginx controller installed. This is necessary for routing traffic to the Labs services.
:::

:::note[Recommendation]
We recommend to use [Kind](https://kind.sigs.k8s.io/) for local development, as it allows you to run Kubernetes clusters in Docker containers.
:::

If you want to follow our local setup recomendations, ensure you are in the **root of the project directory** and **have Docker and Kind installed**. Then run the following commands to set up a Kubernetes cluster using Kind:
```bash
make -C kubernetes install
```

## 4. Setup kubeconfig in base64 format:

The Cluster API needs a `kubeconfig` to access the Kubernetes cluster. This needs to be a base64 encoded version of your kubeconfig file.

1. (Optional) If you are using Kind, generate the kubeconfig file by makefile command:
```bash
make -C kubernetes get-kubeconfig
```
This command will create a file named `kubeconfig_base64` in the `kubernetes` directory, with the `server` endpoint setted to `https://kind-control-plane:6443` - ensuring that the Cluster API can access the Kubernetes cluster.

2. Set the `KUBECONFIG_BASE64` environment variable with the base64 encoded kubeconfig file. You can do this setting the variable in a .env file (see [3. Set environment variables](#3-set-environment-variables)).


## 5. Set environment variables 
Go back to the project's root and update the **.env** (you can rename the .env.example). You need to modify at least the following variables:
    - **KUBECONFIG_BASE64**: with your base64 encoded kubeconfig file. For more information, see [4. Setup kubeconfig in base64 format](#4-setup-kubeconfig-in-base64-format)
    - **GITHUB_INIT_CONTAINER_USERNAME**: with your github username
    - **GITHUB_INIT_CONTAINER_PAT**: with your github personal access token, with permissions *read packages* and *read projects* (that's necessary for pulling labs repositories)

:::warning[Important]
All the variables are documented in the **.env.example** file. Please, read it carefully and set the variables accordingly.
:::note[Recommendation]
We do recommend to update all the *password* variables. Also, you can setup an auth provider if you want to, in section *'*Auth Provider Configuration*. The basic setup is using the **Auth Password Configuration**.

:::

## 6. Setup Local Environment
With all variables set, run the Make command to execute the *Docker compose* and connect the cluster container to the Labs network. 

```bash
make install
```

:::tip[External cluster]
If you have used an external cluster, use the command `make docker-compose`.
:::

## 7. Setup Frontend Environment
The last step is to start the front-end. Go to *front-end* folder and start the service:

```bash
cd front-end
npm start
```

The project now should be up and running. Navigate to `localhost:4200` and access using the credentials you've setted up in .env.

Have fun!

## Extra Tips

### Help
You can run `make help` to see all available commands and their descriptions. You can also run `make -C kubernetes help` to see the available commands for the Kubernetes setup.


### Need more help?
If you have any questions or need further assistance, feel free to reach out to us on our [Discord](https://discord.gg/hXdwCW7e87) or open an issue in the [Labs repository](https://github.com/opiasec/labs/issues).