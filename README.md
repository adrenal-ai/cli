# Adrenal CLI

Sync local files to [Adrenal](https://adrenal.ai) DataHub from your terminal.

## Install

```sh
curl -fsSL https://adrenal.ai/cli/install.sh | sh
```

Supports macOS (Apple Silicon & Intel), Linux, and Windows.

## Usage

```sh
# Authenticate (opens browser)
adrenal login

# Sync a folder
adrenal sync ~/documents

# Sync to a specific connection
adrenal sync ./proposals -c <connection-id>

# List your connections
adrenal connections
```

## Setup

1. Go to [adrenal.ai/datahub/connections/new](https://adrenal.ai/datahub/connections/new) and create a **Local Files** connection
2. Run `adrenal login` — your browser opens to generate a token automatically
3. Run `adrenal sync <path>`

Files are deduplicated by checksum — unchanged files are skipped on re-sync.

## Commands

| Command | Description |
|---------|-------------|
| `adrenal login` | Open browser to authenticate |
| `adrenal logout` | Remove stored credentials |
| `adrenal connections` | List your CLI connections |
| `adrenal sync <path>` | Sync files to DataHub |
| `adrenal version` | Show version |
| `adrenal help` | Show help |
