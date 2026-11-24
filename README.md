
# Vittesh — Command Reference

> Vitte Foundation Shell — Voyager_49

![Version](https://img.shields.io/badge/version-0.1.0-blue)
![Language](https://img.shields.io/badge/language-Vitte-purple)
![Status](https://img.shields.io/badge/status-development-orange)

## Overview

Vittesh is a next-generation system shell designed around:

- Typed objects and structured data.
- Logical spaces and object references.
- Transactional system operations.
- Capability-based security.
- Native activity management.
- Cross-platform executable compatibility.
- Integration with Voyager_49.
- Native implementation in Vitte.

## Table of Contents

- [Native Syntax](#native-syntax)
- [Space Commands](#space-commands)
- [Object Commands](#object-commands)
- [Activity Commands](#activity-commands)
- [System Commands](#system-commands)
- [Network Commands](#network-commands)
- [Transaction Commands](#transaction-commands)
- [Typed Pipelines](#typed-pipelines)
- [VEX Compatibility](#vex-compatibility)
- [Reserved References](#reserved-references)
- [Security](#security)
- [Implementation Status](#implementation-status)

## Native Syntax

```text
command target :attribute = value
```

| Symbol | Description |
|--------|-------------|
| `@` | Object or space reference |
| `:` | Named attribute |
| `=` | Attribute assignment |
| `=>` | Typed pipeline |
| `?` | Property query |
| `{ }` | Instruction block |
| `[ ]` | Collection |

## Space Commands

| Command | Description |
|---------|-------------|
| `orya` | Observe a logical space |
| `nelya` | Change the active space |
| `kyora` | Create an isolated space |
| `ovely` | Establish object relationships |

### Examples

```text
orya @here
nelya @projects
kyora "workspace" :isolated
ovely @workspace @sources
```

## Object Commands

| Command | Description |
|---------|-------------|
| `avora` | Instantiate an object |
| `elyra` | Inspect object properties |
| `vyora` | Transform an object |
| `zerya` | Remove an object from its active space |
| `aevra` | Restore a previous revision |

### Examples

```text
avora source "main.vit" @here
elyra @main
vyora @main :name = "kernel.vit"
zerya @temporary
aevra @main :revision = 1
```

## Activity Commands

| Command | Description |
|---------|-------------|
| `ivora` | Start an activity |
| `syora` | Observe running activities |
| `nevra` | Suspend an activity |
| `alvya` | Resume an activity |
| `dorya` | Terminate an activity |
| `ryven` | Adjust activity resources |

### Examples

```text
ivora @compiler :args = ["main.vit"]
syora @system
nevra @compiler
alvya @compiler
ryven @compiler :memory = 256MiB
dorya @compiler
```

## System Commands

| Command | Description |
|---------|-------------|
| `veora` | Inspect system state |
| `myora` | Observe memory resources |
| `uvora` | Inspect hardware devices |
| `kerya` | Inspect available capabilities |
| `orvya` | Observe system events |

### Examples

```text
veora @system
myora @system
uvora @devices
kerya @session
orvya @system
```

## Network Commands

| Command | Description |
|---------|-------------|
| `arvya` | Observe network interfaces |
| `elyon` | Inspect network connections |
| `navora` | Establish a communication channel |

### Examples

```text
arvya @network
elyon @connections
navora @remote :protocol = "tcp"
```

## Transaction Commands

| Command | Description |
|---------|-------------|
| `kyora` | Open a transactional space |
| `tyvra` | Validate and commit a transaction |
| `aevra` | Restore a previous persistent state |

### Example

```text
kyora "update" :transaction {
    vyora @main :name = "main_old.vit"
    avora source "main.vit" @project
    tyvra @update
}
```

Transactions apply only to resources managed by the
Vittesh transaction engine.

External side effects are not automatically reversible.

## Typed Pipelines

Vittesh pipelines transfer structured objects instead
of exclusively transferring raw byte streams.

| Operation | Description |
|-----------|-------------|
| `filter` | Select matching objects |
| `order` | Sort objects by property |
| `decode` | Decode external data |
| `orya` | Render structured results |

### Example

```text
syora @system
    => filter :memory > 128MiB
    => order :memory :desc
    => orya
```

## VEX Compatibility

VEX stands for **Vitte Execution Exchange**.

VEX provides an explicit execution interface for
traditional programs and external interpreters.

### Unix

```text
vex unix "git" :args = ["status"]
```

### Linux

```text
vex linux "gcc" :args = ["main.c", "-o", "main"]
```

### Windows

```text
vex windows "notepad.exe"
```

### Bash

```text
vex bash {
    echo "Hello from Bash"
    ls -la
}
```

Executable compatibility depends on the host operating
system, processor architecture, executable format,
available libraries and supported ABI.

## Reserved References

| Reference | Description |
|-----------|-------------|
| `@here` | Current logical space |
| `@origin` | Initial session space |
| `@system` | System namespace |
| `@session` | Current session |
| `@user` | Current user context |
| `@network` | Network namespace |
| `@devices` | Hardware namespace |
| `@connections` | Active network connections |

## Security

Vittesh uses an explicit capability-based security model.

### Capability Namespaces

```text
object.read
object.create
object.modify
object.remove

space.create
space.navigate

activity.start
activity.control

system.inspect
network.connect

transaction.commit
external.execute
```

Capabilities must be enforced by the runtime and
supported by the underlying operating system.

## Architecture

```text
Vittesh
├── Core
├── Lexer
├── Parser
├── Semantic Engine
├── Runtime
├── REPL
├── Object Registry
├── Native Commands
├── Typed Streams
├── Transaction Engine
├── Security Engine
├── VEX
├── Platform Abstraction
└── Diagnostics
```

## Implementation Status

| Component | Status |
|-----------|--------|
| Native command vocabulary | Designed |
| Command grammar | Draft |
| Lexer | Planned |
| Parser | Planned |
| REPL | Planned |
| Native command execution | Planned |
| Object registry | Planned |
| Typed pipelines | Planned |
| Transaction engine | Planned |
| Capability enforcement | Planned |
| POSIX compatibility | Planned |
| Windows compatibility | Planned |
| Voyager_49 integration | Planned |

## Project Philosophy

Vittesh is not intended to reproduce traditional Unix
commands under different names.

Its purpose is to establish a native system interaction
model based on objects, spaces, activities, capabilities,
transactions and explicit execution.

## Ecosystem

- Vitte Programming Language
- Vitte Foundation Distribution
- Voyager_49 Operating System
- Vittesh
- Vitte Execution Exchange

## Contributing

Contributions, architectural proposals, bug reports,
documentation and compatibility improvements are welcome.

See [CONTRIBUTING.md](CONTRIBUTING.md) for details.

## Security Policy

See [SECURITY.md](SECURITY.md) for vulnerability reporting.

## License

See [LICENSE](LICENSE) for licensing information.

---

**Vittesh — Vitte Foundation Shell**

Designed for the Vitte ecosystem.
