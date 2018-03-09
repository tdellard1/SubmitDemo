This is library project with a custom view that implements concept of Submit Button (<https://dribbble.com/shots/1426764-Submit-Button?list=likes&offset=3>) made by Colin Garven.  

###Demo###

![](gifs/submitview.gif)

###Usage###

``` xml
 <com.tuesda.submit.SubmitView
        android:layout_centerInParent="true"
        android:id="@+id/submit"
        android:layout_width="200dp"
        android:layout_height="200dp" />
```

``` xml
mSubmit.setOnProgressStart(new SubmitView.OnProgressStart() {
            @Override
            public void progressStart() {
                // do something when progress start
            }
        });
        
        mSubmit.setOnProgressDone(new SubmitView.OnProgressDone() {
            @Override
            public void progressDone() {
                // do something when progress is done
            }
        });
```

###public interface###

| Function Name |  Effect|
|:------|:-----|
|`setBackColor(int color)`| Set the background color of the icon, the default is green(0xff00cd97)，上图Demo设置为蓝色(0xff0097cd)|
|`setText(String str)`|Settings button name, default`Submit`|
|`reset()`|Button will reset to the initial state|
|`setProgress(float progress)`|Setting the implementation process is executing work|
|`isProgressDone()`| Work is being performed is completed|
|`setOnProgressStart(OnProgressStart listener)`|Set upprogressHe began to call back|
|`setOnProgressDone(OnProgressDone listener)` | Set up progressCompletion callback|
