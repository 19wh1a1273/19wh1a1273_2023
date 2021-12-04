INPUT:                              
-----
5
OUTPUT:
-----
*
* *
* * *
* * * *
* * * * *

Program:
------
#include<bits/stdc++.h>

using namespace std;

int main(){

    int n,i,j;
    
    cin>>n; //no.of rows
    
    for(i=0;i<n;i++){
    
        for(j=0;j<(i+1);j++)
        
            cout<<"* ";
            
        cout<<endl;
    }
    
    return 0;
    
}
