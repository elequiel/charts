# Description

See image content on [Docker Hub](https://hub.docker.com/r/elequiel/adoagent)
# Usage
## Requirements
- ADO Organization and project
- Generate PAT
  
## Optional
- Create agent group


# Deploy

```bash
helm upgrade --install helm-adoagent -n adoagent . \
	--set image.repository=elequiel/adoagent \
	--set image.tag=1.0 \
	--set configMap.AZP_POOL=containered-agent-pool \
	--set configMap.AZP_URL=https://dev.azure.com/zeksantos \
	--set configMap.AZP_AGENT_NAME=helm-ado-agent-01 \
	--set secret.AZP_TOKEN=$PAT
```