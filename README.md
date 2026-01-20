# Kubernetes Helm charts by @IMIO

This is a [Helm](https://helm.sh) charts repository for Kubernetes made by @IMIO.

### Add Helm repository

To install the [imio](https://www.imio.be/) repo just run:

```bash
helm repo add imio https://imio.github.io/helm-charts
helm repo update
```

### Helm Charts

* [odoo](https://github.com/IMIO/helm-odoo)

  ```bash
  helm install your-release-name imio/odoo
  ```

* [onechart](https://github.com/IMIO/helm-onechart)

  ```bash
  helm install your-release-name imio/onechart
  ```

* [plausible-analytics](https://github.com/IMIO/helm-plausible-analytics)

  ```bash
  helm install your-release-name imio/plausible-analytics
  ```

* [odoo](https://github.com/IMIO/helm-plone)

  ```bash
  helm install your-release-name imio/plone
  ```

* [smtp4dev](https://github.com/IMIO/helm-smtp4dev)

  ```bash
  helm install your-release-name imio/smtp4dev
  ```

### License

[Apache License 2.0](/LICENSE)
