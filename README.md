## Unofficial affecto.xyz development domain DNS configuration repository

Edit the `Routefile` to add, change or remove DNS entries for the domain affecto.xyz.

When you push your changes, the Travis CI service (configured in `.travis.yml`)
will use the [`roadworker`](http://roadworker.codenize.tools/) tool to push the 
new DNS configuration to the Amazon AWS Route53 DNS service.

The domain registration and Route53 are currently on Mikael Gueck's Gandi.net
and AWS accounts. Perhaps it might be a good idea to move them at some point?

The relevant AWS IAM credentials are specifically crafted to only allow write
access to this one hosted zone on Route53, see `zone-iam-policy.json`.
The actual IAM credentials are embedded as encrypted environmental variables in
the `.travis.yml` configuration file.

Travis CI: https://travis-ci.org/affecto/affecto.xyz-route53

GitHub: https://github.com/affecto/affecto.xyz-route53
