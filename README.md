# RANDOM-NUMBER-GENERATOR-APP


## AIM:

Develop an android application to generate random numbers within a given range input from the user.


## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:
Step 1: Create a New Project in Android Studio

Step 2: Working with the activity_main.xml File

Step 3: Working with the MainActivity File



## PROGRAM:
```
/*
Android Application to generate random numbers within a given range input from the user.
Developed by: Sabitha P
Registeration Number : 212222040137
*/
```
### In activity_main.xml
```
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <TextView
        android:id="@+id/textView"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="RANDOM NUMBER GENERATOR"
        android:textSize="24sp"
        android:textStyle="bold|italic"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.177" />

    <TextView
        android:id="@+id/textView2"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginStart="36dp"
        android:text="SET RANGE"
        android:textSize="20sp"
        android:textStyle="bold|italic"
        app:layout_constraintBottom_toTopOf="@+id/button"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/textView"
        app:layout_constraintVertical_bias="0.736" />

    <EditText
        android:id="@+id/input"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginTop="164dp"
        android:ems="10"
        android:hint="input any number"
        android:inputType="text"
        app:layout_constraintBottom_toTopOf="@+id/button"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.55"
        app:layout_constraintStart_toEndOf="@+id/textView2"
        app:layout_constraintTop_toBottomOf="@+id/textView"
        app:layout_constraintVertical_bias="0.273" />

    <TextView
        android:id="@+id/result"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginTop="68dp"
        android:textSize="24sp"
        android:textStyle="bold|italic"
        app:layout_constraintBottom_toTopOf="@+id/button"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.498"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/textView"
        app:layout_constraintVertical_bias="0.108" />

    <Button
        android:id="@+id/button"
        android:layout_width="175dp"
        android:layout_height="56dp"
        android:text="GENERATE"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/textView"
        app:layout_constraintVertical_bias="0.564" />

</androidx.constraintlayout.widget.ConstraintLayout>
```
### In MainActivity.java

```
package com.example.random;

import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;
import android.widget.TextView;
import java.util.Random;
import org.w3c.dom.Text;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        Button btn = (Button) findViewById(R.id.button);
        btn.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                EditText f = (EditText) findViewById(R.id.input);
                TextView res = (TextView) findViewById(R.id.result);
                int range = Integer.parseInt(f.getText().toString());
                Random r = new Random();
                int rand_no = r.nextInt(range - 0)+0;
                res.setText(rand_no + " ");
            }
        });
    }
}
```


## OUTPUT
![image](https://github.com/sabithapaulraj/RANDOM-NUMBER-GENERATOR-APP/assets/118343379/a975391e-00d5-4fbe-bcfe-ef8ff2f43da8)


## Working in Android Studio

![image](https://github.com/sabithapaulraj/RANDOM-NUMBER-GENERATOR-APP/assets/118343379/f04562a9-4b3f-4810-89fd-80fd15a85e16)


## RESULT
Thus a Simple Android Application to generate random numbers within a given range input from the user in Android Studio is developed and executed successfully.


