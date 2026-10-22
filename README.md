# Remove File

**R**e**m**oves a given file or folder in a cross-platform way.

Created by Jesse Talavera-Greenberg.

# Installation

Enable local and third-party actions for your repository, then just follow the instructions in Usage.

## Usage

Use this action in any particular step like so:

```yaml
- name: Remove File
  uses: JesseTG/rm@v1.0.3
  with:
    path: /path/to/something/you/want/to/delete

```

Other useful facts:

- Uses [`io.rmRF`](https://github.com/actions/toolkit/tree/master/packages/io#rm--rf), so it will remove files and directories recursively.
- Succeeds even if the requested path doesn't exist.
- Works on all environments.
- Only supports one path at a time; for multiple paths, use this action multiple times.
- Supports relative and absolute paths, but does *not* support globs or wildcards.
- **Does not protect important system paths.** Be careful if you're using a self-hosted runner.
- Can be used to remove files from your repository within a workflow, but you will have to commit the changes yourself.

## License

MIT.

## Privacy

This Action contacts Chainguard's licensing server to verify authorization. Connection metadata (IP address, GitHub repository identifier, timestamp, and any metadata encoded in the auth token) is transmitted to Chainguard, Inc. even if authorization is denied in accordance with our [Privacy Notice](https://www.chainguard.dev/legal/privacy-notice)
