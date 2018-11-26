# buck-cells-test

```bash=
$ buck run :app
```

Buck seems to require all cells to be declared at the top-level: 

```ini=
[repositories]
  vendor-foo = ./vendor/foo
  vendor-bar = ./vendor/foo/vendor/bar
```

Without you get this error: 

> repositories.vendor-bar must exist in the root cell's cell mappings.

This is a hindrance because now you cannot nest cells without figuring out the transitive cells. 

Tested using: 

```bash=
$ buck --version
buck version 2018.10.29.01
```
