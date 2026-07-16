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

* [plone](https://github.com/IMIO/helm-plone)

  ```bash
  helm install your-release-name imio/plone
  ```

* [smtp4dev](https://github.com/IMIO/helm-smtp4dev)

  ```bash
  helm install your-release-name imio/smtp4dev
  ```

### Verify chart signatures

Chart releases can optionally be signed with a GPG key, which produces a provenance file (`<chart>-<version>.tgz.prov`) published alongside the `.tgz`. If the version you want to install has a matching `.prov` file, you can verify it came from @IMIO before installing.

* Public key: [imio-helm-pubkey.asc](./imio-helm-pubkey.asc) (also served at https://imio.github.io/helm-charts/imio-helm-pubkey.asc)
* Fingerprint: `99D0 D64F 8598 75E8 C74C D910 801C 27FD 9E48 A92A`
* Owner: `devops (GPG key to sign IMIO helm chart) <devops@imio.be>`

Always check the fingerprint below against the imported key — don't trust the key file alone, since anyone who could tamper with the download could ship a matching-looking key too.

```bash
# 1. Import the key, then confirm its fingerprint matches the one above
curl -sSL https://imio.github.io/helm-charts/imio-helm-pubkey.asc | gpg --import
gpg --fingerprint devops@imio.be

# 2. Export a binary keyring (the armored .asc will NOT load in `helm verify`)
gpg --export devops@imio.be > imio-helm.gpg

# 3. Install or pull with verification
helm install your-release-name imio/smtp4dev --verify --keyring ./imio-helm.gpg
```

### License

[Apache License 2.0](/LICENSE)
