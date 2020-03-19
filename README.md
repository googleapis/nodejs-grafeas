[//]: # "This README.md file is auto-generated, all changes to this file will be lost."
[//]: # "To regenerate it, use `python -m synthtool`."
<img src="https://avatars2.githubusercontent.com/u/2810941?v=3&s=96" alt="Google Cloud Platform logo" title="Google Cloud Platform" align="right" height="96" width="96"/>

# [Grafeas: Node.js Client](https://github.com/googleapis/nodejs-grafeas)

[![release level](https://img.shields.io/badge/release%20level-general%20availability%20%28GA%29-brightgreen.svg?style=flat)](https://cloud.google.com/terms/launch-stages)
[![npm version](https://img.shields.io/npm/v/@google-cloud/grafeas.svg)](https://www.npmjs.org/package/@google-cloud/grafeas)
[![codecov](https://img.shields.io/codecov/c/github/googleapis/nodejs-grafeas/master.svg?style=flat)](https://codecov.io/gh/googleapis/nodejs-grafeas)




A [Grafeas API Client](https://grafeas.io/) compatible with Google Cloud's
[Container Analysis API](https://cloud.google.com/container-registry/docs/container-analysis).


* [Grafeas Node.js Client API Reference][client-docs]
* [Grafeas Documentation][product-docs]
* [github.com/googleapis/nodejs-grafeas](https://github.com/googleapis/nodejs-grafeas)

Read more about the client libraries for Cloud APIs, including the older
Google APIs Client Libraries, in [Client Libraries Explained][explained].

[explained]: https://cloud.google.com/apis/docs/client-libraries-explained

**Table of contents:**


* [Quickstart](#quickstart)
  * [Before you begin](#before-you-begin)
  * [Installing the client library](#installing-the-client-library)
  * [Using the client library](#using-the-client-library)
* [Samples](#samples)
* [Versioning](#versioning)
* [Contributing](#contributing)
* [License](#license)

## Quickstart

### Before you begin

1.  [Select or create a Cloud Platform project][projects].
1.  [Enable the Grafeas API][enable_api].
1.  [Set up authentication with a service account][auth] so you can access the
    API from your local workstation.

### Installing the client library

```bash
npm install @google-cloud/grafeas
```


### Using the client library

```javascript

// const projectId = 'my-project';

// instantiate the client.
const grpc = require('@grpc/grpc-js');
const {GrafeasClient} = require('@google-cloud/grafeas');
const client = new GrafeasClient({
  sslCreds: grpc.credentials.createInsecure(), // or any other credentials object.
  servicePath: '0.0.0.0', // overriding the service path.
  port: 8080, // overriding the port.
});

// populate the request.
const formattedName = client.projectPath(projectId);
const request = {
  parent: formattedName,
};

// fetch the list of occurrences.
const [resp] = await client.listOccurrences(request);
console.info(resp);

```



## Samples

Samples are in the [`samples/`](https://github.com/googleapis/nodejs-grafeas/tree/master/samples) directory. The samples' `README.md`
has instructions for running the samples.

| Sample                      | Source Code                       | Try it |
| --------------------------- | --------------------------------- | ------ |
| Quickstart | [source code](https://github.com/googleapis/nodejs-grafeas/blob/master/samples/quickstart.js) | [![Open in Cloud Shell][shell_img]](https://console.cloud.google.com/cloudshell/open?git_repo=https://github.com/googleapis/nodejs-grafeas&page=editor&open_in_editor=samples/quickstart.js,samples/README.md) |



The [Grafeas Node.js Client API Reference][client-docs] documentation
also contains samples.

## Versioning

This library follows [Semantic Versioning](http://semver.org/).


This library is considered to be **General Availability (GA)**. This means it
is stable; the code surface will not change in backwards-incompatible ways
unless absolutely necessary (e.g. because of critical security issues) or with
an extensive deprecation period. Issues and requests against **GA** libraries
are addressed with the highest priority.





More Information: [Google Cloud Platform Launch Stages][launch_stages]

[launch_stages]: https://cloud.google.com/terms/launch-stages

## Contributing

Contributions welcome! See the [Contributing Guide](https://github.com/googleapis/nodejs-grafeas/blob/master/CONTRIBUTING.md).

Please note that this `README.md`, the `samples/README.md`,
and a variety of configuration files in this repository (including `.nycrc` and `tsconfig.json`)
are generated from a central template. To edit one of these files, make an edit
to its template in this
[directory](https://github.com/googleapis/synthtool/tree/master/synthtool/gcp/templates/node_library).

## License

Apache Version 2.0

See [LICENSE](https://github.com/googleapis/nodejs-grafeas/blob/master/LICENSE)

[client-docs]: https://googleapis.dev/nodejs/grafeas/latest
[product-docs]: https://cloud.google.com/container-registry/docs/container-analysis
[shell_img]: https://gstatic.com/cloudssh/images/open-btn.png
[projects]: https://console.cloud.google.com/project
[billing]: https://support.google.com/cloud/answer/6293499#enable-billing
[enable_api]: https://console.cloud.google.com/flows/enableapi?apiid=containeranalysis.googleapis.com
[auth]: https://cloud.google.com/docs/authentication/getting-started
