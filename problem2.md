# Daily-Question-
#2nd problem from CODECHEF DSA series
# Appy and Contest
#Coding in c++
#include <iostream>
using namespace std;
#define l1 long long int
int probgcd(l1 A,l1 B)
{
    if(B==0)
        return A;
    return probgcd(B,A%B);
}
int problcm(l1 A,l1 B)
{
    return (A*B)/probgcd(A,B);
}
int main() {
	// your code goes here
	int t;
	cin>>t;
	while(t--)
	{
	    l1 N,K;
	    l1 A,B;
	    cin>>N>>A>>B>>K;
	    l1 count=0;
	    int gcd=probgcd(A,B);
	   // cout<<gcd;
	    int lcm=problcm(A,B);
	    //cout<<lcm;
	    count=(N/A)+(N/B)-2*(N/lcm);
	    if(count>=K)
	        cout<<"Win"<<"\n";
	    else
	        cout<<"Lose"<<"\n";
	}
	
	
	
	return 0;
}


