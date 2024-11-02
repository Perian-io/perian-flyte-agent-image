# perian-flyte-agent-image
A Flyte agent docker image that includes the PERIAN agent

## Build and release instructions

The `official` image is based on the agent release performed by the Flyte team, while the `unofficial` version is build by the PERIAN team directly. All features in the `unofficial` image eventually appear in `official` after they are approved by the Flyte team.

Always make sure to use the same image as the agent package and version you're using locally.

### Official

Update the versions used in the Dockerfile if necessary.

```bash
PERIAN_AGENT_VERSION=1.13.12
cd official/
docker build . -t ghcr.io/perian-io/flyte-agent:latest -t ghcr.io/perian-io/flyte-agent:$PERIAN_AGENT_VERSION
docker push ghcr.io/perian-io/flyte-agent --all-tags
```

### Unofficial

```bash
PERIAN_AGENT_VERSION=1.13.13
cd unofficial/
docker build . -t ghcr.io/perian-io/flyte-agent-unofficial:latest -t ghcr.io/perian-io/flyte-agent-unofficial:$PERIAN_AGENT_VERSION
docker push ghcr.io/perian-io/flyte-agent-unofficial --all-tags
```
