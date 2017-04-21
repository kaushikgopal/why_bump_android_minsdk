You should always keep bumping your minSdk version for the Android app. Newer API levels (OS versions in Android) come with more fixes and features that you can start using.

Please feel free to generously contribute PRs to this project. 

This is a list of feature you get by bumping your minSdk (and more importantly a bunch of problems you avoid):


# minSdkVersion 24 (7.0) Nougat

* [Multi-Window Support](https://developer.android.com/guide/topics/ui/multi-window.html)
* [Java 8 language features and API](https://developer.android.com/studio/preview/features/java8-support.html) (Note: some of the known and loved features like Lambdas and Method references are already available via Android Studio. However certain other features like Streams, functions, FunctionalInterface etc. are only available from 24. See [linked doc](https://developer.android.com/studio/preview/features/java8-support.html) for details).

# minSdkVersion 21 (5.0) Lollipop

* [Material design theme introduced](https://developer.android.com/training/material/theme.html)
* [Native support for elevation & view clipping](https://developer.android.com/training/material/shadows-clipping.html)
* [Native `VectorDrawable` and `AnimatedVectorDrawable` support](https://developer.android.com/guide/topics/graphics/vector-drawable-resources.html) (none of the ugly workarounds required if you use the native version. [Read this post](https://medium.com/@chrisbanes/appcompat-v23-2-age-of-the-vectors-91cbafa87c88)).
* [Native `JobScheduler` use](https://developer.android.com/reference/android/app/job/JobScheduler.html) (i.e. if you'd rather not use [Firebase JobDispatcher](https://github.com/firebase/firebase-jobdispatcher-android))
* [Optimized multidex in dev builds](https://developer.android.com/studio/build/multidex.html#dev-build) (Faster build times)

# minSdkVersion 19 (4.4 - 4.4.4) KitKat

* [`ObjectAnimator.pause` support](http://stackoverflow.com/questions/25231707/how-to-resume-and-pause-objectanimator-in-android-for-api-levels-below-19)
* Ability to use immersive mode : SYSTEM_UI_FLAG_IMMERSIVE (Android 4.4 comes with a new immersive mode that hides status bar and navigation bar in your app. Basically it hides everything from screen except your app).
* Chromium based WebView, which is still a WebView..., but far less horrible, fragmented and vulnerable compared to the WebViews before 4.4.
* Java 7 [try-with-resources](https://issuetracker.google.com/issues/36999599#comment3)

# minSdkVersion 18 (4.3.x) Jelly Bean

* [Bluetooth Low Energy (BLE) is introduced](https://developer.android.com/guide/topics/connectivity/bluetooth-le.html)
* [Android Keystore Provider](https://developer.android.com/training/articles/keystore.html#UsingAndroidKeyStore)

# minSdkVersion 17 (4.2.x) Jelly Bean MR1

* Only need to use start/end layout attributes (vs also adding left/right respectively)
* Samsung __bug__ with RTL (you need to have some padding on everything, otherwise Samsung will blow up cause they overrode or had their own version of rtl before Android had it built in?). Listen to [this Fragmented episode with Dan Lew](fragmentedpodcast.com/episodes/049) where he talks about it.
* Native [Nested Fragments](https://developer.android.com/about/versions/android-4.2.html#NestedFragments) (common usecase: ViewPager used inside a fragment, and the ViewPager itself is provided child Fragments for screen) [exists in support lib].

# minSdkVersion 16 (4.1.x) Jelly Bean


# minSdkVersion 14 (4.0.1 - 4.0.2) Ice Cream Sandwich

* Holo theme introduced

# Resources

* [Mapping between API Levels and commercial Android OS Versions](https://source.android.com/source/build-numbers)
* [Android OS platform distribution dashboard (maintained by Google)](https://developer.android.com/about/dashboards/index.html)
* [Wikipedia Android version history by API level](https://en.wikipedia.org/wiki/Android_version_history#Version_history_by_API_level) (has a pretty detailed feature list)
