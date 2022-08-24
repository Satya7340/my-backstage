# [Backstage](https://backstage.io)

To play with this project which has been generated using the command `npx @backstage/create-app` and which has been customized to
include the following plugins:

- k8s: https://backstage.io/docs/features/kubernetes/overview
- Carbon Cloud Footprint: https://github.com/cloud-carbon-footprint/ccf-backstage-plugin 

The backend Dockerfile has also been modified (see [commit](https://github.com/halkyonio/my-backstage/commit/2d93a33901128ef78b3ef31906c26c59e6e0bc59)) to install the python mkdocs package able to build locally the documentation.

Clone it and install the nodejs needed packages:
```sh
git clone https://github.com/halkyonio/my-backstage && cd my-backstage
yarn install && yarn build
```

To play with it locally, run:

```sh
yarn dev
```

When an image is needed locally (kind, minikube, ..., then build it:
```sh
yarn build-image -t backstage:dev
kind load docker-image backstage:dev
```
