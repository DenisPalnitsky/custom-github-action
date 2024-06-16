# Custom Github Action Example

# Short sha

This is a custom GitHub Action that provides the short git SHA.

## Outputs

- `sha-short`: The short git SHA (7 characters)

## Usage

You can use this action in your workflow file as follows:

```yaml
steps:
    - name: Checkout repository
    uses: actions/checkout@v4

    - name: Use custom action
    id: custom-action
    # this is our custom action's repository name and branch that we want to use
    uses: denispalnitsky/custom-github-action@main

    - name: Print result
    run: |
        echo "Short sha of current commit: ${{ steps.custom-action.outputs.sha-short }}"
```