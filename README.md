FadingActionBar
==================

FadingActionBar is a library which implements the cool fading action bar effect that can be seen in the new Play Music app.

This library uses the techniques outlined by Cyril Mottier in [a popular blog post][1].

The three most commonly used action bar implementations are supported: stock (API 11+), ActionBarCompat and ActionBarSherlock.

![Example Image][2]

Try out the sample application:

<a href="https://play.google.com/store/apps/details?id=com.manuelpeinado.fadingactionbar.demo">
  <img alt="Android app on Google Play"
       src="https://developer.android.com/images/brand/en_app_rgb_wo_45.png" />
</a>

Or browse the [source code of the sample application][3] for a complete example of use.

Including in your project
-------------------------

The library is pushed to Maven Central as a AAR, so you just need to add the following dependency to your `build.gradle`.
    
    dependencies {
        compile 'com.github.manuelpeinado.fadingactionbar:fadingactionbar:3.0.0'
    }
    
If your project doesn't use the stock action bar, but one of the compatibility implementations, you would use the following:

    dependencies {
        // Use the following if your project uses ActionBarCompat
        compile 'com.github.manuelpeinado.fadingactionbar:fadingactionbar-abc:3.0.0'
        // Or the following if your project uses ActionBarSherlock
        compile 'com.github.manuelpeinado.fadingactionbar:fadingactionbar-abs:3.0.0'
    }


Usage
-----

Using the library is really simple, just look at the source code of the provided samples:

* [If your content should be in a `ScrollView`][4].
* [If your content should be in a `ListView`][5].

You can even use the library [from a fragment][6], which is useful when implementing a dual phone/tablet layout.

See the demos included in the sample application for a complete overview of the features supported by the library.

Known Issues
------------

There are important issues with the library and ListViews. More specifically, the following scenarios are known to be broken:

* The activity is re-created due to a configuration change.
* The `notifyDataSetChanged` method of the ListView is invoked by the application.

If none of these two scenarios take place in your application (kind of unlikely, I know) then your are good to go. Otherwise, I'd strongly suggest you stick to having your content in a ScrollView until a solution to these issues is found.

For more information, see [this][7].

Acknowledgements
--------------------

* Thanks to [Cyril Mottier][8] for sharing the techniques that make this library possible.
* Thanks to [Antonio Leiva][9] for writing the Navigation Drawer sample.


Who's using it
--------------

* [#ДАНСwithme][10]. This app attempts to organise information from various social network streams into a single source.

* [Pearl Jam Lyrics][11]. Unofficial app for Pearl Jam fans that want to have all the lyrics of their favorite band in the palm of their hands.

*Does your app use FadingActionBar? If you want to be featured on this list drop me a line.*


Developed By
--------------------

Manuel Peinado Gallego - <manuel.peinado@gmail.com>

<a href="https://twitter.com/mpg2">
  <img alt="Follow me on Twitter"
       src="https://raw.github.com/ManuelPeinado/NumericPageIndicator/master/art/twitter.png" />
</a>
<a href="https://plus.google.com/106514622630861903655">
  <img alt="Follow me on Google+"
       src="https://raw.github.com/ManuelPeinado/NumericPageIndicator/master/art/google-plus.png" />
</a>
<a href="http://www.linkedin.com/pub/manuel-peinado-gallego/1b/435/685">
  <img alt="Follow me on LinkedIn"
       src="https://raw.github.com/ManuelPeinado/NumericPageIndicator/master/art/linkedin.png" />


License
-----------

    Copyright 2013 Manuel Peinado

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.




 [1]: http://cyrilmottier.com/2013/05/24/pushing-the-actionbar-to-the-next-level/
 [2]: https://raw.github.com/ManuelPeinado/FadingActionBar/master/art/readme_pic.png
 [3]: https://github.com/ManuelPeinado/FadingActionBar/tree/master/samples/stock
 [4]: https://github.com/ManuelPeinado/FadingActionBar/blob/master/samples/stock/src/com/manuelpeinado/fadingactionbar/demo/ScrollViewActivity.java
 [5]: https://github.com/ManuelPeinado/FadingActionBar/blob/master/samples/stock/src/com/manuelpeinado/fadingactionbar/demo/ListViewActivity.java
 [6]: https://github.com/ManuelPeinado/FadingActionBar/blob/master/sample/src/com/manuelpeinado/fadingactionbar/demo/SampleFragment.java
 [7]: https://github.com/ManuelPeinado/FadingActionBar/blob/master/sample/src/com/manuelpeinado/fadingactionbar/demo/SampleFragment.java
 [8]: http://cyrilmottier.com
 [9]: https://github.com/antoniolg
 [10]: https://play.google.com/store/apps/details?id=com.yavorivanov.android.danswithme 
 [11]: https://play.google.com/store/apps/details?id=com.juannale.pearljamlyricsapp


