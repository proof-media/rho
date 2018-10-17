
# rholang @proof

Experiments on the [RChain blockchain](https://www.rchain.coop/platform) writing [rholang](https://developer.rchain.coop/tutorial/) contracts.

## tested versions

### voting

Voting has been tested with:
- RNode [`v0.6.4`](https://hub.docker.com/r/rchain/rnode/tags/)
- Release [`0.0.10`](https://github.com/proof-media/rchain-grpc/releases) of our gRPC API for Python

And in official live zoom session with:
- RNode [`v0.7.1`](https://hub.docker.com/r/rchain/rnode/tags/)
- Compose settings (see [our gitlab repo](https://gitlab.proofmediadev.com/open-source/rchain-testnode#instructions))

### registry

Tested only in standalone mode of latest rnode `v0.7.1`.

`::TO BE COMPLETED::`

NOTE: as of 17/10/2018 the `dev` docker tag image doesn't work while `testing` does.

```bash
# using compose in rchain-notebook
# $ docker-compose exec rnode bash

rnode deploy --phlo-limit 100000000 --phlo-price 1 \
    /opt/contracts/registry/registry-server.rho \
    && rnode deploy --phlo-limit 100000000 --phlo-price 1 \
    /opt/contracts/registry/registry-client.rho \
    && rnode propose

```


