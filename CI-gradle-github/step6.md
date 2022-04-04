# Using Maven Publish with Gradle

Gradle can be used in combination with Maven plugins to deploy build artifacts to a Maven repository. To do this we need to include the Maven Publish Plugin in our build script.

<pre class="file" data-filename="./katacoda-code/app/build.gradle" data-target="insert"  data-marker="// add maven-publish">
plugins {
    id 'maven-publish'
}
</pre>

The Maven Publish Plugin works with [MavenPublication](https://docs.gradle.org/current/dsl/org.gradle.api.publish.maven.MavenPublication.html) and [MavenArtifactRepository](https://docs.gradle.org/current/dsl/org.gradle.api.artifacts.repositories.MavenArtifactRepository.html) repositories. 
