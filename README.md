[//]: # "This README.md file is auto-generated, all changes to this file will be lost."
[//]: # "To regenerate it, use `python -m synthtool`."
<img src="https://avatars2.githubusercontent.com/u/2810941?v=3&s=96" alt="Google Cloud Platform logo" title="Google Cloud Platform" align="right" height="96" width="96"/>

# [Grafeas: Node.js Client](https://github.com/googleapis/nodejs-grafeas)


[![npm version](https://img.shields.io/npm/v/@google-cloud/grafeas.svg)](https://www.npmjs.org/package/@google-cloud/grafeas)
[![codecov](https://img.shields.io/codecov/c/github/googleapis/nodejs-grafeas/main.svg?style=flat)](https://codecov.io/gh/googleapis/nodejs-grafeas)




A [Grafeas API Client](https://grafeas.io/) compatible with Google Cloud's
[Container Analysis API](https://cloud.google.com/container-registry/docs/container-analysis).


A comprehensive list of changes in each version may be found in
[the CHANGELOG](https://github.com/googleapis/nodejs-grafeas/blob/main/CHANGELOG.md).

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

Samples are in the [`samples/`](https://github.com/googleapis/nodejs-grafeas/tree/main/samples) directory. Each sample's `README.md` has instructions for running its sample.

| Sample                      | Source Code                       | Try it |
| --------------------------- | --------------------------------- | ------ |
| Quickstart | [source code](https://github.com/googleapis/nodejs-grafeas/blob/main/samples/quickstart.js) | [![Open in Cloud Shell][shell_img]](https://console.cloud.google.com/cloudshell/open?git_repo=https://github.com/googleapis/nodejs-grafeas&page=editor&open_in_editor=samples/quickstart.js,samples/README.md) |



The [Grafeas Node.js Client API Reference][client-docs] documentation
also contains samples.

## Supported Node.js Versions

Our client libraries follow the [Node.js release schedule](https://nodejs.org/en/about/releases/).
Libraries are compatible with all current _active_ and _maintenance_ versions of
Node.js.

Client libraries targeting some end-of-life versions of Node.js are available, and
can be installed via npm [dist-tags](https://docs.npmjs.com/cli/dist-tag).
The dist-tags follow the naming convention `legacy-(version)`.

_Legacy Node.js versions are supported as a best effort:_

* Legacy versions will not be tested in continuous integration.
* Some security patches may not be able to be backported.
* Dependencies will not be kept up-to-date, and features will not be backported.

#### Legacy tags available

* `legacy-8`: install client libraries from this dist-tag for versions
  compatible with Node.js 8.

## Versioning

This library follows [Semantic Versioning](http://semver.org/).








More Information: [Google Cloud Platform Launch Stages][launch_stages]

[launch_stages]: https://cloud.google.com/terms/launch-stages

## Contributing

Contributions welcome! See the [Contributing Guide](https://github.com/googleapis/nodejs-grafeas/blob/main/CONTRIBUTING.md).

Please note that this `README.md`, the `samples/README.md`,
and a variety of configuration files in this repository (including `.nycrc` and `tsconfig.json`)
are generated from a central template. To edit one of these files, make an edit
to its templates in
[directory](https://github.com/googleapis/synthtool).

## License

Apache Version 2.0

See [LICENSE](https://github.com/googleapis/nodejs-grafeas/blob/main/LICENSE)

[client-docs]: https://cloud.google.com/nodejs/docs/reference/grafeas/latest
[product-docs]: https://cloud.google.com/container-registry/docs/container-analysis
[shell_img]: https://gstatic.com/cloudssh/images/open-btn.png
[projects]: https://console.cloud.google.com/project
[billing]: https://support.google.com/cloud/answer/6293499#enable-billing
[enable_api]: https://console.cloud.google.com/flows/enableapi?apiid=containeranalysis.googleapis.com
[auth]: https://cloud.google.com/docs/authentication/getting-started
