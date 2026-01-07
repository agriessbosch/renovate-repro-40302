To observe the error run with the following options:

    docker run --rm -ti -e LOG_LEVEL=debug -e RENOVATE_TOKEN=<replace> -e GITHUB_COM_TOKEN=<replace> -v $PWD:/work -w /work renovate/renovate:42.72.0 --dry-run=full --autodiscover=true --autodiscover-filter=agriessbosch/renovate-repro-40302
