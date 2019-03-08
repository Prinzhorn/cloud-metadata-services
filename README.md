# cloud-metadata-services

List of metadata service endpoints for different cloud providers for your pentesting needs.

| Provider                  | Metadata Endpoint Example                                                  | Protection                                                                             | Documentation                                                                             |
| ------------------------- | -------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- |
| Amazon Web Services (AWS) | `http://169.254.169.254/latest/meta-data/ami-id`                           | _none_ (custom logic[1] possible)                                                      | https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-instance-metadata.html            |
| Google Cloud              | `http://metadata.google.internal/computeMetadata/v1/instance/machine-type` | `Metadata-Flavor: Google` header, rejects `X-Forwarded-For` (bypass using `/v1beta1/`) | https://cloud.google.com/compute/docs/storing-retrieving-metadata                         |
| Microsoft Azure           | `http://169.254.169.254/metadata/instance?api-version=2017-12-01`          | `Metadata:true` header, rejects `X-Forwarded-For`                                      | https://docs.microsoft.com/en-us/azure/virtual-machines/windows/instance-metadata-service |
| DigitalOcean              | `http://169.254.169.254/metadata/v1/`                                      | _none_                                                                                 | https://www.digitalocean.com/docs/droplets/resources/metadata/                            |
| OpenStack                 | `http://169.254.169.254/openstack/latest`                                  | _none_                                                                                 | https://blogs.vmware.com/openstack/introducing-the-metadata-service/                      |
| Rancher (Kubernetes)      | `http://rancher-metadata/2015-07-25/`                                      | _none_                                                                                 | https://rancher.com/introducing-rancher-metadata-service-for-docker/                      |

[1] https://medium.com/netflix-techblog/netflix-information-security-preventing-credential-compromise-in-aws-41b112c15179

Feel free to add more services and details. The Markdown is formatted using [prettier](https://prettier.io/), I'd appreciate if PRs do that as well.
