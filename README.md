# Ex.No:2a Implicit Intents

## AIM:

To create a layout,click button,open google page using Implicit Intents in Android Studio.

## EQUIPMENTS REQUIRED:

Android Studio(Min. required Artic Fox)

## ALGORITHM:

Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as “ex.no.2″ and click Next. 

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: open google page using Implicit Intents and display factorial number using Explicit Intents in MainActivity file.

Step 7: Save and run the application.

## PROGRAM:

```
/*
Program to implement “Implicit Intents”.
Developed by: U.BHAVYA
Registeration Number : 212220230055
*/
```
#### MainActivity.java
```
package com.example.exp2aimplicit;

        import androidx.appcompat.app.AppCompatActivity;

        import android.content.Intent;
        import android.net.Uri;
        import android.os.Bundle;
        import android.widget.Button;
        import android.widget.EditText;

public class MainActivity extends AppCompatActivity {

    Button button;
    EditText editText;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        button = findViewById(R.id.button);
        editText =  findViewById(R.id.editText);

        button.setOnClickListener(view -> {
            String url=editText.getText().toString();
            Intent intent=new Intent(Intent.ACTION_VIEW, Uri.parse(url));
            startActivity(intent);
        });
    }
}
```
#### activity_main.xml
```
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">


    <EditText
        android:id="@+id/editText"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginStart="8dp"
        android:layout_marginEnd="8dp"
        android:ems="10"
        android:importantForAutofill="no"
        android:inputType="text"
        android:minHeight="48dp"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.589"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.476"
        tools:ignore="LabelFor,TextFields,SpeakableTextPresentCheck" />

    <Button
        android:id="@+id/button"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginStart="156dp"
        android:layout_marginTop="172dp"
        android:text="/visit"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.089"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.518" />

</androidx.constraintlayout.widget.ConstraintLayout>
```

## OUTPUT:

![1p](https://user-images.githubusercontent.com/75235293/165377357-25b4c3aa-510a-444e-a762-6f95d16ef895.jpg)

![2p](https://user-images.githubusercontent.com/75235293/165377397-7fce32e9-6371-46eb-9ef8-e04bb2663e5e.jpg)

## RESULT:

Thus a Simple Android Application to open google page using Implicit Intents using Android Studio is developed and executed successfully.
