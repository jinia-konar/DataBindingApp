#### Simple App for the working flow of data binding

Using data binding can lead to faster development times, faster execution times and more readable and maintained code. Android data binding generates binding classes at compile time for layouts.

Android data binding is part of an [android jetpack](https://developer.android.com/jetpack) (a collection of tools that lets developers create high-quality software). If you’re a developer with any knowledge in android app development, you’ll be familiar with **findViewById()**, the method of declaring views in an activity. Let's say that I'm building an app that displays my name in textView. Here I illustrate both ways, with and without data binding, of defining a view.
##### Without Data Binding
```
TextView myName = findViewById(R.id.m);
myName.setText(“XYZ”)
```

##### With Data Binding
```
<TextView
    android:text="@{modelClass.userName}" />
```

I add a small line of code in your build.gradle to enable data binding in my project:
```
dataBinding{
   enabled true
}
```

In order to implement data binding, we need to wrap the whole layout in <layout></layout> tag, like this:
```
<?xml version="1.0" encoding="utf-8"?>
<layout>
    <RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
        xmlns:tools="http://schemas.android.com/tools"
        android:layout_width="match_parent"
        android:layout_height="match_parent">

        <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_centerInParent="true"
            android:gravity="center"
            android:text="Hello World!!"/>

    </RelativeLayout>
</layout>
```

There is more in data binding like one-way and two-way data binding which you can learn by referring the below youtube video link.

For reference:-
* [Data Binding with LiveData (Two-way & One-way) – Android Kotlin Tutorial](https://resocoder.com/2018/09/21/data-binding-with-livedata-two-way-one-way-android-kotlin-tutorial/)
* [Youtube Video](https://youtu.be/T-nQP9fidKU)
