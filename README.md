# repository-template-java
A template to use when starting a new open source project.

## perform a repository wide search and replace for "repository-template-java" and the "target-repo-name"

e.g. by using

```
cp -R repository-template-java/ new-name && cd new-name && git config --local --unset remote.origin.url && git config --local --add remote.origin.url git@github.com:baloise/new-name.git && git reset --hard $(git commit-tree FETCH_HEAD^{tree} -m "Initial contribution") &&  git grep -l 'repository-template-java' | xargs sed -i '' -e 's/repository-template-java/new-name/g' && mvn clean verify && git add -A && git commit -m "Rename from template to new-name" && cd ..
```
[![Codacy Badge](https://api.codacy.com/project/badge/Grade/bf6fa237dd934970991ecba2c66db23e)](https://app.codacy.com/app/baloise/repository-template-java?utm_source=github.com&utm_medium=referral&utm_content=baloise/repository-template-java&utm_campaign=Badge_Grade_Dashboard)
[![DepShield Badge](https://depshield.sonatype.org/badges/baloise/repository-template-java/depshield.svg)](https://depshield.github.io)
![Build Status](https://github.com/baloise/repository-template-java/workflows/CI/badge.svg)

## the [docs](docs/index.md)

## releasing

Run e.g. on main: `mvn -B release:prepare` e.g. via [![Gitpod ready-to-code](https://img.shields.io/badge/Gitpod-ready--to--code-blue?logo=gitpod)](https://gitpod.io#https://github.com/baloise/repository-template-java)

Subsequently the GitHub action worksflow "create release" will pick up the published tag and release and deploy the artifacts in the Github package registry.
