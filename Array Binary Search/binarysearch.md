<pre>
1.  Find the first one


</pre>
<pre>
2.  Search in Sorted Rotated Array [Pattern Introduction Video]

</pre>
<pre>
3.  Find peak element in the given array

#include <bits/stdc++.h>
using namespace std;

int peakElement(vector<int>&nums){
    int n = nums.size();
        for(int i=0;i<n-1;i++){
            if(nums[i] > nums[i+1] )
                return i;
        }
        return n-1;
}

int main(){
    int N;
    cin>>N;
    vector<int>nums(N);
    for(auto &x:nums)cin>>x;
    cout<<peakElement(nums)<<"\n";
}

</pre>
<pre>
4.  Count occurrences of an integer
#include <bits/stdc++.h>
using namespace std;

int countOccurrences(int n, vector<int> &arr, int k){
     return upper_bound(arr.begin(),arr.end(),k)-lower_bound(arr.begin(),arr.end(),k);
}

int main(){
    int n, k;
    cin >> n >> k;
    vector<int> arr(n);
    for (int i = 0; i < n; i++)
    {
        cin >> arr[i];
    }
    int result = countOccurrences(n, arr, k);
    cout << result;
}
</pre>
<pre>

5.  Find the Nth root

</pre>
<pre>
6.  Find the Kth smallest element in a matrix


</pre>
