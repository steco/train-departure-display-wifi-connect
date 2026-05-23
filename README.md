# Summary

A multi-container project which adds [wifi-connect](https://github.com/balena-os/wifi-connect) to [train-departure-display](https://github.com/chrisys/train-departure-display)

# Implementation Details

## Train Departure Display

[train-departure-display](https://github.com/chrisys/train-departure-display) is pulled into this repo using [git submodules](https://git-scm.com/book/en/v2/Git-Tools-Submodules).

When cloning this repo, use the `--recursive` flag to pull down the submodules:
```
git clone --recursive https://github.com/steco/train-departure-display-wifi-connect.git
```

To update to the latest version of train-departure-display:

```
git submodule update --remote --merge
```

## Wifi Connect

For Wifi Connect, the installation is all handled in [Dockerfile.template](wifi-connect/Dockerfile.template) which is copied
into this project.  Any changes in the [WiFi Connect](https://github.com/balena-os/wifi-connect/blob/master/Dockerfile.template)
project will need to be manually copied across to here.
