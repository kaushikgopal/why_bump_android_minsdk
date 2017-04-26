You should always keep bumping your minSdk version for the Android app. Newer API levels (OS versions in Android) come with more fixes and features that you can start using. But if you're required to make that case, this document should help.

What you get:

__Features:__

Android Studio currently already provides a neat listing (with a picker and all) everytime you create an Android Studio project. For the lazy, i'll include a screenshot from each of those APIs.

If there's a feature not on that list, that you think is worth calling out, send a PR and we'll add it here!

__Bugs:__

Sometimes there are terrible bugs/limitations with OS versions (or the phone manufacturer variant of that OS). If you notice these and want to make the world for AndroidDev better, send a PR and we'll add it here!

__Features that are not user facing:__

There are programmer facing features like language features (Lambdas, method references, try with resources) that are hugely critical for developers. These are usually not called out in that new Android Studio project creator listing. If you know of these and want to make the lives of other AndroidDev better, send a PR!

# minSdkVersion 24 (7.0) Nougat

* [Multi-Window Support](https://developer.android.com/guide/topics/ui/multi-window.html)
* [Java 8 language features and API](https://developer.android.com/studio/preview/features/java8-support.html) (Note: some of the known and loved features like Lambdas and Method references are already available via Android Studio. However certain other features like Streams, functions, FunctionalInterface etc. are only available from 24. See [linked doc](https://developer.android.com/studio/preview/features/java8-support.html) for details).

# minSdkVersion 23 (6.0) Marshmallow

![api 23 features](https://github.com/kaushikgopal/why_bump_android_minsdk/blob/master/api_23_m.png "API 23 features")
* Removes Apache HTTP client. Compulsory to use [HttpURLConnection](https://developer.android.com/reference/java/net/HttpURLConnection.html) class for API calls.
* [Runtime permission](https://developer.android.com/training/permissions/requesting.html).
* Removes programmatic access to the device’s local hardware identifier like MAC or Bluetooth address.(From now onwards [WifiInfo.getMacAddress()](https://developer.android.com/reference/android/net/wifi/WifiInfo.html#getMacAddress()) and the [BluetoothAdapter.getAddress()](https://developer.android.com/reference/android/bluetooth/BluetoothAdapter.html#getAddress()) methods will return a constant value of `02:00:00:00:00:00`.)

# minSdkVersion 22 (5.1) Lollipop

![api 22 features](https://github.com/kaushikgopal/why_bump_android_minsdk/blob/master/api_22_l.png "API 22 features")

# minSdkVersion 21 (5.0) Lollipop

![api 21 features](https://github.com/kaushikgopal/why_bump_android_minsdk/blob/master/api_21_l.png "API 21 features")

* [Native support for elevation & view clipping](https://developer.android.com/training/material/shadows-clipping.html)
* [Native `VectorDrawable` and `AnimatedVectorDrawable` support](https://developer.android.com/guide/topics/graphics/vector-drawable-resources.html) (none of the ugly workarounds required if you use the native version. [Read this post](https://medium.com/@chrisbanes/appcompat-v23-2-age-of-the-vectors-91cbafa87c88)).
* [Native `JobScheduler` use](https://developer.android.com/reference/android/app/job/JobScheduler.html) (i.e. if you'd rather not use [Firebase JobDispatcher](https://github.com/firebase/firebase-jobdispatcher-android))
* [Optimized multidex in dev builds](https://developer.android.com/studio/build/multidex.html#dev-build) (Faster build times)
* ART runtime support.
* 64-bit NDK support.
* Introduced [Camera2](https://developer.android.com/reference/android/hardware/camera2/package-summary.html) API.

# minSdkVersion 19 (4.4 - 4.4.4) KitKat

![api 19 features](https://github.com/kaushikgopal/why_bump_android_minsdk/blob/master/api_19_k.png "API 19 features")

* Chromium based WebView, which is still a WebView..., but far less horrible, fragmented and vulnerable compared to the WebViews before 4.4.
* "Lossless" WebP support. Actually [lossless was made available in API 18](https://developer.android.com/studio/write/convert-webp.html) but [when those in the know were asked for suggested minSdk (for WebP), they suggested 19](https://twitter.com/Eric_Cochran/status/855446820708679680).
* Java 7 [try-with-resources](https://issuetracker.google.com/issues/36999599#comment3)


# minSdkVersion 18 (4.3.x) Jelly Bean

![api 18 features](https://github.com/kaushikgopal/why_bump_android_minsdk/blob/master/api_18_j.png "API 18 features")

# minSdkVersion 17 (4.2.x) Jelly Bean MR1

![api 17 features](https://github.com/kaushikgopal/why_bump_android_minsdk/blob/master/api_17_j.png "API 17 features")

* Samsung __bug__ with RTL (you need to have some padding on everything, otherwise Samsung will blow up cause they overrode or had their own version of rtl before Android had it built in?). Listen to [this Fragmented episode with Dan Lew](fragmentedpodcast.com/episodes/049) where he talks about it.
* [WebP support](https://developer.android.com/guide/topics/media/media-formats.html) (but not lossless, see note in API 19)

# minSdkVersion 16 (4.1.x) Jelly Bean

![api 16 features](https://github.com/kaushikgopal/why_bump_android_minsdk/blob/master/api_16_j.png "API 16 features")

* Sony has a `setPaddingRelative` that [risks a stackoverflow error](https://twitter.com/seebrock3r/status/855735534223855616).

# minSdkVersion 14 (4.0.1 - 4.0.2) Ice Cream Sandwich

* Holo theme introduced
* USB On-The-Go support.

# minSdkVersion < 14

No, __don't use anything below 14 please__.

# Resources

* [Mapping between API Levels and commercial Android OS Versions](https://source.android.com/source/build-numbers)
* [Android OS platform distribution dashboard (maintained by Google)](https://developer.android.com/about/dashboards/index.html)
* [Wikipedia Android version history by API level](https://en.wikipedia.org/wiki/Android_version_history#Version_history_by_API_level) (has a pretty detailed feature list)
