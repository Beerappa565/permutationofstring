# permutationofstring


import java.io.*;
import  java.util.*;
class GFG {
	public static ArrayList<String> getpermutation(String str)
	{
	    if(str.length()==0)
	    {
	        ArrayList<String>base=new ArrayList<>();
	        base.add("");
	        return base;
	    }
	    char c=str.charAt(0);
	    String ros=str.substring(1);
	        
	    ArrayList<String> rr=getpermutation(ros);
	    ArrayList<String>mr=new ArrayList<>();
	
	    for(String rrs:rr)
	    {
	        for(int i=0;i<=rrs.length();i++)
	        {
	            String val=rrs.substring(0,i)+c+rrs.substring(i);
	            mr.add(val);
	        }
	    }
	    return mr;
	}
	public static void main (String[] args) {
		
	    //Scanner s=new Scanner(System.in);
	    //String str=s.nextLine();
	    //String str="abc";
		System.out.println(getpermutation("abc"));
	}
}
