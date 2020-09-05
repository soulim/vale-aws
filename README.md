# AWS style for Vale CLI _(vale-aws)_

A style for Vale prose linter.

## What is Vale?

Vale is a syntax-aware linter for prose built with speed and extensibility in mind.

Unlike most writing-related software, Vale's primary purpose isn't to provide its own advice; it's designed to enforce an existing style guide through its YAML-based extension system.

Vale uses a plain-text (INI and YAML) configuration system that makes it possible to share configurations across platforms, applications, and users.

Repository: [github.com/errata-ai/vale](https://github.com/errata-ai/vale)

## Install

```
git clone git@github.com:soulim/vale-aws.git
```

## Usage

```
mkdir -p ~/.config/vale/styles/AWS
bin/list | bin/gen > ~/.config/vale/styles/AWS/Names.yml
```

```
# ~/.config/vale/vale.ini

StylesPath = styles

[*.{md,txt}]
BasedOnStyles = Vale, AWS
```

## Contributing

PRs accepted.

## License

MIT © [Alexander Sulim](https://sul.im/)
