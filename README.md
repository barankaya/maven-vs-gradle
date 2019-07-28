# maven-vs-gradle

## Gradle vs Maven (or Both)

The world of build tools evolved from simple compilation (gcc) to make files, then evolution of ant(+ivy) and Maven, now the latest build tool is Gradle.

It’s always a puzzle which build tool to choose – Maven, Gradle or both. Sometime it’s first time project setup or it could be migration from existing tool, but it’s always a debate to choose one or the other.

There have been lot of talks and discussions on Gradle, Maven (and/or Gradle vs maven). There is buzz around that Android/Google adopted Gradle as its standard build tool.

Here, I would like to explore the possibilities of adopting Gradle or Maven (Or both), Intentionally i am keeping ant+ivy out of this talk.

Lets take a look at the details on why Android may have adopted Gradle

**Key points for Google to go ahead with Gradle for their android development are:**

- Create multiple APKs for your app with different features using the same project.(create several variants of an application)
- Reuse code and resources.
- Customize, configure, and extend the build process.
- Customized integration with their own IDE Android Studio.
- Single build tools to support multiple languages.

**What we may be looking from build tools**

- How easy is the learning curve?
- How fast are different builds with each tool?
- How complex is it to create and maintain the build script?
- How many plugins exist and how simple is it to customize your own plugins?
- How good is the community and documentation for each tool?
- How well does each tool integrate with developer tools? (IDE, App Server, CI server).

Lets take a look at Maven and Gradle build tools on basis of above points and give them score as per our use case.

Here is the Tabular comparison for each point between Maven and Gradle.
			
Points | Maven | Gradle | Score
------------ | ------------- | ------------- | -------------
How easy is the initial learning curve | Maven is XML based tool, XML is very commonly used/known. If existing project are using maven then developers are comfortable with the system.| Gradle is [DSL](http://dsl-course.org) based system and need to learn explicitly. Developers need to learn new system from beginning if they are not familier | Maven – 8/10Gradle – 5/10 
How fast are different builds with each tool ||Taken a report from zeroturnaround, they have done detail analysis of the speed of builds with both built tools and found maven and gradle are close enough on build timings. | Maven – 8/10Gradle – 9/10
How complex is it to create and maintain the build script?|Maven build scripts are xml based, which has predefined structure and only one way to write.So it makes it more standard and less flexible.|Gradle has its own DSL which is introduced by Gradleitself and tightly connected to Gradle internals But its flexible and simple and short|Maven – 5/10Gradle – 7/10
How many plugins exist and how simple is it to customize your own plugins?|Maven is called “plugin execution framework” Hundreds of plugins exist for Maven and you can create your own plugin is simple.|Gradle’s architecture is also plugin-based, It’s easy to write plugins But availability of plugin in community may not be ease.|Maven – 8/10Gradle – 6/10
How good is the community and documentation for each tool?|Maven is in the market for very long time, Documentation is good, Lots of resources and help available in open community and forum.|Gradle is very recent. It is open source but still under control of gradleware. They have option for commercial support.|Maven – 9/10Gradle – 8/10
How well does each tool integrate with developer tools? (IDE, App Server, CI server).|With many years of background Maven has full support to almost each tool and every category (IDE, App Server, CI).|Lacking in the App Server and CI ServerCategories, mainly due to newness.|Maven – 9/10Gradle – 5/10

**Total Score**

Maven – 47/60

Gradle – 40/60

## Choices

**Gradle**

You may not be using other features which are used by Google for android development as those features may or may not match with your needs, however Gradle is essentially emerging as a popular tool and you may definitely want to have a look at it.


**Maven**

Maven is widely used and has robust defined workflow around it. Developers are very familiar with the system. However this may not be a viable option as android development needs to use Gradle.


**Maven and Gradle (both)**

This would be the one option for a company with a wide range of development options. It may give developers flexibility to adopt tools as per their choice with a given workflow.

[Reference #](https://devops.com/puzzle-gradle-maven/)
