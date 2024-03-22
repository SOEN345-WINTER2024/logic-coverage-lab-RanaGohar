Name: Rana Gohar

Student ID: 40117475 <br/>

### Method with clauses in the KISS application: <br/>

```
public void run() {
    if ((getParent() != null) && hasWindowFocus()
            && mOriginalWindowAttachCount == getWindowAttachCount()
            && !mHasPerformedLongPress) {
        if (performLongClick()) {
            mHasPerformedLongPress = true;
        }
    }
}
```

#### Get Predicate Coverage:


p =(getParent() != null) && hasWindowFocus() && mOriginalWindowAttachCount == getWindowAttachCount() && !mHasPerformedLongPress <br/>

To make p true:<br/>
Set getParent() to return a non-null value (true).<br/>
Set hasWindowFocus() to return true.<br/>
Set mOriginalWindowAttachCount and getWindowAttachCount() to be equal.<br/>
Set mHasPerformedLongPress to false, which is negated to true (!false = true).<br/>
To make p false:<br/>
Set getParent() to return null (false).<br/>
Set hasWindowFocus() to return false.<br/>
Set mOriginalWindowAttachCount and getWindowAttachCount() to be different (false).<br/>
Set mHasPerformedLongPress to true, which is negated to false (!true = false).<br/>
