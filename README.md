# Android Live Templates #

Live Templates for Android Studio / Intellij IDEA. Originally forked from [Michal Moczulski](https://github.com/mrmike).

## Installation ##

The **Android.xml** file should be placed in the following location:

### **Windows:** ###
```
<your home directory>\.<product name><version number>\config\templates
```

### **Linux:** ###
```
~\.<product name><version number>\config\templates
```


### **MacOS:** ###
```
~/Library/Preferences/<product name><version number>/templates
```

## Templates list ##

### Logging ###

* tag - Adds a log TAG to the class
```
private static final String TAG = $CLASS_NAME$.class.getSimpleName();
```
* ld - Send a DEBUG log message.
```
Log.d(TAG, "$MSG$");
```
* le - Send a ERROR log message.
```
Log.e(TAG, "$MSG$");
```
* li - Send a INFO log message.
```
Log.i(TAG, "$MSG$");
```
* lw - Send a WARN log message.
```
Log.w(TAG, "$MSG$");
```
* lv - Send a VERBOSE log message.
```
Log.v(TAG, "$MSG$");
```
* wtf - What a Terrible Failure: Report an exception that should never happen.
```
Log.wtf(TAG, "$MSG$");
```
* profile - measure execution time
```
final long start = System.currentTimeMillis();
$END$
Log.d("profiling", "[$methodName$]:" + (System.currentTimeMillis() - start));
```

### ButterKnife ###
Tags for the [ButterKnife](http://jakewharton.github.io/butterknife/) view injection library

* inject (**ButterKnife**) - inject view
```
@InjectView(R.id.$VIEW$)
$TYPE$ $NAME$
```
* click (**ButterKnife**) - add OnClickListener
```
@OnClick(R.id.$VIEW$)
void on$NAME$Click() {
    $END$
}
```

### Misc ###
* toast - show toast
```
Toast.makeText($context$, $msg$, Toast.LENGTH_SHORT).show();
```
* inflate - Create layoutInflater and inflate view
```
android.view.LayoutInflater inflater = LayoutInflater.from($context$);
android.view.View view = inflater.inflate(R.layout.$layout$, $parent$, $attach$);
```
* fv - Find View by Id
```
$TYPE$ $VAR$ = ($TYPE$)findViewById(R.id.$ID$);
$END$
```

### XML Layouts ###
* android - Add android namespace (**XML**)
```
xmlns:android="http://schemas.android.com/apk/res/android"
```
* tools - Add tools namespace (**XML**)
```
xmlns:tools="http://schemas.android.com/tools"
```
* ttext - Add tools:text attribute
```
tools:text="$text$"
```