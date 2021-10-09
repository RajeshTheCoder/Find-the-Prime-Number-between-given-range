# Find-the-Prime-Number-between-given-range-in-Java
import java.util.*;
public class Main
{
    public  static boolean isPrime(int num)
{
    int i;
    for(i=2;i<=Math.sqrt(num);i++)
    {
        if(num%2==0)
        {
            return false;
        }
    }
    return true;
}
	public static void main(String[] args) {
		Scanner sc=new Scanner(System.in);
		int num=sc.nextInt();
		Main x=new Main();
		int i,j,arr[];
		arr = new int[10000];
		for(i=2;i<=num;i++) arr[i]=i;
		for(i=2;i<=Math.sqrt(num);i++)
		{
		    if((arr[i]!=0) && (x.isPrime(i)))
		    {
		        for(j=2;i*j<=num;j++) arr[i*j]=0;
		    }
		}
	for(i=2;i<=num;i++){
	   if(arr[i]!=0)
	      System.out.print(arr[i]+" ");
	}
	}
}


