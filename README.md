**DEPRECATED** this action is no longer required as it's now supported natively by actions/setup-node@v2

# Read nvmrc action

Simple action to read value from `.nvmrc` file.



## Usage

Example of workflow:

```yaml
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@v2
  
    # Read node version from `.nvmrc` file
    - id: nvmrc
      uses: browniebroke/read-nvmrc-action@v1

    - uses: actions/setup-node@v1
      with:
        # use the output from the action
        node-version: '${{ steps.nvmrc.outputs.node_version }}'

```
