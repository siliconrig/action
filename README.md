# flashbay-action

GitHub Action for [Flashbay](https://flashbay.dev) hardware-in-the-loop CI/CD.

Thin wrapper that installs the [fbay-cli](https://github.com/flashbay-dev/fbay-cli) and runs it within your GitHub Actions workflow.

**Status:** Scaffold only — not yet functional.

## Usage

```yaml
- uses: flashbay-dev/flashbay-action@v1
  with:
    api-key: ${{ secrets.FLASHBAY_API_KEY }}
    board: esp32-s3
    firmware: build/firmware.bin
    command: flash-and-test
```

## Inputs

| Input | Required | Description |
|---|---|---|
| `api-key` | Yes | Flashbay API key |
| `board` | Yes | Board type (e.g., `esp32-s3`) |
| `firmware` | No | Path to firmware binary |
| `command` | No | CLI command to run (default: `flash-and-test`) |
