# AndSes6Ass2

MainActivity.java
package me.rk.andses6ass2;

import android.support.v7.app.ActionBar;
import android.support.v7.app.AppCompatActivity;
import android.os.Bundle;
import android.view.Menu;
import android.view.MenuInflater;
import android.view.MenuItem;
import android.widget.Toast;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        getSupportActionBar();
    }

    @Override
    public boolean onCreateOptionsMenu(Menu menu) {
        getMenuInflater().inflate(R.menu.main_menu, menu);
        return true;
    }

    @Override
    public boolean onOptionsItemSelected(MenuItem item) {
        int id=item.getItemId();
        switch (id){
            case R.id.about_id:
                Toast.makeText(MainActivity.this, "About menu selected", Toast.LENGTH_SHORT).show();
            case R.id.info_id:
                Toast.makeText(MainActivity.this, "Info menu selected", Toast.LENGTH_SHORT).show();
        }
        return super.onOptionsItemSelected(item);
    }
}

main_menu.xml
<?xml version="1.0" encoding="utf-8"?>
<menu xmlns:android="http://schemas.android.com/apk/res/android">

    <item
        android:id="@+id/info_id"
        android:title="Info"
        android:icon="@drawable/ic_info_outline_black_24dp"
        android:showAsAction="always"/>
    <item
        android:id="@+id/about_id"
        android:title="About"
        android:icon="@drawable/query"
        android:showAsAction="always"/>
</menu>



