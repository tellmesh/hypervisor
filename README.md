# hypervisor

TellMesh control plane — contract registry, domain packs, deployment registry, routing and CLI.

Extracted from [tellmesh/resource-agent-hypervisor](https://github.com/tellmesh/resource-agent-hypervisor).

```text
hypervisor -> policy, lifecycle, deployment, audit, describe-agent
uri2ops    -> operator execution (does NOT click/type for you)
uri3       -> URI resolve, workflow graphs
```

**Rule:** Hypervisor approves, deploys and monitors agents. It does not execute browser/OS/robot actions — that is `uri2ops`.

## Install

```bash
uv sync
# or: pip install -e .
```

## CLI quickstart

```bash
hypervisor --help
hypervisor deployments
hypervisor describe-agent weather-map-agent.local
hypervisor run-agent weather-map-agent.local --detach --if-running reuse
hypervisor inspect-agent browser-operator.local
hypervisor replay-failure check-agent-health --create-test tests/replay/test_check_agent_health.py
```

## Monorepo umbrella

Agents, domains, examples: [`../tellmesh/`](../tellmesh/).

| Example | Path |
|---------|------|
| Run agent | [`tellmesh/examples/09_run_agent_hypervisor`](../tellmesh/examples/09_run_agent_hypervisor) |
| Autonomous agents | [`tellmesh/examples/38_autonomous_agents`](../tellmesh/examples/38_autonomous_agents) |
| Golden path | [`tellmesh/examples/30_golden_path`](../tellmesh/examples/30_golden_path) |

## Links

- [TODO](TODO.md)
- [resource-agent-hypervisor](../resource-agent-hypervisor)
- [hypervisor-dashboard](../hypervisor-dashboard)
- Org status: [`../TODO_STATUS.md`](../TODO_STATUS.md)

## License

Licensed under Apache-2.0.
