This is a fork of [garethr/docker](gitlab.com/garethr/garethr-docker).

For help you should go there first.

# Changes

## Registry Mirror

A registry mirror can be specified in the options using the `docker` class
parameter `$registry_mirror`.

## Image and run dependency

I have untangled the dependency between all images and containers
(`docker::run`), now only each `run` resource depends on its corresponding
image. The main difference is that the `$image` parameter to `docker::run`
must be the plain image name without the tag, and the `$image_tag` parameter
must be specified if running with an image tag is desired.

# Branches

The patches are in separate branches. See the `patches` branch for all the
patches applied and kept reasonably up to date with upstream. See other
branches for patches.
