# shfz-actions-setup

This action for setup shfz.

## Inputs

## `version`

**Required** The version of [shfz](https://github.com/shfz/shfz).

## Outputs

## Example usage

```
uses: shfz/shfz-actions-setup@v0.0.2
with:
  version: '0.0.2'
```

## Includes actions

```yml
    - name: setup shfz
      run: |
        wget https://github.com/shfz/shfz/releases/download/v${{ inputs.version }}/shfz_${{ inputs.version }}_linux_amd64.tar.gz
        tar -zxvf shfz_${{ inputs.version }}_linux_amd64.tar.gz
        sudo mv shfz /usr/local/bin/
        sudo chmod +x /usr/local/bin/shfz
        shfz --help
      shell: bash
    - name: run shfz server
      run: shfz server &
      shell: bash
```
