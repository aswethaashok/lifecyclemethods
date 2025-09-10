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

![WhatsApp Image 2025-09-10 at 10 05 09_97274880](https://github.com/user-attachments/assets/78487d20-55b8-40de-b830-61f3a2639452) ![WhatsApp Image 2025-09-10 at 10 05 09_9b20657f](https://github.com/user-attachments/assets/0643eae3-7501-4ce5-8885-38ef0d0144da) ![WhatsApp Image 2025-09-10 at 10 05 10_f192b7ac](https://github.com/user-attachments/assets/c222c6c7-5163-4002-be58-f62f7cbaa70f)  ![WhatsApp Image 2025-09-10 at 10 05 10_17480b3f](https://github.com/user-attachments/assets/374b0e1b-0f69-4a34-ab3b-a0f511e8012d)  ![WhatsApp Image 2025-09-10 at 10 05 08_3632d692](https://github.com/user-attachments/assets/423f7472-949b-492f-9538-392121782113)


## RESULT
Thus a Simple Android Application create a HelloWorld Activity using all lifecycles methods to display messages using Android Studio is developed and executed successfully.
