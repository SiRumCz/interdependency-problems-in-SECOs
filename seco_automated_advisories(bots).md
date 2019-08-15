This topic studies the feature and mechanism for current trending dependency(library) management bots.

## Automated Pull Requests

### Dependabot (https://dependabot.com)
source code: https://github.com/dependabot/dependabot-core<br>
#### Features
- **Pull requests**<br> 
  - include release notes, changelogs, commit links and vulnerability details<br>
- **Bot behavior is configurable**<br>
  - how many dependencies to be updated<br>
  - how frequent to have pull requests<br>
- **Automatically handle security advisories**<br> 
  - for Ruby, Python, JavaScript, Java, .NET, PHP, Elixir and Rust<br>
- **Compatibility score for each update**<br> 
  - aggregate everyone's test results<br>
- **Support for GitHub Enterprise, GitLab and Azure DevOps**
#### Mechanisms
doc: https://github.com/dependabot/dependabot-core#architecture<br>
**dependabot-{package-manager}**
1. fetch dependency files and extract the list of dependencies for a project
2. check for dependency updates
3. create pull request on dependency file with new versions and restrictions

### Greenkeeper (https://greenkeeper.io/)
only works for JavaScript packages hosted on GitHub using either NPM or Yarn.<br>
source code: https://github.com/greenkeeperio/greenkeeper<br>
#### Features
- **Automated, real-time dependency updates**<br>
  - Only on *JavaScript* projects using either NPM or Yarn<br>
- **Full support for GitHub private packages**<br>
- **Self-hosted Greenkeeper Enterprise option**<br>
  - Commercial version for GitHub Enterprise users<br>
- **CI test suite integrated**<br>
  - Run CI on every dependency update<br>
- **Built-in lockfile support**<br>
- **Seamless integration**<br>
  - The porcess will not interupt the current workflow<br>

#### Mechanisms

### Snyk (https://snyk.io)
source code: https://github.com/snyk/snyk<br>
#### Features
- **Find vulnerabilities**
  - Map the full application dependency tree to fild the vulnerabilities(tested against Snyk's comprehensive vulnerability database) in all open source dependencies
- **Fix vulnerabilities**
  - Automatically generate fix pull request that helps for 1) upgrade, 2) precision patch
- **Monitor throughout the Software Development Life Cycle**
  - Supports platform: GitHub, BitBucket, and GitLab.
  - CI/CD: Jenkins, Teamcity, Travis and more
  - PaaS and serverless: Heroku, Cloud Foundry, AWS Lambda and more

## Passive Badges with Dashboard

### David-DM (https://david-dm.org/)

### semantic-release (https://semantic-release.gitbook.io/semantic-release/)

### Codecov (https://codecov.io/gh)
