### Dependency modelling table for 5 software ecosystems

**Maven**: an Apache software used for software project management and comprehension tool based on the concept of project object model(POM). https://maven.apache.org/ <br>
**NPM**: a node package management tool for Node.js runtime environment and JavaScript web applicaiton frameworks, libraries, and utilities. NPM registry currently hosts over 1,000,000 packages with 11,000,000,000 weekly and 49,000,000,000 monthly downloads. https://www.npmjs.com/ <br>
**CRAN**: the Comprehensive R Archive Network that stores identical, up-to-date, versions of code and documentation for R. https://cran.r-project.org/ <br>
**dpkg**: a package manager for Debian-based systems. As of July 30th 2019, Debian stable version contains 28,497 packages in main section. http://man7.org/linux/man-pages/man1/dpkg.1.html <br>
**Cargo**: a package manager for Rust programming language. Rust is a modern system-level programming language. I expect to see Rust community carry out the best practices in dependency management given the fact it is a young and trending platform. https://crates.io/ <br>

|                    | Maven               | NPM                  | CRAN                | dpkg                       | Cargo               |
| ------------------ | ------------------- | -------------------- | ------------------- | -------------------------- | ------------------- |
| software ecosystem | Java / Apache       | JavaScript / Node.js | R                   | Debian / Linux OS          | Rust                |
| type of ecosystem  | packaging ecosystem | packaging ecosystem  | packaging ecosystem | distribution for Linux OSs | packaging ecosystem |
| metadata           | pom.xml             | package.json         | DESCRIPTION         | DEBIAN/control             | Cargo.toml          |
