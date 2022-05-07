# The-Attack-of-Queen_CODECHEF
/*Chef has started developing interest in playing chess, and was learning how the Queen moves.

Chef has an empty N×N chessboard. He places a Queen at (X,Y) and wonders - What are the number of cells that are under attack by the Queen?

Notes:

The top-left cell is (1,1), the top-right cell is (1,N), the bottom-left cell is (N,1) and the bottom-right cell is (N,N).
The Queen can be moved any number of unoccupied cells in a straight line vertically, horizontally, or diagonally.
The cell on which the Queen is present, is not said to be under attack by the Queen.
Input Format
The first line contains a single integer T - the number of test cases. Then the test cases follow.
The first and only line of each test case contains three integers N, X and Y, as described in the problem statement.

Output Format
For each test case, output in a single line, the total number of cells that are under attack by the Queen.

Constraints
1≤T≤104
1≤N≤106
1≤X,Y≤N
Sample Input 1 
5
1 1 1
3 2 2
3 2 1
2 2 2
150 62 41
Sample Output 1 
0
8
6
3
527
*/
/* package codechef; // don't place package name! */

import java.util.*;
import java.lang.*;
import java.io.*;

/* Name of the class has to be "Main" only if the class is public. */
class Codechef
{   
    public static void main(String as[])
    {
	    Scanner ob=new Scanner(System.in);
        int m=ob.nextInt();
        for(int i=0;i<m;i++)
        {
            int n=ob.nextInt();
            int x=ob.nextInt();
            int y=ob.nextInt();
            int c=0;
            int a=(x-1)+(n-x)+(y-1)+(n-y);
            if(x-1 > y-1)
                c+=y-1;
            else
                c+=x-1;
            
            if(x-1>n-y)
                c+=n-y;
            else    
                c+=x-1;
            
            if(n-x>y-1)
                c+= y-1;
            else
                c+=n-x;
            
            if(n-x>n-y)
                c+=n-y;
            else
                c+=n-x;
            
            System.out.println(a+c);
                
            
        }
    }
}            

