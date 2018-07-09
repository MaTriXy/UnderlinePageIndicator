# Underline Page Indicator

![Demo](https://github.com/dcampogiani/UnderlinePageIndicator/blob/master/demo.gif?raw=true)

This indicator will underline each tab text with, morphing its size while scrolling


## How to use

Add TabLayout and UnderlinePageIndicator to XML:

```xml
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    android:orientation="vertical"
    tools:context=".MainActivity">

    <android.support.design.widget.TabLayout
        android:id="@+id/tabs"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        app:tabIndicatorHeight="0dp"
        app:tabMode="fixed" />

    <com.danielecampogiani.underlinepageindicator.UnderlinePageIndicator
        android:id="@+id/indicator"
        android:layout_width="match_parent"
        android:layout_height="2dp" />


    <android.support.v4.view.ViewPager
        android:id="@+id/pager"
        android:layout_width="match_parent"
        android:layout_height="match_parent" />

</LinearLayout>
```

Style TabLayout with ```app:tabIndicatorHeight="0dp"``` and  ```app:tabMode="fixed"```

Setup with ViewPager

```kotlin
pager.adapter = Adapter(...)
indicator.setTabLayoutAndViewPager(tabs, pager)
```

Checkout the app project for an example.

## Thanks
 - [ViewPagerIndicator](https://github.com/JakeWharton/ViewPagerIndicator)
