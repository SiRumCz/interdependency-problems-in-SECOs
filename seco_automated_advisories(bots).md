This topic studies the feature and mechanism for current trending dependency(library) management bots. The bots I select for this topic was top bots from github marketplace with `Dependency management` Type filtered. The list is accessible from https://github.com/marketplace/category/dependency-management

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
- **Transitive dependency for JavaScript**
  - https://dependabot.com/blog/securing-javascript-transitive-dependencies/
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

### MyGet (https://www.myget.org/)
organization github: https://github.com/MyGet, This is a commercial product. No available source code.<br>
#### Features
- **Manage softwares**
  - from NuGet, OneGet, Chcolatey, TeamCity, npmjs, Maven Centrral, Bower, Packagist, PyPI, proxied into one URL provided by MyGet
- **Package mirroring**
  - mirror package onto MyGet feed. Upstream package source can be proxied and filtered.
- **Continous Integration**
  - Assembla, GitHub, Visual Studio Team Services, or BitBucket code repository
  - MyGet build servers(or use developers own build server, such as VSTS, TeamCity, Jenkins) compile code, discover and run tests, and creat package artifacts
  - MyGet publishes the build as package to developers' feed if the build test is error-free
- **Continous Security**
  - quickly see the overview of potential vulnerabilities in all dependencies
  - percentage of packages with potential vulnerabilities VS percentage of packages without known vulnerabilities
- **License governance**
  - inspect and manage licenses used across feeds
  - for example: ensure no GPL software is being used in commercial apps
  
### Renovate (https://renovatebot.com/)
Universal dependency update automation tool that fits into your workflows.<br>
#### Features
- **Real time library version monitoring**
- **Supported languages**
  - Dockerfile, Go, Gradle, HCL, Java, JavaScript, Maven POM, PHP, Python, Ruby
- **Detailed updates**
  - changelogs and commit hostries with each update
- **Run existing test suite**
- **Customizable upgrade schedule**

### Depfu (https://depfu.com)

### Sonatype DepShield (https://depshield.github.io/)

## Passive Badges with Dashboard

### David-DM (https://david-dm.org/)

### semantic-release (https://semantic-release.gitbook.io/semantic-release/)

### Codecov (https://codecov.io/gh)

## Comparison Table
This table shows how GitHub Dependency Mamagement Bots differ in features

|                                     | Dependabot                    | Greenkeeper | Snyk             | MyGet      | Renovate         | Depfu    | Sonatype DepShield |
| ----------------------------------- | ----------------------------- | ----------- | ---------------- | ---------- | ---------------- | -------- | ------------------ |
| Support studied software ecossytems | NPM, Rust(Cargo), Java(Maven) | NPM only    | Java(Maven), NPM | Maven, NPM | Java(Maven), NPM | NPM only | All                |
| Free for open source projects       | yes                           | yes         | yes              | no         | yes              | yes      | yes                |
| vulnerability database              | yes                           | no          | yes              | yes        | no               | yes      | yes                |
| lockfile support                    | yes                           | yes         | yes              | yes        | no               | yes      | no                 |
| automated pull request              | yes                           | yes         | yes              | yes        | yes              | yes      | no                 |
| automated issue                     | no                            | no          | no               | no         | no               | no       | yes                |
| CI built-in                         | no                            | no          | yes              | yes        | no               | no       | no                 |
| License issue                       | no                            | no          | yes              | yes        | no               | no       | no                 |
