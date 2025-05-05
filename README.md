# Copier template to create Plone Backend / Classic UI setups

## Features

- support's 3 storage options: direct (standalone), ZEO, relstorage
- uses pyproject.toml, [PDM](https://pdm-project.org/en/latest/) and [UV](https://docs.astral.sh/uv/) with [hatchling](https://hatch.pypa.io/1.13/config/build/#build-system) build-backend
- is able to update existing projects when the template changes

More about using [PDM](https://pdm-project.org/en/latest/) to manage packages.
More info about [Copier](https://copier.readthedocs.io/en/stable/) to generate projects from templates.


## Usage

## Create project

```sh
uvx copier copy gh:mrtango/pdmplone my-project.de
cd my-project.de
uvx pdm install
```

## Update existing project

When ever the template has updates, you can update your generated project.

```sh
uvx copier update --trust
```

or without the answering the questions again:

```sh
uvx copier update --defaults --trust
```

You can also add `https://github.com/MrTango/pdmplone` to trusted locations and run the commands without the `--trust` parameter.

https://copier.readthedocs.io/en/stable/settings/#trusted-locations

On Linux:

```sh
mkdir ~/.config/copier
touch ~/.config/copier/settings.yml
```