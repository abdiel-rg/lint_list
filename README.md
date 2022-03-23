# Lint_List

This package gets the lints from the [linter](https://pub.dev/packages/linter) package, specifically the ones from this path: `linter/example/all.yaml`, and makes them available for use.

It also gets automatically updated every now and then using GitHub Actions.

## Installation

Add this package to the `dev_dependencies` section of the `pubspec.yaml` file:

```yaml
dev_dependencies:
    lint_list:
```

## Usage

After installing the package, replace the line that starts with `include`, in the `analysis_options.yaml` file, with this line:

```yaml
include: package:lint_list/all.yaml
```

### Why do I have to replace the line and not paste the previous line below it?

According to the [**Customizing static analysis**](https://dart.dev/guides/language/analysis-options#the-analysis-options-file) guide on [dart.dev](https://dart.dev):
*"YAML doesn’t allow duplicate keys, you can include at most one file"*.
