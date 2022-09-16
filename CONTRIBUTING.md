# Contributing

First, we are glad you are interested in contributing to our project.
Below you will find the information you need to get started.

## Requirements

For local development and executing the code, you need a few things:

- [asdf](https://asdf-vm.com/) - which manages multiple runtime versions;
- [direnv](https://direnv.net/) - which augments existing shells with a new feature that can load and unload environment variables.

All these tools must be installed and configured according to their official documentation.

### asdf

The config file `.tool-versions` is located in the root directory. The structure is very straightforward.

```shell
terraform 1.2.9
terraform-docs 0.16.0
tflint 0.40.0
pre-commit 2.20.0
```

To install managed tools in proper versions, run the command as in the example below

```shell
% asdf install
terraform 1.2.9 is already installed
pre-commit 2.20.0 is already installed
terraform-docs 0.16.0 is already installed
tflint 0.40.0 is already installed
```
**Notice**: the output will vary; this is just an example.

**Important**: Please keep in mind the versions or tools themselves might change, so it is advised to rerun `asdf install` command after pulling from git.

After the installation process, all the tools will be installed. You can verify this by executing

```shell
% terraform --version
Terraform v1.2.9
on darwin_amd64
```

in the project directory.

More information and examples can be found in the ASDF project [documentation](https://asdf-vm.com/manage/plugins.html).

### direnv

The direnv config files `.envrc` might be present in many directories.
Therefore, you must approve each of them by entering a particular directory whenever their contents change.

**Notice**: The descriptive error will pop up if you forget to do so.

To allow direnv to load its config run:

```shell
% direnv allow
direnv: loading .envrc
direnv: export ~PATH
```
**Notice**: output will vary depending on directory in which you run it.
