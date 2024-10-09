# k6i2n

**Custom k6 distribution with Iván Szkiba's k6 extensions**

This custom k6 distribution contains the k6 extensions created by [Iván Szkiba](https://github.com/szkiba). Some of them have become official Grafana k6 extensions and have been transferred to the [`grafana`](https://github.com/grafana) GitHub organization.

Check the [latest release](https://github.com/szkiba/k6i2n/releases/latest) for a list of included extension versions.

## Usage

Just use the k6 executable from the distribution to try out the included extensions.

## Download

The releases can be downloaded from the [Releases](https://github.com/szkiba/k6i2n/releases) page.

Docker images created from releases are available on the [Packages](https://github.com/szkiba/k6i2n/pkgs/container/k6i2n) page. Images with the `-with-browser` label suffix include a browser for browser-based tests.

## Contents

The distribution includes the following extensions that are maintained up to date.

Name | Description
-----|------------
[xk6-dashboard](https://github.com/grafana/xk6-dashboard)|Create a web-based metrics dashboard
[xk6-faker](https://github.com/grafana/xk6-faker)|Generate random fake data
[xk6-prometheus](https://github.com/szkiba/xk6-prometheus)|Prometheus HTTP exporter for k6
[xk6-top](https://github.com/szkiba/xk6-top)|Updating the current k6 metrics summaries on the terminal during the test run
[xk6-dotenv](https://github.com/szkiba/xk6-dotenv)|Load env vars from a .env file
[xk6-ts](https://github.com/github.com/grafana/xk6-ts)|Add TypeScript support for k6
[xk6-output-plugin](https://github.com/szkiba/xk6-output-plugin)|Dynamic output extension using your favorite programming language
[xk6-cache](https://github.com/szkiba/xk6-cache)|Enable vendoring remote HTTP modules to a single source-control-friendly file
[xk6-csv](https://github.com/szkiba/xk6-csv)|Parse CSV values
[xk6-toml](https://github.com/szkiba/xk6-toml)|Encode and decode TOML values
[xk6-yaml](https://github.com/szkiba/xk6-yaml)|Encode and decode YAML values
[xk6-banner](https://gitlab.com/szkiba/xk6-banner)|Print ASCII art banner from k6 test
[xk6-ansible-vault](https://github.com/szkiba/xk6-ansible-vault)|Encrypt and decrypt Ansible Vault

## Needs attention

Some k6 extensions that cannot be built with the latest k6 version therefore require some attention.

These extensions are temporarily not included in the distribution.

Name | Description
-----|------------
[xk6-g0](https://github.com/szkiba/xk6-g0)|Write k6 tests in golang
[xk6-chai](https://github.com/szkiba/xk6-chai)|Embed k6chaijs into the k6 binary
[xk6-mock](https://github.com/szkiba/xk6-mock)|Mock HTTP(S) servers

## Deprecated

In the meantime, some extension functionalities were also implemented in k6, so they became deprecated.

These extensions will no longer be included in the distribution.

Name | Description
-----|------------
[xk6-jose](https://github.com/szkiba/xk6-jose)|Javascript Object Signing and Encryption (JOSE) support
[xk6-crypto](https://github.com/szkiba/xk6-crypto)|Extended crypto functions

## How it Works

A new release is made if a new version of k6 or one or more of the extensions has been released since the last distribution release. This check runs every two hours.

The semantic version of the distribution will be generated as follows:

- if the major version of any module (k6 or extension) is bumped or a module is removed, the major version will be bumped (potential breaking change)

- if the minor version of any module (k6 or extension) is bumped or a new module is added, the minor version will be bumped (backward compatible feature change)

- otherwise, the patch version will be bumped