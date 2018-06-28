--
layout: layout.pug
navigationTitle:  Installing and Customizing
title: Installing and Customizing
menuWeight: 20
excerpt: Installing DC/OS Apache Spinnaker from the web interface or the CLI
featureMaturity:
enterprise: false
---

 DC/OS Apache Spinnaker service is available in the Universe and can be installed using either the web interface or the DC/OS CLI.

The default DC/OS Apache Spinnaker Service installation provides reasonable defaults for trying out the service, but that may not be sufficient for production use. You may require different configurations depending on the context of the deployment.

## Prerequisites

- If you are using Enterprise DC/OS, you may [need to provision a service account](https://docs.mesosphere.com/1.10/security/ent/service-auth/custom-service-auth/) before installing DC/OS Spinnaker Service. Only someone with `superuser` permission can create the service account.
  - `strict` [security mode](https://docs.mesosphere.com/1.10/security/ent/service-auth/custom-service-auth/) requires a service account.

 - In `permissive` security mode a service account is optional.
 - The `disabled` security mode does not require a service account.
 - Your cluster must have at least three private nodes.

- **Tip:** A complete guide to Configuring DC/OS Access for Spinnaker can be found [here](../security/serviceaccountdetail.md).

# Installing from the DC/OS CLI

To start a basic test cluster of DC/OS Apache Spinnaker Service, run the following command on the DC/OS CLI. Enterprise DC/OS users must follow additional instructions.

   ```shell
   dcos package install spinnaker
   ```

This command creates a new instance with the default name `spinnaker`. Two instances cannot share the same name, so if you install additional instances beyond the default instance you must customize the name at install time for each additional instance. However, the application can be installed using the same name in case of foldered installation, wherein we can install the same application in different folders.

All DC/OS Apache Spinnaker Service CLI commands have a `--name`  argument, allowing you to specify which instance to query. If you do not specify a service name, the CLI assumes a default value matching the package name, such as `spinnaker`. The default value for `--name` can be customized via the DC/OS CLI configuration:

   ```shell
   dcos spinnaker --name=spinnaker <cmd>
   ```

You can specify a custom configuration in an `options.json` file and pass it to `dcos package install` using the `--options` parameter.

   ```shell
   dcos package install spinnaker --options=options.json
   ```

For more information on building the `options.json` file, see [DC/OS documentation](https://docs.mesosphere.com/latest/usage/managing-services/config-universe-service/) for service configuration access.

## Installing from the DC/OS web interface

Note:  Alternatively, you can install DC/OS Spinnaker Service from the DC/OS web interface. Select the app from the Catalog and choose Deploy.

If you install Apache Spinnaker from the DC/OS web interface, the `dcos spinnaker` CLI commands are not automatically installed to your workstation. They may be manually installed using the DC/OS CLI:

   ```shell
   dcos package install spinnaker --cli
   ```
