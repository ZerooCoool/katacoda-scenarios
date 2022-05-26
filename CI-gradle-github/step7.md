# Using Maven Publish with Gradle
In this final part of the tutorial we will explain how you would go about deploying your Gradle build artifact to a Maven repository. We will not actually add the code to the build file and deploy our build to a Maven repository, but give an overview of how it would be done if you have a maven repository. This is just to make you understand how Gradle can be combined with other tools.

Gradle can be used in combination with Maven plugins to deploy build artifacts to a Maven repository. In this tutorial we will give an overview of how Maven works with gradle. To do this we need to include the Maven Publish Plugin in our `katacoda-code/app/build.gradle`{{open}} script.

<pre class="file" data-filename="./katacoda-code/app/build.gradle" data-target="insert"  data-marker="// add maven-publish">
id 'maven-publish'
</pre>

The Maven Publish Plugin works with [MavenPublication](https://docs.gradle.org/current/dsl/org.gradle.api.publish.maven.MavenPublication.html) and [MavenArtifactRepository](https://docs.gradle.org/current/dsl/org.gradle.api.artifacts.repositories.MavenArtifactRepository.html) repositories. The plugin will create an extension of [PublishingExtension](https://docs.gradle.org/current/dsl/org.gradle.api.publish.PublishingExtension.html) which you can then configure in the
<pre>
publishing {
  ...
}
</pre>

script block in `katacoda-code/app/build.gradle`{{open}}.


# Maven Publication
A Maven publication represents how Gradle publishes an artifact in Maven format. More specifically it represents a set of files and a POM. The publishing extenstion provides a container named `publications` where it can be configured in the
<pre>
publishing {
  publications {
    ...
  }
}
</pre>

script block in `katacoda-code/app/build.gradle`{{open}}. The publications are defined by the MavenPublication type mentioned earlier and are added as followed:
<pre>
publishing {
  publications {
    <publication-name>(MavenPublication) {
        from <software-component>
        artifact <artifact-generating-task>
        artifact(source, configuration)
        pom(configuration)
    }
  }
}
</pre>



# Maven Repository
In the Maven publish plugin repositories are defined within the `repositories` container of the publishing extension in `katacoda-code/app/build.gradle`{{open}}. The Maven repositories that your work will be published to are defined by the MavenArtifactRepository type mentioned earlier and are added as followed:
<pre>
publishing {
  ...
  repositories {
    //
    // repositories to publish to
    //
    maven {
      url '...'
      credentials {
        username '...'
        password '...'
      }
      authentication {
        basic(BasicAuthentication)
      }
    }
  }
}
</pre>

That is how you would configure Gradle to publish artifacts to a Maven repository! You just configure your options in the publishing extension with your data and locations.
