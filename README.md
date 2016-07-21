PinchZoom
===============
 
[![](https://img.shields.io/badge/Android%20Arsenal-PinchZoom-brightgreen.svg)]() [![](https://jitpack.io/v/com.github.emrekose26/pinchzoom.svg)](https://jitpack.io/#com.github.emrekose26/pinchzoom)

PinchZoom is a supported library the pinch gestures for Android

### Gradle

In your ``build.gradle`` file:

Add it in your root build.gradle at the end of repositories
```
allprojects {
    repositories {
        maven { url "https://jitpack.io" }
    }
}	
```
Add the dependency
```
dependencies {
    ...
    compile 'com.emrekose:pinchzoom'
}
```

### Usage


In your Activity class :

```java
public class MainActivity extends AppCompatActivity {

    private ImageView imageView;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        imageView = (ImageView)findViewById(R.id.imageView);

        imageView.setOnTouchListener(new Touch());
    }
}
    
```

If you want to change default max and min zoom values

```
   imageView.setOnTouchListener(new Touch(2f,6f));
```

In your xml file : 
```xml
<ImageView
    android:id="@+id/imageView
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:scaleType="matrix" />
```



### Contributing

* Check out the latest master to make sure the feature hasn't been implemented or the bug hasn't been fixed yet
* Check out the issue tracker to make sure someone already hasn't requested it and/or contributed it
* Fork the project
* Start a feature/bugfix branch
* Commit and push until you are happy with your contribution
* Make sure to add tests for it. This is important so I don't break it in a future version unintentionally.


### Copyright and license

Code and documentation copyright 2016 Emre Köse
Code released under the [MIT license](https://github.com/emrekose26/PinchZoom/blob/master/LICENSE.md).