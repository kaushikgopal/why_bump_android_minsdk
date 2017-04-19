You should always keep bumping your minSdk version for the Android app. Newer API levels (OS versions in Android) come with more fixes and features that you can start using.

This is a list of feature you get by bumping your minSdk (and more importantly a bunch of problems you avoid):


# minSdkVersion 21 (5.0) Lollipop

* [Material design Theme introduced](https://developer.android.com/training/material/theme.html)

# minSdkVersion 19 (4.4 - 4.4.4) KitKat

* [`ObjectAnimator.pause` support](http://stackoverflow.com/questions/25231707/how-to-resume-and-pause-objectanimator-in-android-for-api-levels-below-19)

# minSdkVersion 17 (4.2.x) Jelly Bean

* Samsung bug with RTL (you need to have some padding on everything, otherwise Samsung will blow up cause they overrode or had their own version of rtl before Android had it built in?). Listen to [this Fragmented episode with Dan Lew](fragmentedpodcast.com/episodes/049) where he talks about it.

# Resources

* [Mapping between API Levels and commercial Android OS Versions](https://source.android.com/source/build-numbers)
* [Android OS platform distribution dashboard (maintained by Google)](https://developer.android.com/about/dashboards/index.html)
