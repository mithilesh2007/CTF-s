# hard1.apk
firstly i downloaded the apk . to sign up we need a leet name 
examples of leet names:
Player → P14y3r
Legend → L3g3nd
Shadow → $h4d0w
Master → M@st3r

Then in the main activity we can see that the username is retrived from the shared preferences and was being added to usename 2 .
in this line of code ```         String flag = aesEncryption.decrypt("mhVTa4HLNQRuxNNF/+/JJYUNyPvE4JsPe7h9ERBsSgjGxjq6nVtggZMMNXYrjCN0", new SecretKeySpec(bArr, "AES"), iv); ``` for AES encrytion we need a string and a Secretkey . Here bArr should consits of 16 bytes but there is only 12 == 111111111111 so we know that username should contain 4 bytes

in the else if block ``` else if (username2 != null && StringsKt.contains$default((CharSequence) username2, (CharSequence) "1337", false, 2, (Object) null) && !Intrinsics.areEqual(username2, "1337"))``` we can see that username2 should comtain "1337"
so i sign up using 1337 as username and some password and got the flag
