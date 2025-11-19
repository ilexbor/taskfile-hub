<div align="center">
<h1 style="color:#027DFD; font-family: 'Courier New', 'Courier', monospace; font-weight: 200;">{ TASKFILE HUB }</h1>
</div>

A comprehensive collection of reusable and modular Taskfile configurations designed for managing complex monorepo projects across multiple technology stacks.

## Features

- 🎯 **Pre-configured tasks** for Dart, Flutter, Node.js, Python, and Docker
- 🔄 **Interactive package selection** with beautiful TUI
- 🚀 **Monorepo support** with Melos and npm workspaces
- 🛠️ **Tool integrations**: ESLint, Prettier, Ruff, TSC, build_runner, and more
- 📦 **Dependency management** across all supported platforms
- 🎨 **Consistent interface** across different technology stacks
- ⚡ **Cross-platform** bash scripts with proper error handling

## Requirements

- [Task](https://taskfile.dev/) - Task runner
- [gum](https://github.com/charmbracelet/gum) - Terminal UI components
- [jq](https://stedolan.github.io/jq/) - JSON processor

## Installation

### Quick Start: Include all taskfiles

Include the main Taskfile to get access to all available tasks:

```yaml
version: '3'

includes:
  taskfile-hub:
    taskfile: https://raw.githubusercontent.com/ilexbor/taskfile-hub/main/Taskfile.yml
    flatten: true
```

Now you can see all available tasks:
```bash
task -l
```

### Include only specific taskfiles

Or include only the taskfiles you need directly:

```yaml
version: '3'

includes:
  dart:
    taskfile: https://raw.githubusercontent.com/ilexbor/taskfile-hub/main/Taskfile.dart.yml
  docker:
    taskfile: https://raw.githubusercontent.com/ilexbor/taskfile-hub/main/Taskfile.docker.yml
  flutter:
    taskfile: https://raw.githubusercontent.com/ilexbor/taskfile-hub/main/Taskfile.flutter.yml
  npm:
    taskfile: https://raw.githubusercontent.com/ilexbor/taskfile-hub/main/Taskfile.npm.yml
  python:
    taskfile: https://raw.githubusercontent.com/ilexbor/taskfile-hub/main/Taskfile.python.yml
  # Add other taskfiles as needed
```

## Supported tools

### Dart/Flutter
- **Taskfile.dart.yml** - Dart fix and format
- **Taskfile.flutter.yml** - Flutter analyze, test, and coverage
- **Taskfile.pub.yml** - Dart/Flutter dependency management
- **Taskfile.build-runner.yml** - Code generation with build_runner
- **Taskfile.melos.yml** - Monorepo management

### Node.js/TypeScript
- **Taskfile.npm.yml** - npm dependency management and workspace operations
- **Taskfile.nodejs.yml** - Node.js execution
- **Taskfile.tsc.yml** - TypeScript compilation and type checking
- **Taskfile.tsx.yml** - TypeScript execution with hot reload
- **Taskfile.eslint.yml** - ESLint linting
- **Taskfile.prettier.yml** - Code formatting
- **Taskfile.better-auth.yml** - Better Auth schema and migrations

### Python
- **Taskfile.python.yml** - Python package management
- **Taskfile.ruff.yml** - Ruff linting and formatting
- **Taskfile.pytype.yml** - Type checking

### Docker
- **Taskfile.docker.yml** - Docker Compose operations

### DevOps & Utilities
- **Taskfile.env.yml** - Environment management (with SOPS support)
- **Taskfile.workspace.yml** - Workspace cleaning
- **Taskfile.brew.yml** - Homebrew package installation

### Core Utilities
- **Taskfile.shell.yml** - Core execution engine for running commands in packages
- **Taskfile.paths.yml** - Path normalization and filtering utilities
- **Taskfile.tui.yml** - Terminal UI components (spinners, messages, selection)
- **Taskfile.zsh.yml** - Shell command execution

## Variables

Common variables across taskfiles:

- `SPINNER_TITLE` - Custom spinner title
- `STDOUT` - Show/hide stdout (`true`/`false`)
- `STDERR` - Show/hide stderr (`true`/`false`)
- `SCOPE` - Filter packages by path pattern
- `USER_WORKING_DIR` - Working directory (auto-set)
- `ROOT_DIR` - Root directory (auto-set)

## Changelog

For a full list of changes and updates, see the [CHANGELOG.md](CHANGELOG.md).

## Issues

If you encounter any issues or have suggestions for improvements, please [create an issue](https://github.com/ilexbor/taskfile-hub/issues/new/choose) on GitHub.

When reporting a bug or requesting a fix, please provide as much detail as possible to help understand the problem or idea.

Including the following information is highly appreciated:
- Steps to reproduce the issue
- Expected behavior
- Any error messages or logs
- Your environment (operating system, Dart version, etc.)

Your feedback is valuable and will help improve the package!

## Contributing

Contributions are welcome!  
Please [fork this repository](https://github.com/ilexbor/taskfile-hub/fork) and [submit pull requests](https://github.com/ilexbor/taskfile-hub/pulls).

By participating in this project, you agree to abide by our [Code of Conduct](CODE_OF_CONDUCT.md).

## License

This project is licensed under the [BSD-3-Clause License](LICENSE).

## Acknowledgments

- [Task](https://taskfile.dev/) - Amazing task runner
- [gum](https://github.com/charmbracelet/gum) - Beautiful terminal UI components
- [jq](https://stedolan.github.io/jq/) - Command-line JSON processor
- [Melos](https://melos.invertase.dev/) - Monorepo management for Dart

---

<div align="center">
  <h2 style="color:#0553B1;">
    Developed with 💙 by <a href="https://github.com/ilexbor" style="text-decoration:none; color:#027DFD;" onmouseover="this.style.color='#0553B1'" onmouseout="this.style.color='#027DFD'">ilexbor</a>
  </h2>
</div>