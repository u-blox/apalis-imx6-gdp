# Manifests for the Apalis iMX6 Platform

## Build Setup

Create a working directory for the build and clone the source repositories.

```shell
$ mkdir apalis-imx6-gdp
$ cd apalis-imx6-gdp
$ repo init -u https://github.com/u-blox/apalis-imx6-gdp.git -m MANIFEST [-b BRANCH]
$ repo sync
```

Where

* `MANIFEST` is the desired repo manifest file, e.g. `yocto-rocko`
* `BRANCH` is the branch that contains the manifest, e.g. `cohda-gdp`. This technique may be used to retrieve development versions of the manifest.


## Initialize the Build Environment

Load the shell script `ublox-init-build-env` in order to prepare the build environment as well as necessary configuration files under `build/`.

```shell
$ source ublox-init-build-env [-m MACHINE]
```

Where

* `MACHINE` identifies the target hardware, e.g. `apalis-imx6-gdp`.


## Start the Build Process

```shell
$ bitbake ublox-gdp-base-image
```


## References

* https://developer.toradex.com/products/apalis-imx6
