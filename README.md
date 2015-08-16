# ansible-s3-wesbite

A simple ansible role that uses S3, Route53, and cloudfront to create a low-latency static website.

[![Platforms](http://img.shields.io/badge/platforms-ubuntu-lightgrey.svg?style=flat)](#)

Tunables
--------

* `s3_website_domain` (string) - The root domain of your static website. e.g example.com
* `s3_website_region` (string) - The region for your S3 bucket
* `s3_website_s3_endpoint` (string) - The S3 website endpoint. Better to not touch this
* `s3_website_directory` (string) - The local directory where your website is located
* `s3_website_index_document` (string) - The website index document
* `s3_website_error_document` (string) - The website error document
* `s3_website_ns_servers_enabled` (boolean) - If you need to add NS servers from another domain provider
* `s3_website_ns_servers` (list) - A list of NS servers
* `s3_wesbite_bucket_policy` (string) - The bucket policy for S3
* `s3_website_cloudfront_distribution` (string) - The distribution configuration for cloudfront

Dependencies
------------
* [AWS CLI](http://docs.aws.amazon.com/cli/latest/userguide/installing.html)

Example Playbook
----------------
```
- hosts: servers
  roles:
     - role: noqcks.s3-website
       s3_website_domain: "benvisser.me"
       s3_website_directory: "/Users/benvisser/data/website"
```

License
-------
[MIT](https://tldrlegal.com/license/mit-license)

Contributors
------------
* [Ben Visser](https://github.com/noqcks) | [e-mail](mailto:theodore.r.visser@gmail.com)
