# lin_search-by-recursion
Linear search by recursions


#include<bits/stdc++.h>
using namespace std;

bool solve(int *arr,int a,int size)
{
    if(size==0)
    {
        return 0;
    }
    if(*arr==a)
    {
        return true;
    }
    solve(arr+1,a,size-1);
}

int main()
{
    int arr[]={13,15,19,22,32,35,44,53};
    int a;
    cout<<"enter a elements you wnats to search :";
    cin>>a;
    int size=sizeof(arr)/4;
    if(solve(arr,a,size))
        cout<<"element found"<<endl;
    else
        cout<<"element not found"<<endl;
        
}
