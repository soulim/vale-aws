# AWS style for Vale CLI _(vale-aws)_

A style for Vale prose linter.

## Background

While reading about AWS services on the internet, I've noticed that many times authors make mistakes in names of these services. For example they say *Amazon* Lambda instead of [*AWS* Lambda](https://aws.amazon.com/lambda/), or *AWS* DynamoDB instead of [*Amazon* DynamoDB](https://aws.amazon.com/dynamodb/).

I believe it's important to use correct names and terms (especially if you write professionally). However I could also understand that it might be tricky sometimes. It's better to use machines to help us to avoid mistakes.

That's why I created AWS style for Vale linter.

### Example

With this style Vale doesn't just highlight mistakes, but also provide suggestions.

```ShellSession
> vale --output=line samples/
samples/default.md:6:5:AWS.Names:Use 'Amazon DynamoDB' instead of 'AWS DynamoDB'
samples/default.md:8:5:AWS.Names:Use 'AWS Lambda' instead of 'Amazon Lambda'
samples/default.md:10:5:AWS.Names:Use 'AWS IoT Core' instead of 'Amazon IoT Core'
samples/default.md:11:5:AWS.Names:Use 'Amazon Cognito' instead of 'AWS Cognito'
```

### What is Vale?

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
bin/list | bin/gen > AWS/Names.yml
```

```
# vale.ini

StylesPath = styles

[*.{md,txt}]
BasedOnStyles = Vale, AWS
```

## Contributing

PRs accepted.

## License

MIT © [Alexander Sulim](https://sul.im/)
