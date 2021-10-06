TopSheet - a "top" version of BottomSheetBehavior
=========================================

TopSheetBehavior is a code based on https://github.com/MedveDomg/AndroidTopSheet. 

The major change is that this project has taken into account the latest changes until Android SDK 30 (2021 October) and has been migrated it to AndroidX so there are no more dependencies on the old Android Support packages.

Aside from that, some functions that were deprecated on the original project, have been replaced with the newer counterparts.

TopSheetBehavior
-----

Setting state programmatically:
```java
View sheet = findViewById(R.id.top_sheet);
TopSheetBehavior.from(sheet).setState(TopSheetBehavior.STATE_EXPANDED);
```

XML layout example:
You'd have to change ```com.YOUR_PACKAGE_NAMESPACE.TopSheetBehavior``` in favour of your package namespace.

```XML layout
<?xml version="1.0" encoding="utf-8"?>
<androidx.coordinatorlayout.widget.CoordinatorLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    android:layout_width="match_parent"
    android:layout_height="wrap_content">

    <androidx.core.widget.NestedScrollView
        android:id="@+id/routeCaptionBottomSheet"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:background="@android:color/white"
        app:layout_behavior="com.YOUR_PACKAGE_NAMESPACE.TopSheetBehavior">

        <!-- YOUR LAYOUT GOES HERE -->

    </androidx.core.widget.NestedScrollView>

</androidx.coordinatorlayout.widget.CoordinatorLayout>
```

TopSheetDialog
-----
```java
TopSheetDialog dialog = new TopSheetDialog(this);
dialog.setContentView(R.layout.sheet_content);
dialog.show();
```


License
-------

Copyright 2016 Andrea Maglie

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
