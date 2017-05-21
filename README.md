# Fucking how to get Facebook login in react native right
You are almost doing the right thing if you have reached the login screen. But if you are seeing some ‘invalid hash key’ bull shit when you login for the second time, This is what you going to do.

Go to your jdk folder,
If you know where it is, good, if not, execute this
`/usr/libexec/java_home`

Result might look something like this,
`/Library/Java/JavaVirtualMachines/jdk1.8.0_131.jdk/Contents/Home/bin`

Go to that folder and execute this
`keytool -exportcert -alias androiddebugkey -keystore ~/.android/debug.keystore -keypass android -storepass android | openssl sha1 -binary | openssl base64`

Copy this key to you Facebook App Settings

And DardNivaran Complete.

PS When I did this, It didn’t ask me to input the password, So if you are doing this directly, idk, that might cause some problems.

Got this answer from http://stackoverflow.com/a/12405323/5865743
