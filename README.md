# Minimal reproducer for https://github.com/renovatebot/renovate/discussions/40275
## Current behavior

The update of fluxcd controller components fail.

The error happens when the version of fluxcd is updated as part of the `updateArtifacts` phase and produces the following error:

    ✗ unknown command ">" for "flux install"

To observe the error run with the following options:

    docker run --rm -ti -e LOG_LEVEL=debug -e RENOVATE_TOKEN=<replace> -e GITHUB_COM_TOKEN=<replace> -v $PWD:/work -w /work renovate/renovate:42.72.0 --dry-run=full --autodiscover=true --autodiscover-filter=agriessbosch/renovate-repro-40302

## Expected behavior

Update of fluxcd controller components succeed

## Link to the Renovate issue or Discussion

https://github.com/renovatebot/renovate/discussions/40275
