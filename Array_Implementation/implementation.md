 <pre>
 Print Matrix in Spiral Order

 import java.util.*;

class SpiralMatrixII {
    public static void main(String args[]) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int result[][] = spiralMatrixII(n);

        for (int i = 0; i < n; i++) {
            for (int j = 0; j < n; j++) {
                System.out.print(result[i][j] + " ");
            }
            System.out.println();
        }
    }

    static int[][] spiralMatrixII(int n) {
            int[][] res = new int[n][n];
        int number = 1;
        int left = 0,right = n-1,top = 0,bottom = n-1;
        while(left <= right && top <= bottom){
            for(int idx=left;idx<=right;idx++){
                res[top][idx] = number++;
            }
            for(int idx=top+1;idx<=bottom;idx++){
                res[idx][right] = number++;
            }
            for(int idx=right-1;idx>=left;idx--){
                res[bottom][idx] = number++;
            }
            for(int idx=bottom-1;idx>top;idx--){
                res[idx][left] = number++;
            }
            left++;
            right--;
            top++;
            bottom--;
        }
        return res;
    
    }
}
</pre>
<pre>
Increment number represented as array

import java.util.*;


class IncrementNumber{
    public static void main(String args[]){
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();
        int arr[] = new int[n];

        for(int i=0;i<n;i++) {
            arr[i] = Integer.parseInt(sc.next());
        }

        int incArr[] = incrementNumber(n, arr);

        for(int i=0;i<incArr.length;i++) {
            System.out.print(incArr[i]);
        }
        
    }

    static int[] incrementNumber(int n, int arr[]){
          int countNine = 0;
        for(int i=0;i<n;i++){
            if(arr[i] == 9) countNine++;
        }
        int res_size = n;
        if(countNine == n) res_size++;
        int[] res = new int[res_size];
        int index = res_size-1,carry = 0;
        for(int i=n-1;i>=0;i--){
            int sum;
            if(i == n-1) sum = carry+arr[i]+1;
            else sum = carry+arr[i];
            res[index--] = sum%10;
            carry = sum/10;
        }
        if(carry > 0) res[index--] = carry;
        return res;
    }
}

</pre>

<pre>
 Find the maximum profit by buying and selling stocks optimally

 import java.io.*;
import java.util.*;

public class BestTimeToBuyAndSellStocks {
    // Implement your solution Here
    public int maxProfit(int[] prices) {
         int profit = 0;
        for(int i=1;i<prices.length;i++){
            if(prices[i] > prices[i-1]) 
                profit += prices[i]-prices[i-1];
        }
        return profit;
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int[] prices = new int[scanner.nextInt()];
        for (int i = 0; i < prices.length; i++)
            prices[i] = scanner.nextInt();
        scanner.close();

        int result = new BestTimeToBuyAndSellStocks().maxProfit(prices);
        System.out.print(Integer.toString(result));
    }
}
</pre>

<pre>
Rotate Image by 90 degrees

import java.io.*;
import java.util.*;

public class RotateImage {
    public void rotateImage(int[][] matrix) {
         int n = matrix.length;
        for(int i=0;i<n;i++){
            for(int j=i+1;j<n;j++){
                int temp = matrix[i][j];
                matrix[i][j] = matrix[j][i];
                matrix[j][i] = temp;
            }
        }
        for(int i=0;i<n;i++){
            for(int j=0;j<n/2;j++){
                int temp = matrix[i][j];
                matrix[i][j] = matrix[i][n-j-1];
                matrix[i][n-j-1] = temp;
            }
        }
    }

    public static void main(String[] args) throws IOException {
        Scanner scanner = new Scanner(System.in);
        int matrixSize = scanner.nextInt();
        int[][] matrix = new int[matrixSize][matrixSize];
        for (int i = 0; i < matrixSize; ++i) {
            for (int j = 0; j < matrixSize; ++j) {
                matrix[i][j] = scanner.nextInt();
            }
        }
        scanner.close();

        new RotateImage().rotateImage(matrix);
        for (int i = 0; i < matrixSize; ++i) {
            for (int j = 0; j < matrixSize; ++j) {
                System.out.print(matrix[i][j] + " ");
            }
            System.out.println();
        }
    }
}
</pre>

<pre>
Find first missing positive number in array

import java.util.*;

public class FirstMissingPositive {
    private void swap(int[] arr,int p1,int p2){
        int temp = arr[p1];
        arr[p1] = arr[p2];
        arr[p2] = temp;
    }
   public int firstMissingPositive(int[] nums) {
        
        int N = nums.length;
        for(int i=0;i<N;i++){
            int idx = nums[i]-1;
            while(idx >= 0 && idx < N && idx != i){
                swap(nums,i,idx);
                idx = nums[i] - 1;
            }
        }
        for(int i=0;i<N;i++){
            if(i+1 != nums[i]) return i+1;
        }
        return N+1;
    }

    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        int n = in.nextInt();
        int[] nums = new int[n];
        for(int i = 0 ; i < n ; ++i) {
            nums[i] = in.nextInt();
        }
        int result = new FirstMissingPositive().firstMissingPositive(nums);
        System.out.println(result);
    }
}

</pre>


<pre>
Find if the string permutation can form a palindrome

import java.io.*;
import java.util.*;
import java.lang.Math;
public class  PermutationPalindrome {

  public static int isPermutationPalindrome(String s ) {
     HashSet<Character> hs = new HashSet<>();
    for(int i=0;i<s.length();i++){
      if(hs.contains(s.charAt(i))) hs.remove(s.charAt(i));
      else hs.add(s.charAt(i));
    }
    if(hs.size() == 0 || hs.size() == 1) return 1;
    return 0;
  }
  public static void  main (String args []) {

    Scanner sc =  new  Scanner (System.in);
    int t = 1;
    t = sc.nextInt();
    sc.nextLine();
    while (t > 0) {
      t--;
      String s = new String();
      s = sc.next();

      int flag = isPermutationPalindrome(s);
      if (flag == 1) {
        System.out.println("True");
      } else {
        System.out.println("False");
      }
    }
  }

}
</pre>

<pre>
Reverse Order of Words in a String

import java.util.*;


class ReverseWordsInAString{
    public static void main(String args[]){
        Scanner sc = new Scanner(System.in);
        String s = sc.nextLine();
        System.out.println(reverseWordsInAString(s));
        sc.close();
    }

    static String reverseWordsInAString(String s){
        Stack<String> st = new Stack<>();
       String word = "";
       for(int i=0;i<s.length();i++){
           if(s.charAt(i) == ' '){
               if(!word.equals("")){
                   st.push(word);
                   word = "";
               }
           }
           else word = word + s.charAt(i);
       }
       if(!word.equals("")) st.push(word);
       String res = st.pop();
       while(!st.empty()){
           res = res + ' ' + st.pop();
       }
       return res;
    }
}

</pre>

<pre>
 Find if one string is an anagram of the other

 import java.io.*;
import java.util.*;

public class ValidAnagram {
    public boolean validAnagram(String s, String t) {
        if(s.length() != t.length()) return false;
        int[] count1 = new int[26];
        int[] count2 = new int[26];
        for(int i=0;i<s.length();i++){
            count1[s.charAt(i)-'a']++;
            count2[t.charAt(i)-'a']++;
        }
        for(int i=0;i<26;i++){
            if(count1[i] != count2[i]) return false;
        }
        return true;
    }

    public static void main(String[] args) throws IOException {
        BufferedReader in = new BufferedReader(new InputStreamReader(System.in));
        String s = in.readLine();
        String t = in.readLine();

        boolean result = new ValidAnagram().validAnagram(s, t);
        System.out.print(String.valueOf(result));
    }
}
</pre>


<pre>
Set Matrix Rows and Columns to Zero

import java.io.*;
import java.util.*;

class SetMatrixZeroes {
    public void setMatrixZeroes(int[][] matrix) {
         if(matrix.length == 0) return;
        int row0 = 1,col0 = 1;
        for(int i=0;i<matrix[0].length;i++){
            if(matrix[0][i] == 0) row0 = 0;
        }
        for(int i=0;i<matrix.length;i++){
            if(matrix[i][0] == 0) col0 = 0;
        }
        for(int i=1;i<matrix.length;i++){
            for(int j=0;j<matrix[0].length;j++){
                if(matrix[i][j] == 0){
                    matrix[i][0] = 0;
                    break;
                }
            }
        }
        for(int j=1;j<matrix[0].length;j++){
            for(int i=0;i<matrix.length;i++){
                if(matrix[i][j] == 0){
                    matrix[0][j] = 0;
                    break;
                }
            }
        }
        for(int i=1;i<matrix.length;i++){
            if(matrix[i][0] == 0){
                for(int j=0;j<matrix[0].length;j++){
                    matrix[i][j] = 0;
                }
            }
        }
        for(int i=1;i<matrix[0].length;i++){
            if(matrix[0][i] == 0){
                for(int j=0;j<matrix.length;j++){
                    matrix[j][i] = 0;
                }
            }
        }
        if(row0 == 0){
            for(int i=0;i<matrix[0].length;i++){
                matrix[0][i] = 0;
            }
        }
        if(col0 == 0){
            for(int i=0;i<matrix.length;i++){
                matrix[i][0] = 0;
            }
        }
    }
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);

        int m = in.nextInt();
        int n = in.nextInt();

        int[][] matrix = new int[m][n];

        for(int i = 0 ; i < m ; ++i) {
            for(int j = 0 ; j < n ; ++j) {
                matrix[i][j] = in.nextInt();
            }
        }

        in.close();
        new SetMatrixZeroes().setMatrixZeroes(matrix);

        for(int i = 0 ; i < m ; ++i) {
            for(int j = 0 ; j < n ; ++j) {
                System.out.print(matrix[i][j]);
                System.out.print(' ');
            }
            System.out.println();
        }
    }
}
</pre>