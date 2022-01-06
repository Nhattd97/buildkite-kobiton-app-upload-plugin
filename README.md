# Kobiton App Upload Buildkite Plugin

A Plugin that take an apk or ipa file and upload it to Kobiton App.

## Example

Add the following to your `pipeline.yml`:

```yml
steps:
  - command:
    plugins:
      - Nhattd97/kobiton-app-upload#v1.0.0:
          app-name: '<app-name>'
          app-path: '<path-to-your-app>'
          app-type: '<apk or ipa>'
          kobiton-app-id: 'your-kobiton-app-id'
          kobiton-app-access: 'private'
          kobiton-username: '<your-kobiton-username>'
          kobiton-api-key: '<your-kobiton-api-key>'
```

## Configuration

### `pattern` (Required, string)

The file name pattern, for example `*.ts`. Supports any pattern supported by [find -name](http://man7.org/linux/man-pages/man1/find.1.html).

## Developing

To run the tests:

```shell
docker-compose run --rm tests
```

To validate the `plugin.yml`:
```shell
docker-compose run --rm lint
```

## Contributing

1. Fork the repo
2. Make the changes
3. Run the tests
4. Commit and push your changes
5. Send a pull request