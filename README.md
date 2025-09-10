## Ex.No:1 To create a HelloWorld Activity using all lifecycles methods to display messages.


## AIM:

To create a HelloWorld Activity using all lifecycles methods to display messages using Android Studio.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:

Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as HelloWorld and click Next. 

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Display message give in MainActivity file.

Step 7: Save and run the application.

## PROGRAM:
```
/*
Program to print the text “Hello World”.
Developed by: SWETHA A
Registeration Number : 212223220114
*/
```

## OUTPUT

activity_main.xml
```
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:orientation="vertical"
    android:gravity="center"
    android:background="@color/black"
    android:layout_width="match_parent"
    android:layout_height="match_parent">

    <TextView
        android:id="@+id/welcomeText"
        android:text="@string/hello_world"
        android:textSize="28sp"
        android:textStyle="bold"
        android:textColor="#2196F3"
        android:fontFamily="cursive"
        android:layout_margin="16dp"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"/>
</LinearLayout>

```
MainActivity.java

```
package com.example.myex001;

import android.os.Bundle;
import android.widget.TextView;
import android.widget.Toast;
import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {

    TextView welcomeText;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        welcomeText = findViewById(R.id.welcomeText);

        showToast(getString(R.string.on_create));
    }

    @Override
    protected void onStart() {
        super.onStart();
        showToast(getString(R.string.on_start));
    }

    @Override
    protected void onResume() {
        super.onResume();
        showToast(getString(R.string.on_resume));
    }

    @Override
    protected void onPause() {
        super.onPause();
        showToast(getString(R.string.on_pause));
    }

    @Override
    protected void onStop() {
        super.onStop();
        showToast(getString(R.string.on_stop));
    }

    @Override
    protected void onRestart() {
        super.onRestart();
        showToast(getString(R.string.on_restart));
    }

    @Override
    protected void onDestroy() {
        super.onDestroy();
        showToast(getString(R.string.on_destroy));
    }

    private void showToast(String message) {
        Toast.makeText(this, message, Toast.LENGTH_SHORT).show();
    }
}

```
strings.xml

```
<resources>
    <string name="app_name">myex001</string>
    <string name="hello_world">Hello World!</string>
    <string name="profile_desc">Profile Picture</string>

    
    <string name="on_create">Application Created</string>
    <string name="on_start">onStart called</string>
    <string name="on_resume">Application Resumed</string>
    <string name="on_pause">Application Paused</string>
    <string name="on_stop">Application Stopped</string>
    <string name="on_restart">Application Restarted</string>
    <string name="on_destroy">Application Destroyed</string>
</resources>

```
<img width="1918" height="1078" alt="Screenshot 2025-09-10 100313" src="https://github.com/user-attachments/assets/f7924171-5a15-4b2f-a060-0b1dc8574fbb" />


<img width="1917" height="1079" alt="Screenshot 2025-09-10 100323" src="https://github.com/user-attachments/assets/3cc9fcdb-05ed-4db6-85c8-49b2d1f6253f" />

OnResume

<img width="1917" height="1079" alt="Untitled design" src="https://github.com/user-attachments/assets/c5ea09b0-774e-4005-bd41-f8ce99e3495e" />

OnStart

<img width="1917" height="1079" alt="Untitled design (1)" src="https://github.com/user-attachments/assets/b8ac763f-5b2a-45f7-92e9-38c0a0283dd6" />

OnRestarted

<img width="1917" height="1079" alt="Untitled design (2)" src="https://github.com/user-attachments/assets/cf51e8f1-0b99-4b6e-b380-f475935702b7" />

OnStop

<img width="1917" height="1079" alt="Untitled design (3)" src="https://github.com/user-attachments/assets/5266f1c4-da5b-428d-8bc2-fab896999f9d" />

OnPause

<img width="1917" height="1079" alt="Untitled design (4)" src="https://github.com/user-attachments/assets/c230b24d-134a-42e6-9b07-fd7132974f71" />



## RESULT
Thus a Simple Android Application create a HelloWorld Activity using all lifecycles methods to display messages using Android Studio is developed and executed successfully.
