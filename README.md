# Xetabot-Task
A problem soving question &amp; form-componet with validation and popup 


##  Assignment Answer:-
> ### Task-1 : Write a program to get the maximum product of a sub array.
For example,
Input: { -6, 4, - 5, 8, -10, 0, 8 }
Output: 1600
Explanation: The maximum product subarray is {4, -5, 8, -10} having product 1600
Input： ｛40,9，-20，-10｝
Output: 200
Explanation: The maximum product subarray is {-20, -10} having product
200
```cpp
// Online C++ compiler to run C++ program online
#include <iostream>
#include<bits/stdc++.h>
using namespace std;
int main() {
    int n;
    cout<<"Enter the size of the array: ";
    cin>>n;
    int arr[n];
    cout<<"Enter the element of the array: ";
    for(int i=0;i<n;i++){
        cin>>arr[i];
    }
    int pref=1, suff=1;
    int ans=INT_MIN;
    for(int i=0;i<n;i++){
        if(pref==0){
            pref=1;
        }
        if(suff==0){
            suff=1;
        }
        pref=pref*arr[i];
        suff=suff*arr[n-1-i];
        ans=max(ans,max(pref,suff));
    }
    cout<<"Maximum subarray product is: "<<ans<<endl;
    return 0;
}
```
### > Task-2 : Create A Form Component For Student Details Using React & Bootstrap.

**Requirements :
Students Details: Roll No, Name, Age, Email, Mob Number.**

**Also Add Validation For The Student Fields. After Submitting Form, Show Student Details In A Popup.
**

[Form Componnet code link](https://codesandbox.io/p/sandbox/lucid-sun-zndckf?file=%2Fsrc%2FForm.js%3A104%2C1 "Form Componnet code link")

