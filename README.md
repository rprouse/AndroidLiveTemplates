AndroidLiveTemplates
====================

Live Templates set for Android Studio / Intellij IDEA. 

## Installation

Android.xml file should be placed in the following location:

###**Windows:** 
```
<your home directory>\.<product name><version number>\config\templates
```

###**Linux:**
```
~\.<product name><version number>\config\templates
```


###**MacOS:** 
```
~/Library/Preferences/<product name><version number>/templates
```


## Usage

During code editing type one of the template name and press tab.

### Templates list

1. ld - log debug message
```
Log.d("$TAG$", "$MSG$");
```
2. toast - show toast
```
Toast.makeText($context$, $msg$, Toast.LENGTH_SHORT).show();
```
3. profile - measure exceution time
```
final long start = System.currentTimeMillis();
$END$
Log.d("profiling", "[$methodName$]:" + (System.currentTimeMillis() - start));
```
4. view (**ButterKnife**) - inject view
```
@InjectView(R.id.$VIEW$)
$TYPE$ $NAME$
```
5. click (**ButterKnife**) - add OnClickListener
```
@OnClick(R.id.$VIEW$)
void on$NAME$Click() {
    $END$
}
```