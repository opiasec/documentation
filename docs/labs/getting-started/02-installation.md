---
sidebar_label: 'Install'
---

# ⚙️ Installation

1. Clone the project and install the frontend dependencies:

```bash
git clone https://github.com/opiasec/opiaseclabs.git
cd opiaseclabs/front-end
npm install
```

2. To simplified deployment, we are using Makefile. First, you're going to need to setup the Kubernetes cluster:

```bash
# If you're not in the root
cd ../

# In the root
cd kubernetes
make install
```

3. Get the kubeconfig content:
```bash
cat ~/.kube/kubeconfig > kubeconfig
```

4. Open the 'kubeconfig' file with your prefered text editor and edit the *cluster server* value to **https://kind-control-plane:6443**, like the example below. 

```yaml
apiVersion: v1
clusters:
  - cluster:
      certificate-authority-data: [...]d2RPK2NvemZXCi0tLS0tRU5EIENFUlRJRklDQVRFLS0tLS0K
      //highlight-next-line
      server: https://kind-control-plane:6443
    name: kind-kind
contexts:
  - context:
    [...]
```

5. Encode the kubeconfig modified as base64 and insert that value in **.env** (project root), in the variable **KUBECONFIG_BASE64**.
```bash
cat kubeconfig | base64 -w0
```

:::warning[External clusters]
If you already have a deployed cluster, you need to pay attention in your **kubeconfig** cluster server url and authentication methods. The docker container ***needs to be able to access the Kubernetes cluster API***.
:::

6. Go back to the project's root and update the **.env** (you can rename the .env.example). In addition to **KUBECONFIG_BASE64**, you need to update at least:
    - **GITHUB_INIT_CONTAINER_USERNAME**: with your github username
    - **GITHUB_INIT_CONTAINER_PAT**: with your github personal access token, with permissions *read packages* and *read projects* (that's necessary for pulling labs repositories)

:::note[Recommendation]
We do recommend to update all the *password* variables. Also, you can setup an auth provider if you want to, in section *'*Auth Provider Configuration*. The basic setup is using the **Auth Password Configuration**.
:::

7. With all variables set, run the Make command to execute the *Docker compose* and connect the cluster container to the Labs network. 

```bash
# In the project's root
make install
```

:::tip[External cluster]
if you have used an external cluster, use the command `make docker-compose`.
:::

8. The last step is to start the front-end. Go to *front-end* folder and start the service:

```bash
cd front-end
npm start
```

9. The project now should be up and running. Navigate to `localhost:4200` and access using the credentials you've setted up in .env.