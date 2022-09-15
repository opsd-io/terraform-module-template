# Contributing to terraform modules

- [Contributing to terraform modules](#contributing-to-terraform-modules)
	- [Requirements](#requirements)
		- [asdf](#asdf)
		- [direnv](#direnv)

## Requirements

For local development and executing the code you need:

- [asdf](https://asdf-vm.com/) - manages multiple runtime versions - all tools should be installed this way.
- [direnv](https://direnv.net/) - augments existing shells with a new feature that can load and unload environment variables.

These tools must be installed and configured according to their official documentation.

### asdf

Currently there is only one asdf config file - `.tool-versions` - is in root directory.
That means it should not be required to rerun asdf installation process when changing directories.
But keep in mind the versions or tools itself might change so it is advised to rerun it after pulling from git.
To install managed tools in proper versions run:

```shell
% asdf install
terraform 1.1.5 is already installed
pre-commit 2.19.0 is already installed
terraform-docs 0.16.0 is already installed
tflint 0.33.1 is already installed
```
Notice: output will vary, this is just an example.

If you get an error that a plugin is not installed, add it to ASDF

- list of installed plugins:
```shell
% asdf plugin list
```

- list of all plugins:
```shell
% asdf plugin list all
```

- To add the plugin to ASDF run command:
```shell
% asdf plugin-add <plugin-name> <repository>
```

Example:
```shell
% asdf plugin-add pre-commit git@github.com:jonathanmorley/asdf-pre-commit.git
```

### direnv

The direnv config files - `.envrc` - are present in many directories.
You have to approve each of them on first time entering particular directory, and whenever theirs contents changes.
The descriptive error will pop up if you forget to do so.
To allow direnv to load it's config run:

```shell
% direnv allow
direnv: loading .envrc
direnv: export ~PATH
```
Notice: output will vary depending on directory in which you run it.
