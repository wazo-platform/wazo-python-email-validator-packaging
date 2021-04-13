# wazo-python-email-validator-packaging

Debian packaging for [python3-email-validator](https://github.com/JoshData/email-validator/) used in Wazo.

## Reason

* Not packaged by Debian
* Needed by wazo-router-confd and wazo-router-calld

## Upgrading

To upgrade python-email-validator

* Update the version number in the `VERSION` file
* Update the changelog using `dch -i` to the matching version
* Refresh patches
* Push the changes

## Building Locally

To build on a test environment before submitting a change to production the following procedure can be used.

```sh
debian/rules get-orig-source
debuild -us -uc
```
The `.deb` will be located in the parent directory.

