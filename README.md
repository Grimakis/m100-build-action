# m100-build action

Composite GitHub Action that installs `@m100/cli` and builds packed `.DO` and tokenized `.BA` artifacts.

## Inputs
- `source` (required): Path to the source `.DO` file.
- `cli-package` (optional): NPM package name. Default: `@m100/cli`.
- `base` (optional): Base address (hex, no 0x). Default: `8001`.
- `out-dir` (optional): Output directory. Default: `dist`.
- `ascii-name` (optional): Packed `.DO` output name. Defaults to `basename(source)`.
- `tokenized-name` (optional): Tokenized `.BA` output name. Defaults to `ascii-name` with `.DO` -> `.BA`.

## Outputs
- `ascii-path`: Path to the packed `.DO` output.
- `tokenized-path`: Path to the tokenized `.BA` output.

## Example
```yaml
- uses: Grimakis/m100-build-action@v1
  with:
    source: src/EQUITY.DO
    ascii-name: EQUITY.DO
    tokenized-name: EQUITY.BA
```
