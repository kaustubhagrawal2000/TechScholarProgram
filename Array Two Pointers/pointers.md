<pre>
Find Pair with Given Sum in Sorted Array
import java.util.*;

class TwoSumInSortedArray {
    public static void main(String args[]) {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();
        int arr[] = new int[n];

        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }
        int k = sc.nextInt();

        boolean res = twoSumInSortedArray(n, arr, k);

        String ans = (res) ? "Present" : "Not Present";

        System.out.println(ans);

    }

    static boolean twoSumInSortedArray(int n, int arr[], int k) {
        int i=0,j=n-1;
        while(i < j){
            if(arr[i] + arr[j] == k) return true;
            else if(arr[i] + arr[j] < k) i++;
            else j--;
        }
        return false;
    }
}
</pre>
<pre>
Merge Two Sorted Arrays

import java.io.*;
import java.util.*;

public class MergeSortedArray {
    // Implement your solution by completing the below function
    public static int [] mergeSortedArray(int[] nums1, int m, int[] nums2, int n) {
        int[] res = new int[m+n];
        int i=0,j=0,k=0;
        while(i<m && j<n){
            if(nums1[i] <= nums2[j]){
                res[k++] = nums1[i];
                i++;
            }
            else{
                res[k++] = nums2[j];
                j++;
            }
        }
        while(i<m){
            res[k++] = nums1[i];
            i++;
        }
        while(j<n){
            res[k++] = nums2[j];
            j++;
        }
        return res;
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int m = scanner.nextInt();
        int n = scanner.nextInt();
        int[] nums1 = new int[m];
        int[] nums2 = new int[n];

        for (int i = 0; i < m; i++)
            nums1[i] = scanner.nextInt();
        for (int i = 0; i < n; i++)
            nums2[i] = scanner.nextInt();

        scanner.close();

        int[] nums = mergeSortedArray(nums1, m, nums2, n);
        for (int i = 0; i < nums.length; i++)
            System.out.print(nums[i] + " ");
    }
}

</pre>
<pre>
 Find Triplet with Maximum Sum in Unsorted Array [Pattern Introduction]

import java.util.*;

class MaxSumTriplet {
    public static void main(String args[]) {
        Scanner sc = new Scanner(System.in);
        int t = sc.nextInt();
        while (t-- > 0) {

            int n = sc.nextInt();
            long arr[] = new long[n];

            for (int i = 0; i < n; i++)
                arr[i] = sc.nextLong();

            long result = maxSumTriplet(n, arr);

            System.out.println(result);

        }

    }

    static long maxSumTriplet(int n, long arr[]) {
        long sum = 0;
        for(int i=1;i<n-1;i++){
            long a = 0;
            for(int j=0;j<i;j++){
                if(arr[j] < arr[i]) a = Math.max(a,arr[j]);
            }
            if(a == 0) continue;
            long c = 0;
            for(int j=i+1;j<n;j++){
                if(arr[j] > arr[i]) c = Math.max(c,arr[j]);
            }
            if(c == 0) continue;
            sum = Math.max(sum,a+arr[i]+c);
        }
        return sum;
    }
}
</pre>
<pre>
Remove duplicates such that each element occurs at most twice

import java.util.*;

class RemoveDuplicatesFromSortedArrayII {
    public static void main(String args[]) {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();
        int arr[] = new int[n];

        for (int i = 0; i < n; i++)
            arr[i] = sc.nextInt();

        int res = removeDuplicatesFromSortedArrayII(n, arr);

        System.out.println(res);

        for (int i = 0; i < res; i++)
            System.out.print(arr[i] + " ");

    }

    static int removeDuplicatesFromSortedArrayII(int n, int[] arr) {
    
    int j = 0;

    for (int i = 0; i < n; i++) {
      
      if(i < n - 2 && nums[i] == nums[i + 2]) {
        continue;
      }

      nums[j++] = nums[i];
    }

    return j;
    }

}

</pre>
<pre>
 Find pair with given sum in unsorted array

 import java.io.*;
import java.util.*;

public class TwoSum {

    public int[] twoSum(int[] nums, int target) {
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        int[] numbers = new int[scanner.nextInt()];
        for (int i = 0; i < numbers.length; i++)
            numbers[i] = scanner.nextInt();
        int target = scanner.nextInt();
        scanner.close();

        int[] complements = new TwoSum().twoSum(numbers, target);
        System.out.print(complements[0] + " " + complements[1]);
    }
}

</pre>
<pre>
Find the container that holds the most water

import java.io.*;
import java.util.*;

class ContainerWithMostWater {

    // Complete the function implementation below
    public int maxArea(int[] height) {
        int answer = 0;
        return answer;
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int n = scanner.nextInt();
        int height[] = new int[n];
        for(int i = 0 ; i < n ; i++) {
            height[i] = scanner.nextInt();
        }
        scanner.close();
        int result = new ContainerWithMostWater().maxArea(height);
        System.out.println(result);
    }
}

</pre>
<pre>
Merge overlapping intervals


import java.util.*;

class MergeIntervals {

    public int[][] mergeIntervals(int[][] intervals) {

    }

    public static void main(String[] args)
    {
        Scanner scanner = new Scanner(System.in);

        int n = scanner.nextInt();

        int[][] nums = new int[n][2];

        for(int i = 0 ; i < n ;i++) {
            nums[i][0] = scanner.nextInt();
            nums[i][1] = scanner.nextInt();
        }

        int[][] results = new MergeIntervals().mergeIntervals(nums);

        for (int i = 0; i < results.length; ++i) {
            System.out.printf("%d %d\n", results[i][0], results[i][1]);
        }
    }
}


</pre>
<pre>

Find Minimum Number of Meeting Rooms Required

import java.util.*;

public class MeetingRooms {

    public int findNumRooms(int[][] intervals) {
    }

    public static void main(String[] args)
    {
        Scanner scanner = new Scanner(System.in);

        int n = scanner.nextInt();

        int[][] nums = new int[n][2];

        for(int i = 0 ; i < n ;i++) {
            nums[i][0] = scanner.nextInt();
            nums[i][1] = scanner.nextInt();
        }

        int result = new MeetingRooms().findNumRooms(nums);

        System.out.printf("%d", result);
    }

}


</pre>