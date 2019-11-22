# `atomist/npm-goal`

An Atomist goal to run NPM compile, test and publish from an Software
Delivery Machine (SDM).

## Usage

### NPM `install`

Put the following YAML into your SDM goal definition to use the `install`
goal.

```yaml
node_build:
  
  goals:
  - atomist/npm-goal/install@master
      parameters:
        tag: <optional tag of node Docker image>
        command: <optional command to run; either ci or install; defaults to ci>
```
### NPM `compile`

Put the following YAML into your SDM goal definition to use the `compile`
goal.

```yaml
node_build:
  
  goals:
  - atomist/npm-goal/compile@master
      parameters:
        tag: <optional tag of node Docker image>
        command: <optional command to run; defaults to compile>
```

### NPM `test`

Put the following YAML into your SDM goal definition to use the `test`
goal.

```yaml
node_build:
  
  goals:
  - atomist/npm-goal/test@master
```

### NPM `test`

Put the following YAML into your SDM goal definition to use the `test`
goal.

```yaml
node_build:
  
  goals:
  - atomist/npm-goal/test@master
```

### NPM `publish`

Put the following YAML into your SDM goal definition to use the `publish`
goal.

```yaml
node_publish:
  
  goals:
  - atomist/npm-goal/publish@master:
      parameters:
        access: <optional access to package; allowed public or restricted; defaults to restricted>
```

The `publish` goal needs credentials to publish the NPM package to the 
registry. By default the goal will make all NPM resource providers from your
Atomist workspace availabe to the goal. 

## Getting started

See the [Developer Quick Start][atomist-quick] to jump straight to
creating an SDM.

[atomist-quick]: https://docs.atomist.com/quick-start/ (Atomist - Developer Quick Start)

## Contributing

Contributions to this project from community members are encouraged
and appreciated. Please review the [Contributing
Guidelines](CONTRIBUTING.md) for more information. Also see the
[Development](#development) section in this document.

## Code of conduct

This project is governed by the [Code of
Conduct](CODE_OF_CONDUCT.md). You are expected to act in accordance
with this code by participating. Please report any unacceptable
behavior to code-of-conduct@atomist.com.

## Documentation

Please see [docs.atomist.com][atomist-doc] for
[developer][atomist-doc-sdm] documentation.

[atomist-doc-sdm]: https://docs.atomist.com/developer/sdm/ (Atomist Documentation - SDM Developer)

## Connect

Follow [@atomist][atomist-twitter] and [The Composition][atomist-blog]
blog related to SDM.

[atomist-twitter]: https://twitter.com/atomist (Atomist on Twitter)
[atomist-blog]: https://the-composition.com/ (The Composition - The Official Atomist Blog)

## Support

General support questions should be discussed in the `#support`
channel in the [Atomist community Slack workspace][slack].

If you find a problem, please create an [issue][].

[issue]: https://github.com/atomist/npm-goal/issues

---

Created by [Atomist][atomist].
Need Help?  [Join our Slack workspace][slack].

[atomist]: https://atomist.com/ (Atomist - How Teams Deliver Software)
[slack]: https://join.atomist.com/ (Atomist Community Slack)
