This study shows the internal or external policies suggested migration opportunity advisories from official websites and communities for different packaging software ecosystems

## Software Ecosystems

### Maven - Java
**Versions Maven Plugin** [4]<br>
A plugin that allows user to check updates for both maven packages and plugins<br>
![Maven Verssions new release announcement example](https://github.com/SiRumCz/interdependency-problems-in-SECOs/blob/master/src/seco_new_release_screenshots/versions_maven_plugin_scrrenshot.png)

**artifact listener** [5]<br>
create an account on the website and choose the artifact you would like to follow by either manually searching or uploading full pom.xml file.<br>
![Maven Verssions new release announcement example](https://github.com/SiRumCz/interdependency-problems-in-SECOs/blob/master/src/seco_new_release_screenshots/maven_artifact_listener_screenshot.png)

**mailing lists** [10]<br>
Developers has been actively use mailing lists to announce new Maven plugins releases through many subscriptions:<br>
Users: https://lists.apache.org/list.html?users@maven.apache.org<br>
Developers: https://lists.apache.org/list.html?dev@maven.apache.org<br>
Announcements: https://lists.apache.org/list.html?announce@maven.apache.org<br>

**Issue tracker - JIRA** [11]<br>


**IRC (Internet Relay Chat)** <br>

### NPM - JavaScript/Node.js

NPM documents vulnerability threats in their public vulnerability database such as NPM security advisories(https://www.npmjs.com/advisories) or Snyk vulnerability DB.<br>

### CRAN - R
NEWS.md : release announcement<br>

publish package release announcement on the **RStudio blog**(https://blog.rstudio.com/) [3]<br>
![RStudio blog new release announcement example](https://github.com/SiRumCz/interdependency-problems-in-SECOs/blob/master/src/seco_new_release_screenshots/rstudio_blog_screenshot.png)

**Twitter** with the #rstats hashtag [3]<br>
![Twitter new release announcement example](https://github.com/SiRumCz/interdependency-problems-in-SECOs/blob/master/src/seco_new_release_screenshots/twitter_rstats_hashtag_screenshot.png)

send to the r-packages **mailing-list**(https://stat.ethz.ch/mailman/listinfo/r-packages) [3], r-help mailing-list has been active since late 90's and is still very active.<br>
![R-help mailing-list new release announcement example](https://github.com/SiRumCz/interdependency-problems-in-SECOs/blob/master/src/seco_new_release_screenshots/r-help_screenshot.png)

**R-bloggers**(https://www.r-bloggers.com)<br>
![R-bloggers new release announcement example](https://github.com/SiRumCz/interdependency-problems-in-SECOs/blob/master/src/seco_new_release_screenshots/Screenshot%20from%202019-08-07%2012-13-25.png)

Open source, collaborative, distributed software developement platforms:
- Bioconductor(https://www.bioconductor.org/)
- R-Forge(https://r-forge.r-project.org/)
- RForge(https://www.rforge.net/)

Based on Alexandre Decan's studies[9] on the influence of using GitHub on CRAN, it shows that many R packages are hosted on GitHub and there is still important acceleration of the number of new packages appearing each month. One of the reason is that some packages depend on external packages which opposed the CRAN policy, and therefore cannot be accepted by CRAN.

### dpkg - Debian GNU/Linux
**Twitter** was used by debian developers to make new release announcements<br>
![Twitter debian package new release announcement example](https://github.com/SiRumCz/interdependency-problems-in-SECOs/blob/master/src/seco_new_release_screenshots/twitter_debian_screenshot.png)

**mailing list**

**blogs**

**IRC channels**

### Cargo - Rust
Officially the only mailing list **rust-dev**(https://mail.mozilla.org/listinfo/rust-dev) was shut down few years ago due to low traffic[8]<br>
Maintainers use **Rust user community**(https://users.rust-lang.org/) to make new release announcement<br>
![users_rust-lang new release announcement example](https://github.com/SiRumCz/interdependency-problems-in-SECOs/blob/master/src/seco_new_release_screenshots/rust_lang_announcement_screenshot.png)

Developers also use **Reddit**(https://www.reddit.com/r/rust/) as active community to communitcate new release changes<br>
![reddit_r/rust new release announcement example](https://github.com/SiRumCz/interdependency-problems-in-SECOs/blob/master/src/seco_new_release_screenshots/reddit_rust_screenshot.png)

I have also seen uses of new release announcement on **Twitter** with different hash tags<br>
- #rust-lang<br>
![reddit_r/rust new release announcement example](https://github.com/SiRumCz/interdependency-problems-in-SECOs/blob/master/src/seco_new_release_screenshots/twitter_rust_lang_screenshot.png)
- #rust<br>
![reddit_r/rust new release announcement example](https://github.com/SiRumCz/interdependency-problems-in-SECOs/blob/master/src/seco_new_release_screenshots/twitter_rust_lang_screenshot_2.png)

## References
[1] Christopher Bogart, Christian Kastner, James Herbsleb. When it breaks, it breaks: How ecosystem developers reason about the stability of dependencies. *30th IEEE/ACM International Conference on Automated Software Engineering Workshop*. 2015<br>
[2] Christopher Bogart, Christian Kastner, James Herbsleb, Ferdian Thung. How to Break an API: Cost Negotiation and Community Values in Three Software Ecosystems. *24th ACM SIGSOFT International Symposium on Foundations of Software Engineering*. 2016<br>
[3] http://r-pkgs.had.co.nz/release.html#promotion<br>
[4] http://www.mojohaus.org/versions-maven-plugin/<br>
[5] https://www.artifact-listener.org/<br>
[6] https://github.blog/2017-10-11-a-more-connected-universe/<br>
[7] https://users.rust-lang.org/c/announcements<br>
[8] https://mail.mozilla.org/pipermail/rust-dev/2015-January/011558.html<br>
[9] Alexandre Decan, Tom Mens, Maelick Claes, Philippe Grosjean. When GitHub meets CRAN: An Analysis of Inter-Repository Package Dependency Problems. *IEEE 23rd International Conference on Software Analysis, Evolution, and Reengineering*. 2016<br>
[10] https://maven.apache.org/mailing-lists.html<br>
[11] https://maven.apache.org/issue-management.html<br>
