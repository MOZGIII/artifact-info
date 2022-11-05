# artifact-info action

The action to get the artifact info.

Would be. Doesn't work at the moment, see <https://github.com/actions/upload-artifact/issues/53>.

## Usage

```yaml
- name: Upload artifact
  uses: actions/upload-artifact@v3
  with:
    name: sample-artifact
    path: sample-artifact.txt

- uses: MOZGIII/artifact-info@v1
  id: artifact-info
  with:
    artifact-name: sample-artifact

- run: echo ${{ steps.artifact-info.outputs.archive-download-url }}
```

See [.github/workflows/test.yml](.github/workflows/test.yml).
