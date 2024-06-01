# Max-Frequency-Element
Find the element with max frequency in an array.
//Element having max frequency in array
#include<iostream>
using namespace std;

int main(){
	int n;
	cout<<"Enter the size: ";
	cin>>n;
	int arr[n];
	for(int i=0;i<n;i++){
		cin>>arr[i];
	}
	int c[n];
	for(int i=0;i<n;i++){
		int count=0;
		for(int j=i+1;j<n;j++){
			if(arr[i]!=-100){
			if(arr[i]==arr[j]){
				count++;
				arr[j]=-100;
			}
		}
		}
		if(count!=0){
			c[i]=count;
		}
	}
	int temp[n];
	int k=0;
	for(int i=0;i<n;i++){
		if(arr[i]!=-100){
			temp[k]=arr[i];
			k++;
		}
	}
	int max=c[0];
	for(int i=0;i<n;i++){
		if(c[i]>=c[0]){
			cout<<temp[i]<<" is max freq occuring with freq of "<<c[i];
		}
	}
	
}
