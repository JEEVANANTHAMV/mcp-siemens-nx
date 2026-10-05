# Siemens NX

> Automates Siemens NX 3D CAD — parts, sketches, features, assemblies, and drawings — through this assistant. Needs Siemens NX installed, with its companion bridge app running.

The bundle zip (**62.6 MB**) is stored in this repository at **`a392f659-00a5-4da5-9d46-39adc0c17ee4.zip`**.

This repository is part of the **Forjinn-Desk** MCP bundle collection. An MCP bundle is a self-contained server that a host application launches and communicates with over the MCP (Model Context Protocol) protocol.

## Repo metadata

| Field | Value |
| --- | --- |
| Registry ID | `a392f659-00a5-4da5-9d46-39adc0c17ee4` |
| Status in registry | active |
| Bundle size | 62.6 MB |
| Distribution | committed to this repo |

## Environment variables

| Variable | Value / note |
| --- | --- |
| `NX_MCP_WORKSPACE` | `__INSTALL_DIR__` |
| `NX_MCP_ENABLE_EXPERIMENTAL` | `1` |
| `NX_MCP_ENABLE_JOURNAL` | `1` |

## MCP launch configuration

The host replaces `__INSTALL_DIR__` (install dir) and `__PYTHON__` (bundled Python) at runtime.

```json
{
  "command": "__PYTHON__",
  "args": [
    "-m",
    "nx_mcp.server"
  ],
  "env": {
    "NX_MCP_WORKSPACE": "__INSTALL_DIR__",
    "NX_MCP_ENABLE_EXPERIMENTAL": "1",
    "NX_MCP_ENABLE_JOURNAL": "1",
    "PYTHONPATH": "__INSTALL_DIR__"
  }
}
```


## Install / usage

1. Get the bundle:
   - download `a392f659-00a5-4da5-9d46-39adc0c17ee4.zip` from this repo (Code → Download ZIP, or `git clone`).
2. Extract to your target installation directory (config paths expect contents at the install-dir root).
3. Set the environment variables listed above.
4. Launch using the MCP config JSON (or let a host client manage it automatically).

> Bundles may include vendored runtimes (bundled Python, Node, or native executables). Builds are Windows x64.
