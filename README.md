# Helix Configuration

My configuration for the [Helix editor][website].

## Clone

### Linux and macOS

```bash
git clone https://github.com/heaths/helix ~/.config/helix
```

### Windows

```powershell
git clone 'https://github.com/heaths/helix' $env:APPDATA/helix
```

## Installation

See [Installing Helix](https://docs.helix-editor.com/install.html) for more options.

### Ubuntu

```bash
sudo add-apt-repository ppa:maveonair/helix-editor
sudo apt update
sudo apt install helix
```

### Windows

```bash
winget install -e Helix.Helix
```

### macOS

```bash
brew install helix
```

## Language Support

See [Language Server Configurations](https://github.com/helix-editor/helix/wiki/Language-Server-Configurations) for more options.

### Bash

```bash
npm i -g bash-language-server
```

### Bicep

[Install .NET](https://dot.net/download) for your platform.

```bash
gh -R Azure/bicep release download -p bicep-langserver.zip -O ~/Downloads/bicep-langserver.zip
unzip -d ~/.cache/bicep-langserver ~/Downloads/bicep-langserver.zip
echo << 'EOF' > ~/.local/bin/bicep-langserver
#!/usr/bin/env bash
dotnet ~/.cache/bicep-langserver/Bicep.LangServer.dll
EOF
chmod +x ~/.local/bin/bicep-langserver
```

### Docker

```bash
npm install -g dockerfile-language-server-nodejs   # Docker
npm install -g @microsoft/compose-language-service # Docker Compose
```

### GraphQL

```bash
npm i -g graphql-language-service-cli
```

### Go

```bash
go install golang.org/x/tools/gopls@latest                     # LSP
go install github.com/nametake/golangci-lint-langserver@latest # LSP
go install github.com/go-delve/delve/cmd/dlv@latest            # Debugger
go install golang.org/x/tools/cmd/goimports@latest             # Formatter
```

### HTML

```bash
npm i -g vscode-langservers-extracted
```

### JavaScript

See [TypeScript](#typescript).

### JSON

```bash
npm i -g vscode-langservers-extracted
```

### Markdown

Using [Marksman](https://github.com/artempyanykh/marksman):

#### Linux and macOS

```bash
brew install marksman
```

#### Windows

```bash
scoop install marksman
```

### Python

```bash
npm install -g pyright
```

### Rust

```bash
rustup component add clippy rust-analyzer
```

### TOML

```bash
cargo install taplo-cli --locked --features lsp
```

### TypeScript

```bash
npm install -g typescript typescript-language-server
```

### TypeSpec

```bash
npm install -g @typespec/compiler
hx -g fetch
hx -g build
```

### YAML

```bash
npm i -g yaml-language-server@next
```

[docs]: https://docs.helix-editor.com/
[website]: https://helix-editor.com/
