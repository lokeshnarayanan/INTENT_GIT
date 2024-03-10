# Ex-No_2-Intent(Implicit & Explicit)

Develop program to perform explicit and implicit intent by creating a buttons using Android Studio

## AIM:
To develop a program to perform explicit and implicit intent by creating a buttons using Android Studio

## EQUIPMENTS REQUIRED:

Android Studio(Min. required Artic Fox)


## ALGORITHM:
Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as Intent and click Next.

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Create a Layout and two buttons named as explicit intent and implicit Intent 

Step 7: By clicking Implict Intent button open google page using Implicit Intents in MainActivity file.

Step 8: By clicking Explicit Intent button open second page using Explicit Intents in MainActivity file.

Step 7: Save and run the application.


# Program:

Program to create a layout by click button option ,open google page using Implicit Intents in Android Studio. .
### Developed by: LOKESH N
### RegisterNumber: 212222100023
## Activity_main.xml:
```python
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">
<Button
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:id="@+id/btn1ex"
    android:layout_gravity="center"
    android:layout_centerHorizontal="true"
    android:layout_alignParentTop="true"
    android:layout_marginTop="250dp"
    android:text="Explicit button"/>
    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_centerVertical="true"
        android:layout_centerHorizontal="true"
        android:id="@+id/btn2im"
        android:text="implicit button"/>




</RelativeLayout>

```

## Activity_second.xml:
```python
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity2">
    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Hello!"
        android:fontFamily="sans-serif-medium"
        android:layout_centerInParent="true"
        android:textSize="30dp"
        tools:ignore="MissingConstraints" />

</RelativeLayout>
```
## MainActivity.java:
```python
package com.example.second_exp;

import androidx.appcompat.app.AppCompatActivity;

import android.content.Intent;
import android.net.Uri;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;

public class MainActivity extends AppCompatActivity {
    Button explicit_btn,implicit_btn;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        explicit_btn=(Button)findViewById(R.id.btn1ex);
        implicit_btn=(Button)findViewById(R.id.btn2im);
        explicit_btn.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                Intent intent=new Intent(getBaseContext(),MainActivity2.class);
                startActivity(intent);
            }

        });
        implicit_btn.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                Intent intent2=new Intent(Intent.ACTION_VIEW);
                intent2.setData(Uri.parse("https://www.google.com"));
                startActivity(intent2);
            }
        });


    }

}
```
## Activity_second.java:
```python
package com.example.second_exp;

import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;

public class MainActivity2 extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main2);
    }
}
```



## OUTPUT:
![image](https://github.com/lokeshnarayanan/INTENT_GIT/assets/119393019/ebe78e47-34d2-49ba-ab76-cca59e7910f7)


## EXPLICIT:

![image](https://github.com/lokeshnarayanan/INTENT_GIT/assets/119393019/dbb3c687-5415-4b8f-9c58-6143be0b17fc)

## IMPLICIT:
![google](https://github.com/lokeshnarayanan/INTENT_GIT/assets/119393019/ca471703-f34f-427f-8a89-7a492a4525fc)



## RESULT:
Thus a Simple Android Application to open google page using Implicit Intents in Android Studio was developed and executed successfully.
