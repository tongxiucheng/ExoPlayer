# ExoPlayer Readme #

## Description ##

ExoPlayer is an application level media player for Android. It provides an
alternative to Android’s MediaPlayer API for playing audio and video both
locally and over the Internet. ExoPlayer supports features not currently
supported by Android’s MediaPlayer API, including DASH and SmoothStreaming
adaptive playbacks. Unlike the MediaPlayer API, ExoPlayer is easy to
customize and extend, and can be updated through Play Store application
updates.
ExoPlayer 是 Android 上一个应用级的媒体播放器。它为 Android MediaPlayer 的 API 在播放本地或在线的视频与音频上提供了一个候选。ExoPlayer 支持一些 Android MediaPlayer API 无法提供的特性，包括 DASH 和 SmoothStreaming 自适应回放，持久的高速缓存和自定义渲染器。不像 MediaPlayer API，EXOPlayer 很容易定制和扩展，而且它可以通过 Play Store 更新升级。

## News ##

Read news, hints and tips on the [news][] page.

[news]: https://google.github.io/ExoPlayer/news.html

## Documentation ##

* The [developer guide][] provides a wealth of information to help you get
started.
* The [class reference][] documents the ExoPlayer library classes.
* The [release notes][] document the major changes in each release.

[developer guide]: https://google.github.io/ExoPlayer/guide.html
[class reference]: https://google.github.io/ExoPlayer/doc/reference
[release notes]: https://github.com/google/ExoPlayer/blob/dev/RELEASENOTES.md

## Project branches ##

  * The [master][] branch holds the most recent minor release.
  * Most development work happens on the [dev][] branch.
  * Additional development branches may be established for major features.

[master]: https://github.com/google/ExoPlayer/tree/master
[dev]: https://github.com/google/ExoPlayer/tree/dev

## Using Eclipse ##

The repository includes Eclipse projects for both the ExoPlayer library and its
accompanying demo application. To get started:

  1. Install Eclipse and setup the [Android SDK][].

  1. Open Eclipse and navigate to File->Import->General->Existing Projects into
     Workspace.

  1. Select the root directory of the repository.

  1. Import the ExoPlayerDemo and ExoPlayerLib projects.

[Android SDK]: http://developer.android.com/sdk/index.html


## Using Gradle ##

ExoPlayer can also be built using Gradle. You can include it as a dependent project and build from source:

```
// settings.gradle
include ':app', ':..:ExoPlayer:library'

// app/build.gradle
dependencies {
    compile project(':..:ExoPlayer:library')
}
```

If you want to use ExoPlayer as a jar, run:

```
./gradlew jarRelease
```

and copy library.jar to the libs-folder of your new project.

The project is also available on [jCenter](https://bintray.com/google/exoplayer/exoplayer/view):

```
compile 'com.google.android.exoplayer:exoplayer:rX.X.X'
```

Where `rX.X.X` should be replaced with the desired version.
