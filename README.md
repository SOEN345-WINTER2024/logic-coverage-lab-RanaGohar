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


#### Get Clause Coverage:

Test case 1: Evaluate the first clause to true, and the rest to true.<br/>
&emsp;&bull;Set getParent() to return a non-null value (true).<br/>
&emsp;&bull;Set hasWindowFocus() to return true.<br/>
&emsp;&bull;Set mOriginalWindowAttachCount and getWindowAttachCount() to be equal.<br/>
&emsp;&bull;Set mHasPerformedLongPress to false.<br/>
Test case 2: Evaluate the first clause to false, and the rest to true.<br/>
&emsp;&bull;Set getParent() to return null (false).<br/>
&emsp;&bull;Set hasWindowFocus() to return true.<br/>
&emsp;&bull;Set mOriginalWindowAttachCount and getWindowAttachCount() to be equal.<br/>
&emsp;&bull;Set mHasPerformedLongPress to false.<br/>
Test case 3: Evaluate the first clause to true, and the rest to false.<br/>
&emsp;&bull;Set getParent() to return a non-null value (true).<br/>
&emsp;&bull;Set hasWindowFocus() to return false.<br/>
&emsp;&bull;Set mOriginalWindowAttachCount and getWindowAttachCount() to be different.<br/>
&emsp;&bull;Set mHasPerformedLongPress to true.<br/>
Test case 4: Evaluate the first clause to false, and the rest to false.<br/>
&emsp;&bull;Set getParent() to return null (false).<br/>
&emsp;&bull;Set hasWindowFocus() to return false.<br/>
&emsp;&bull;Set mOriginalWindowAttachCount and getWindowAttachCount() to be different.<br/>
&emsp;&bull;Set mHasPerformedLongPress to true.<br/>


#### Get CACC

Test Case 1: <br/>
&emsp;&bull;Set major clause (getParent() != null) to true and the rest of the conditions to true, causing p to be true.<br/>
Test Case 2: <br/>
&emsp;&bull;Set major clause to false and the rest of the conditions to true, causing p to be false.<br/>
Test Case 3: <br/>
&emsp;&bull;Set major clause to true and the rest of the conditions to false, causing p to be false.<br/>
Test Case 4: <br/>
&emsp;&bull;Set major clause to false and the rest of the conditions to false, causing p to be false.<br/>


#### Get RACC

Test Case 1: <br/>
&emsp;&bull;Set major clause (getParent() != null) to true and the rest of the conditions to true, choosing specific values for the minor clauses.<br/>
Test Case 2: <br/>
&emsp;&bull;Set major clause to false and the rest of the conditions to true, ensuring the same values are chosen for the minor clauses as in Test Case 1.<br/>
Test Case 3: <br/>
&emsp;&bull;Set major clause to true and the rest of the conditions to false, choosing the same values for the minor clauses as in Test Case 1.<br/>
Test Case 4: <br/>
&emsp;&bull;Set major clause to false and the rest of the conditions to false, ensuring the same values are chosen for the minor clauses as in Test Case 1.<br/>





