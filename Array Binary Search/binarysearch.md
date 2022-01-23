<pre>
1.  Find the first one
int zeroOnes(int n, vector<int > arr){
    for (int i = 0; i < n; i++)
 
        
        if (arr[i] == 1)
            return i;
 
    
    return -1;
}


int main(){
    int n;
    cin>>n;
    vector<int > arr(n);
    for(int i=0;i<n;i++){
        cin>> arr[i];
    }
    int result = zeroOnes(n, arr);
    cout << result << "\n";
}

</pre>
<pre>
2.  Search in Sorted Rotated Array [Pattern Introduction Video]

#include <bits/stdc++.h>
using namespace std;

class SearchInRotatedSortedArray {
  public:
    int search(vector<int>& nums, int target) {
        int l = 0,r = nums.size()-1;
        while(l <= r){
            int mid = l+(r-l)/2;
            if(nums[mid] == target) return mid;
            if(nums[l] <= nums[mid]){
                if(target >= nums[l] && target <= nums[mid]) r = mid-1;
                else l = mid+1;
            }
            else if(nums[mid] <= nums[r]){
                if(target >= nums[mid] && target <= nums[r]) l = mid+1;
                else r = mid-1;
            }
        }
        return -1;
    }
};

int main() {
    FastIO();
    int n;
    cin >> n;
    vector<int> nums;
    ReadMatrix<int>().OneDMatrix(n, nums);

    int queries;
    cin >> queries;
    for (int i = 0; i < queries; i++) {
        int target;
        cin >> target;
        int result = SearchInRotatedSortedArray().search(nums, target);
        cout << result << "\n";
    }

    return 0;
}
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

int kthSmallestElementInMatrix(vector<vector<int>> matrix,int k)
{
      int n=matrix.size();
    vector<int> temp;
    for(auto i=0;i<n;i++)
        for(auto j=0;j<n;j++)
        temp.push_back(matrix[i][j]);
    
    sort(temp.begin(),temp.end());
    int ans=temp[k-1];
    return ans;
}

int main()
{
    int n,k;cin>>n>>k;

    vector<vector<int> > matrix(n);
    for(int i=0;i<n;i++){
        for(int j = 0;j<n;j++){
            int x;cin>>x;
            matrix[i].push_back(x);
        }
    }
    int ans = kthSmallestElementInMatrix(matrix,k);
    cout<<ans<<endl;
}
</pre>
