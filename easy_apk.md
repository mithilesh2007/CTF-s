# easy4.apk
- In the main activity
  ```
  public static final boolean onCreate$lambda$0(MainActivity this$0, View view, MotionEvent motionEvent) {
        Intrinsics.checkNotNullParameter(this$0, "this$0");
        Log.i("kitty kitty bang bang", "Listening for taps...");
        if (motionEvent.getAction() != 0) {
            return true;
        }
        Log.i("kitty kitty bang bang", "Screen tapped!");
        this$0.showOverlayImage();
        this$0.playSound(R.raw.bang);
        Log.i("kitty kitty bang bang", "BANG!");
        Log.i("kitty kitty bang bang", "flag{" + this$0.stringFromJNI() + '}');
        return true;
  ```
  - in this code it says that when the screen is tapped there is a msg in the logcat syaing that the screen is tapped and the flag appears
  - the flag is flag{f9028245dd46eedbf9b4f8861d73ae0f}
 
  # easy1.apk
  - In the main activity
    ```
    public void submitPassword(View view) {
        EditText editText = (EditText) findViewById(R.id.editText2);
        if (DigestUtils.md5Hex(editText.getText().toString()).equalsIgnoreCase("b74dec4f39d35b6a2e6c48e637c8aedb")) {
            ((TextView) findViewById(R.id.textView)).setText("Success! CTFlearn{" + editText.getText().toString() + "_is_not_secure!}");
        }
    }
    ```
  - in this block of code there is an encoded md5 string if you decode it you get the password . Then we need to enter the password in the app we get the flag 
  - CTFlearn{Spring2019_is_not_secure!}

  # easy2.apk
  - in the strings.xml file
  ```
  VGhlIGZsYWcgaXM6IGZsYWd7NDZhZmQ0ZjhkMmNhNTk1YzA5ZTRhYTI5N2I4NGFjYzF9Lg==
  ```
  - there is a base64 excrypted text , if you decrypt it we get the flag

  # easy3.apk
  - firstly i hosted the third activity using the command "adb shell am start -n com.example.app2/com.example.app2.ThirdActivity", then there is a msg saying that the flag is right in front of your eyes, so i checked the activity_third.xml , it has half of the flag and the other half is in the strings.xml

  
