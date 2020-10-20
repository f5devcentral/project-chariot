# project-chariot

Project to explore a programatic way to interface with charon/ACC.

This project is currently private.

&nbsp;

---

&nbsp;

## Overview

Charon or (A)S3 (C)onfiguration (C)onverter is solving a huge need to help bring our customers from legacy tmos application configs to AS3

The current solution requires the use of local docker.  This is a good first step that keeps the tool in a nice single package.

I have found that running the container is easily described in the documenation but harder to implmenet in reality due to the following:
    - host system variances (mac, windows, linux)
        - file system differences
    - Windows users running VMWare Workstation are not able to run local docker

Seems that volume mounting is the difficult piece and can really hold back any potential users with little to no docker experience.

The intent here is to wrap the ACC tool in another docker container that will provide a full api that can be run as a service.  This will further abstract it's process and allow for more programatic(api) interfacing like the vscode-f5-chariot extension (which provides a workspace for extracting applications, interacting and posting as3 declarations)

&nbsp;

> this is all assuming we cannot get it released as an rpm and intagrate directly

&nbsp;

---

&nbsp;

## Architecture

&nbsp;

---

&nbsp;

## Getting Started

Provide a quick example of how to use your code.  This should provide the user with a launch point to quickly see what the project can offer them. 

&nbsp;

---

&nbsp;

## Installation

Installation should included cloning the repo, starting the docker container, import ACC, convert configurations.

&nbsp;

---

&nbsp;

## Usage

Once the container is up and running, a webpage should be available to show the user the status of the tool, like needing to upload an ACC archive to load the charon tool into this tool.

If the local docker image is available the page should display an input box to paste config, with a button to convert. Clicking the button should provide converted output below.  This page should also include output from the execution of the output and any additional logging

The web page should be driven by API, so any interactions done in the page should be avaible programatically

&nbsp;

---

&nbsp;

## Development

Looking to develop this with PS resources.

This tool will be developed using:
- nodejs v12-lts
- TypeScript v4.x

Looking to utilize KOA for api framework
- https://koajs.com/
- https://www.npmjs.com/package/koa
- https://github.com/koajs/koa

Would like to document api with Swagger 3.0
Node tests with mocha?
test coverage with istanbul (nyc)

&nbsp;

---

&nbsp;

## Support

For support, please open a GitHub issue.  Note, the code in this repository is community supported and is not supported by F5 Networks.  For a complete list of supported projects please reference [SUPPORT.md](SUPPORT.md).

&nbsp;

---

&nbsp;

## Community Code of Conduct
Please refer to the [F5 DevCentral Community Code of Conduct](code_of_conduct.md).

&nbsp;

---

&nbsp;

## License
[Apache License 2.0](LICENSE)

&nbsp;

---
&nbsp;

## Copyright
Copyright 2014-2020 F5 Networks Inc.

&nbsp;

---

&nbsp;

### F5 Networks Contributor License Agreement

Before you start contributing to any project sponsored by F5 Networks, Inc. (F5) on GitHub, you will need to sign a Contributor License Agreement (CLA).

If you are signing as an individual, we recommend that you talk to your employer (if applicable) before signing the CLA since some employment agreements may have restrictions on your contributions to other projects.
Otherwise by submitting a CLA you represent that you are legally entitled to grant the licenses recited therein.

If your employer has rights to intellectual property that you create, such as your contributions, you represent that you have received permission to make contributions on behalf of that employer, that your employer has waived such rights for your contributions, or that your employer has executed a separate CLA with F5.

If you are signing on behalf of a company, you represent that you are legally entitled to grant the license recited therein.
You represent further that each employee of the entity that submits contributions is authorized to submit such contributions on behalf of the entity pursuant to the CLA.