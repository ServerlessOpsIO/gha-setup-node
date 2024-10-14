# gha-setup-node
This GitHub Action sets up a NodeJS environment for use in workflows.

_*NOTE: This workflow is opinionated and meets the needs of its author. It is provided publicly as a reference for others to use and modify as needed.*_

This action will perform the following actions:
* Install nodejs
* Enable Yarn
* Install dependencies

## Usage
See below for inputs, outputs, and examples.

### Inputs

_Note: either `node_version` or `node_version_file` must be set but not both._

- `node_version` (_optional_): The version of NodeJS to use.
- `node_version_file` (_optional_): The file to read the NodeJS version from.

### Outputs
- `node-version`: he installed NodeJS version. Useful when given a version range as input.
- `cache-hit`: A boolean value to indicate a cache entry was found

### Examples
To use this action, add the following step to your workflow:

```yaml
steps:
  - name: Checkout code
    uses: ServerlessOpsIO/gha-setup-workspace@v1

  - name: Setup NodeJS environment
    uses: ServerlessOpsIO/gha-setup-node@v1
    with:
      node_version: 'lts/*'
```

## Contributing
Contributions are welcome! Please open an issue or submit a pull request for any changes.

## Contact
For any questions or support, please open an issue in this repository.
