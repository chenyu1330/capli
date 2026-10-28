# Capli

**Real screenshots for agent-written documentation.**

Capli (Capture + CLI) is a planned Windows and macOS command-line tool that helps AI agents capture real application screenshots and hand them off to documentation workflows.

[简体中文](README.zh-CN.md) · [Requirements draft](docs/requirements.md)

## Status

**Requirements and design stage.** There is no runnable application or release yet. Features below describe the proposed direction, not existing capabilities.

## The workflow

1. Discover the intended application window.
2. Capture it to a local image with structured metadata.
3. Let the calling agent inspect the image and confirm its content.
4. Prepare the image for documentation, with optional cropping and annotations.
5. Hand the artifact to the agent's document editor or generate an image reference.

## Proposed scope

- A consistent CLI for Windows and macOS.
- Explicit window targets and clearly defined capture coordinates.
- Structured JSON output, stable error codes and environment diagnostics.
- Local image artifacts with source and capture metadata.
- Documentation-oriented examples and agent integration instructions.

Browser capture, annotation features, document adapters, MCP support and any desktop companion are being evaluated. Platform-specific capabilities will be documented explicitly.

## Design principles

- Report what was actually captured; do not infer success from a file path alone.
- Treat ambiguous targets and missing permissions as explicit outcomes.
- Keep original captures separate from processed images.
- Let agents use their existing models and document-editing tools.

## Development

The implementation language, platform backends and build commands are not selected yet. See the [requirements discussion draft](docs/requirements.md) for confirmed requirements and open decisions.

## License

[MIT](LICENSE)
