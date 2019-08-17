This topic studies the feature and mechanism for current trending dependency(library) management bots.

## Automated Pull Requests

### Dependabot (https://dependabot.com)
source code: https://github.com/dependabot/dependabot-core<br>
#### Features
- **Pull requests**
  - include release notes, changelogs, commit links and vulnerability details
- **Bot behavior is configurable**
  - how many dependencies to be updated
  - how frequent to have pull requests
- **Automatically handle security advisories**
  - for Ruby, Python, JavaScript, Java, .NET, PHP, Elixir and Rust
- **Compatibility score for each update**
  - aggregate everyone's test results
- **Support for GitHub Enterprise, GitLab and Azure DevOps**
#### Mechanisms
doc: https://github.com/dependabot/dependabot-core#architecture<br>
**dependabot-{package-manager}**
1. fetch dependency files and extract the list of dependencies for a project
2. check for dependency updates
3. create pull request on dependency file with new versions and restrictions

**security advisory**
Ruby: Rubysec (https://rubysec.com) <br>

### Greenkeeper (https://greenkeeper.io/)
only works for JavaScript packages hosted on GitHub using either NPM or Yarn.<br>
source code: https://github.com/greenkeeperio/greenkeeper<br>
#### Features
- **Automated, real-time dependency updates**
  - Only on *JavaScript* projects using either NPM or Yarn
- **Full support for GitHub private packages**
- **Self-hosted Greenkeeper Enterprise option**
  - Commercial version for GitHub Enterprise users
- **CI test suite integrated**
  - Run CI on every dependency update
- **Built-in lockfile support**
  - package-lock.json(NPM), yarn.lock(Yarn)
- **Seamless integration**
  - The porcess will not interupt the current workflow

#### Mechanisms
Monitoring dependency list of NPM projects hosted on GitHub. When any module from the list get updated in NPM registry, Greenkeeper will create a new branch with that update for the project. If projects have CI integrated, it will also check the test result to determine the needs for opening new issue regarding this update.

### Snyk (https://snyk.io)
source code: https://github.com/snyk/snyk<br>
#### Features
- **Find vulnerabilities** `snyk test`
  - Map the full application dependency tree to fild the vulnerabilities(tested against Snyk's comprehensive vulnerability database) in all open source dependencies
- **Fix vulnerabilities** `snyk wizard` and `snyk protect`
  - Automatically generate fix pull request that helps for 1) upgrade, 2) precision patch
- **Monitor throughout the Software Development Life Cycle**
  - Supports platform: GitHub, BitBucket, and GitLab.
  - CI/CD: Jenkins, Teamcity, Travis and more
  - PaaS and serverless: Heroku, Cloud Foundry, AWS Lambda and more
- **Prevent**
  - secure development: integrated in IDE(?)
  - secure source code: pull requests to fail checks on new vulnerable dependency addition
  - secure build: fail CI builds, **policy based**
- **Alert** `snyk monitor`
  - newly disclosed vulnerabilities
  - email and Slack notifications
  - automatic pull request
  - comprehensive information and remediation guidance

Note: **Supporting languages**
  - Ruby, Java, Scala, Python, Golang, .NET, PHP, Node.js(NPM&Yarn)

## Passive Badges with Dashboard

### David-DM (https://david-dm.org/)

### semantic-release (https://semantic-release.gitbook.io/semantic-release/)

### Codecov (https://codecov.io/gh)
