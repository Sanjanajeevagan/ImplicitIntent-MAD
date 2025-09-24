# Ex.No:3a Develop program to create a text field and a button “Navigate”. When you enter “www.gmail.com” and press navigate button it should open google page using Implicit Intents.


## AIM:

To create a navigate button using Implicit Intent to display the gmail page using Android Studio.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:



## PROGRAM:
```

Program to print the text “Implicitintent”.
Developed by: Sanjana J
Registeration Number :212224230240

```
## Activity_main.xml

```
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:padding="16dp"
    android:gravity="center">

    <EditText
        android:id="@+id/etUrl"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Enter URL here"
        android:inputType="textUri"
        android:padding="12dp"
        android:layout_marginBottom="20dp"/>

    <Button
        android:id="@+id/btnImplicit"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Open URL"
        android:padding="16dp"/>

</LinearLayout>
```
##  Main_activity.java

```
package com.example.anint;

import android.content.Intent;
import android.net.Uri;
import android.os.Bundle;
import android.widget.Button;
import android.widget.Toast;

import androidx.activity.EdgeToEdge;
import androidx.appcompat.app.AppCompatActivity;
import androidx.core.graphics.Insets;
import androidx.core.view.ViewCompat;
import androidx.core.view.WindowInsetsCompat;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        Button btnImplicit = findViewById(R.id.btnImplicit);

        btnImplicit.setOnClickListener(v -> {
            // Create an implicit intent to open Gmail website
            Intent intent = new Intent(Intent.ACTION_VIEW);
            intent.setData(Uri.parse("https://www.gmail.com"));
            startActivity(intent);
        });
    }
}
```

## OUTPUT

<img width="1583" height="884" alt="Screenshot 2025-09-24 091454" src="https://github.com/user-attachments/assets/b0cb4290-53f3-4270-b7cb-80d36c76ed1e" />

<img width="1591" height="936" alt="Screenshot 2025-09-24 091511" src="https://github.com/user-attachments/assets/1fa754f3-2d05-4b29-86cd-0c0d3833e3e7" />

## RESULT
Thus a Simple Android Application create a navigate button using Implicit Intent to display the gmail page using Android Studio is developed and executed successfully.


