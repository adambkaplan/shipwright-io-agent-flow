# Shipwright Agent Flow

An agentic AI contribution workflow across the core Shipwright projects. This
repository coordinates AI-assisted development across the Shipwright ecosystem
by providing a unified workspace with all relevant codebases available as git
submodules.

## Repository Layout

```
repos/
├── build/       # github.com/shipwright-io/build
├── cli/         # github.com/shipwright-io/cli
├── community/   # github.com/shipwright-io/community
├── operator/    # github.com/shipwright-io/operator
├── triggers/    # github.com/shipwright-io/triggers
└── website/     # github.com/shipwright-io/website
```

## Cloning

Clone this repository with all submodules initialized in one step:

```bash
git clone --recurse-submodules https://github.com/shipwright-io/agent-flow.git
```

If you already cloned without `--recurse-submodules`, initialize and populate
the submodules afterward:

```bash
git submodule update --init --recursive
```

## Updating Submodules

Pull the latest commits for all submodules at once:

```bash
git submodule update --remote --merge
```

Or update a specific submodule (e.g., `build`):

```bash
git submodule update --remote --merge repos/build
```

## Shipwright Projects

| Submodule | Description |
|-----------|-------------|
| [build](repos/build) | Core build controller and CRD definitions |
| [cli](repos/cli) | `shp` command-line interface |
| [operator](repos/operator) | OLM-based operator for cluster installation |
| [triggers](repos/triggers) | Tekton Triggers integration |
| [website](repos/website) | Documentation site (shipwright.io) |
| [community](repos/community) | Governance, contributing guidelines, and community docs |
