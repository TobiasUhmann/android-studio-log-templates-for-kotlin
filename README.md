# Android Studio Live Templates for Logging in Java

Android Studio provides 'Live Templates' for inserting recurring code snippets like loops and log statements. For example, hitting TAB when entering `logd` will produce

    Log.d(TAG, "divide: foo");
    
One can edit these templates and add new ones in Android Studio under 'Settings > Editor > Live Templates'.

This repo provides some additional logging templates that add the current thread name and an unambigious string ('###') to the respective standard version. There is one template for each built-in one. For example, `logd` is extended to `logdt` which adds the thread name:

    Log.d(TAG, Thread.currentThread().getName() + " ### "
                + "divide: foo");

The resulting log entry looks something like this:

    05-11 21:48:30.338 4988-4988/com.example.test D/MainActivity: main ### divide: foo

It can be filtered easily by searching for '###'. The string is not part of the TAG because the latter is omitted from the log occasionally.

# Usage

* Download `settings.jar` and import it in Android Studio via 'File > Import Settings...'

OR

* Download `AndroidLog.xml` and move it to Android Studio's `templates` directory (on Windows: C:\Users\John\\.AndroidStudio3.1\config\templates)
