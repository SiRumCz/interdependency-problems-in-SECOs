# Dependency modelling comparision table for 5 software ecosystems

## Selected packaging ecosystems

**Maven**: an Apache software used for software project management and comprehension tool based on the concept of project object model(POM). https://maven.apache.org/ <br>
**NPM**: a node package management tool for Node.js runtime environment and JavaScript web applicaiton frameworks, libraries, and utilities started in 2010. NPM registry currently hosts over 1,000,000 packages with 11,000,000,000 weekly and 49,000,000,000 monthly downloads, it is the largest considered ecosystem. https://www.npmjs.com/ <br>
**CRAN**: the Comprehensive R Archive Network that stores identical, up-to-date, versions of code and documentation for statistical computing enviroment R. https://cran.r-project.org/ <br>
**dpkg**: a package manager for Debian-based systems. As of July 30th 2019, Debian stable version contains 28,497 packages in main section. http://man7.org/linux/man-pages/man1/dpkg.1.html <br>
**Cargo**: the official package manager for Rust programming language since 2014. Rust is a modern system-level programming language released in 2012 by Mozilla. I expect to see Rust community carry out the best practices in dependency management given the fact it is a young and trending platform. https://crates.io/ <br>

## Table

|                                 | Maven                       | NPM                     | CRAN                | dpkg                       | Cargo               |
| ------------------------------- | --------------------------- | ----------------------- | ------------------- | -------------------------- | ------------------- |
| software ecosystem              | Java / Apache               | JavaScript / Node.js    | R                   | Debian / Linux OS          | Rust                |
| type of ecosystem               | packaging ecosystem         | packaging ecosystem     | packaging ecosystem | distribution for Linux OSs | packaging ecosystem |
| metadata                        | pom.xml                     | package.json            | DESCRIPTION         | DEBIAN/control             | Cargo.toml          |
| general dependency              | dependencies, compile scope | dependencies            | Depends             | Depends                    | dependencies        |
| build/test/developer dependency | test scope                  | devDependencies         | Build-Depends       | Build-Depends              | dev-dependencies    |
| optional dependency             |                             | optionalDependen-
cies  | Suggests            | Recommands                 |                     |
| conflicting dependency          |                             |                         | Conflicts           | Conflicts                  |                     |
| breaking dependency             |                             |                         | Breaks              | Breaks                     |                     |
| versioning policy               | semantic versioning         | semantic versioning     |                     |                            | semantic versioning |
| policy                          |                             |                         | rolling release     |                            |                     |

## References
Alexandre Decan, Tom Mens, Philippe. An Empirical Comparision of Dependency Network Evolution in Seven Software Packaging Ecosystems. *Journal, Empirical Software Engineering Volume 24 Issue 1*. 2019
