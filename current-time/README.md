# Current Time Javascript Action

This action sets the current ISO8601 time to the `time` output.

## Outputs

### `time`

The UTC time when this step was run.

## Example usage

```yaml
steps:
- name: Get current time
  uses: gerred/actions/current-time@master
  id: current-time
- name: Use current time
  env:
    TIME: "${{ steps.current-time.outputs.time }}"
  run: echo $TIME
```