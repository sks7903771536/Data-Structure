#  Permutation with spaces
// Permutation with spaces
#include <bits/stdc++.h>
using namespace std;

void solve(string ip,string op,int i)
{
    if(i==ip.size())
    {
        cout<<"("<<op<<")";return ;
    }
    
    if(i<ip.size()-1)
    {
        op=op+ip[i]+" ";
        solve(ip,op,i+1);
        op.erase(op.size()-2,op.size());
    }
    op=op+ip[i];
    solve(ip,op,i+1);
    return ;
}
int main() {
	//code
	int t;
	cin>>t;
	while(t--)
	{
	    
	    string ip;
	    cin>>ip;
	    
	    string op;
	    int i=0;
	    solve(ip,op,i);
	    cout<<endl;
	}
	return 0;
}
