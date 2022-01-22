<pre>
Find the equal partition index

import java.util.*;

class EqualPartition {
    public static void main(String args[]) {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();
        long arr[] = new long[n];

        for (int i = 0; i < n; i++)
            arr[i] = sc.nextLong();

        int res = equalPartition(n, arr);

        System.out.println(res);

    }

    static int equalPartition(int n, long arr[]) {
    }
}
</pre>
<pre>
Find the largest sum contiguous subarray

import java.io.*;
import java.util.Scanner;
public class  ContigiousSequence {
	public static  long contigiousSequence(int arr[] , int n) {


	}
	public static void  main (String args []) {

		Scanner sc =  new  Scanner (System.in);

		int n = sc.nextInt();
		int arr [] = new int[n + 5];
		for ( int i = 0 ; i < n; i++)
			arr[i] = sc.nextInt();

		long max = contigiousSequence(arr, n);
		System.out.println(max);

	}
}

</pre>
<pre>
Find if there exists a subarray with sum 0

import java.util.*;

class SubarraySumZero{
	public static String subarraySumZero(Vector<Integer> arr)
 	{
        String result;
        return result;
	}
	public static void main(String[] args) {
		Scanner sc=new Scanner(System.in);
		int t=sc.nextInt();
		for(int j=0;j<t;j++)
		{
			int n=sc.nextInt();
			Vector<Integer> arr=new Vector<Integer>();
			for(int i=0;i<n;i++)
			{
				arr.add(sc.nextInt());
			}
			System.out.println(subarraySumZero(arr));
		}

	}
}
</pre>
<pre>
Find largest subarray with sum 0

import java.util.*;

class LargestSubarraySumZero {
    public static void main(String args[]) {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();
        int arr[] = new int[n];

        for (int i = 0; i < n; i++)
            arr[i] = sc.nextInt();

        ArrayList<Integer> res = largestSubarraySumZero(n, arr);

        for (int j : res)
            System.out.print(j + " ");

    }

    static ArrayList<Integer> largestSubarraySumZero(int n, int arr[]) {
    }
}
</pre>
<pre>
 Find the longest substring with at most K Distinct characters

 import java.util.*;

// Implement your solution here
class LongestSubstringWithAtMostKDistinctCharacter {

    public int lengthOfLongestSubstringKDistinct(String s, int k) {

    }
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int n = scanner.nextInt();
        int k = scanner.nextInt();
	    scanner.nextLine();
        String s = scanner.nextLine();
        scanner.close();

        int result = new LongestSubstringWithAtMostKDistinctCharacter().lengthOfLongestSubstringKDistinct(s,k);
        System.out.println(result);
    }
}

</pre>
<pre>
Find the maximum sum possible out of all subarrays of size k

import java.util.*;

class MaximumSubarraySumSizeK {
    public static void main(String args[]) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int k = sc.nextInt();
        int arr[] = new int[n];
        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }
        System.out.println(maximumSubarraySumSizeK(arr, n, k));
        sc.close();
    }

    static int maximumSubarraySumSizeK(int[] arr, int n, int k) {
    }
}

</pre>
<pre>
Find the longest substring without a repeating character

import java.util.*;

class LongestSubstringWithoutRepeatingCharacter {
    public int lengthOfLongestSubstring(String s) {
        int longestSubstringLength = 0;
        return longestSubstringLength;
    }
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        String s = in.nextLine();
        int result = new LongestSubstringWithoutRepeatingCharacter().lengthOfLongestSubstring(s);
        System.out.println(result);
    }
}


</pre>