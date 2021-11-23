Input: 4
[2,7,11,15]
target=9
output: [2,7]

Code:
------

#include<bits/stdc++.h>
using namespace std;

int main(){

    int n,target;
    cin>>n;
    int arr[n];
    for(int i=0;i<n;i++){
        cin>>arr[i];
    }
    cin>>target;
    for(int i=0;i<n;i++){
        for(int j=i+1;j<n;j++){
            if(arr[i]+arr[j]==target)
                cout<<"["<<i<<","<<j<<"]"<<endl;
        }
    }
    return 0;
    
}
