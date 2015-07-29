# JavaTest

**code**
public class arrays {
	
	/**
	 * @param args
	 */
	public static void main(String[] args) {
		// TODO Auto-generated method stub
         int[]  a = {1,2,3,4,5};
         int[] l = {1001,1002,1003,1004,1005};
         System.arraycopy(a, 2, l, 2, 3);
         for(int i=0; i<l.length; i++)
        	 System.out.println(i + ": "+ l[i]);
         }
}

**result**
0: 1001
1: 1002
2: 3
3: 4
4: 5

