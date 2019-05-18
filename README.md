[![Build Status](https://travis-ci.org/rneureuther1/cyclonedx-gradle-plugin.svg?branch=master)](https://travis-ci.org/rneureuther1/cyclonedx-gradle-plugin)
[![License](https://img.shields.io/badge/license-Apache%202.0-brightgreen.svg)][License]
[![Website](https://img.shields.io/badge/https://-cyclonedx.org-blue.svg)](https://cyclonedx.org/)
[![Group Discussion](https://img.shields.io/badge/discussion-groups.io-blue.svg)](https://groups.io/g/CycloneDX)
[![Twitter](https://img.shields.io/twitter/url/http/shields.io.svg?style=social&label=Follow)](https://twitter.com/CycloneDX_Spec)


CycloneDX Gradle Plugin
=========

The CycloneDX Gradle plugin creates an aggregate of all dependencies and transitive dependencies of a project 
and creates a valid CycloneDX bill-of-material document from the results. CycloneDX is a lightweight BoM 
specification that is easily created, human readable, and simple to parse. The resulting bom.xml can be used
with tools such as [OWASP Dependency-Track](https://dependencytrack.org/) for the continuous analysis of components.

Gradle Usage
-------------------
First, build and publish this plugin to your local maven repository
```
gradle publishToLocalMaven
```

Second, in the existing project's _settings.gradle_, ensure that the plugins are resolved from local maven
```
pluginManagement {
  repositories {
      mavenLocal()
  }
}
```

Third, in the existing project's _build.gradle_, ensure that the plugin is applied
```
plugins { 
    id 'org.cyclonedx.gradle.bom' version "1.0.0-SNAPSHOT"
}
```

Fourth, in the existing project's directory, call the appropriate task (in development)
```
gradle cyclonedxBom
```


Copyright & License
-------------------

CycloneDX Gradle Plugin is Copyright (c) Steve Springett. All Rights Reserved.

Permission to modify and redistribute is granted under the terms of the Apache 2.0 license. See the [LICENSE] file for the full license.

[License]: https://github.com/CycloneDX/cyclonedx-gradle-plugin/blob/master/LICENSE
