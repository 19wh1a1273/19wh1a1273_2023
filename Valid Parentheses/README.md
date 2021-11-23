Input:
-----
3
({[]})
(){}[]
({[}])
output:
-------
True
True
False

code:
-----
#include<bits/stdc++.h>
using namespace std;

string isBalanced(string s)
{
    stack<char> st;
    int i;
    for(i = 0; i<s.length(); i++)
    {
        if(s[i] == '(' || s[i] == '[' || s[i] == '{')
        {
            st.push(s[i]);
        }
        else if(!st.empty())
        {
        if((s[i] == ')' && st.top() != '(') || (s[i] == ']' && st.top() != '[') || (s[i] == '}' && st.top() != '{'))
        {
            return "False";
        }
        else
        {
            st.pop();
        }
        }
        else{
            st.push(s[i]);
        }
    }
    if(st.empty())
    {
        return "True";
    }
    return "False";

}
int main()
{
    int t;
    cin>>t;
    string str;
    while(t--)
    {
        cin>>str;
        cout<<isBalanced(str)<<"\n";
    }
    return 0;
}
