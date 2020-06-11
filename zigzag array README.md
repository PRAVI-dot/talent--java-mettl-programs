# talent--java-mettl-programs
import java.io.; import java.math.; import java.security.; import java.text.; import java.util.; import java.util.concurrent.; import java.util.function.; import java.util.regex.; import java.util.stream.*; import static java.util.stream.Collectors.joining; import static java.util.stream.Collectors.toList; import java.util.Scanner;

public class Zigzag { public static void main(String[] args) { int a[],b,count=0,counts=0; Scanner in=new Scanner(System.in); b=in.nextInt(); a=new int[b]; int sub=0,sum=0; for(int i=0;i<b;i++) { int c=in.nextInt(); a[i]=c; } for(int j=0;j<b-2;j++) { if(j%2==0) { if(a[j]<a[j+1]) { continue; } else { a[j+1]=0; j++; count++; } } else { if(a[j]>a[j+1]) { continue; } else { a[j+1]=0; j++; count++; } } }

for(int k=0;k<b-2;k++) { if(k%2==0) { if(a[k]>a[k+1]) { continue; } else { a[k+1]=0; k++; counts++; } } else { if(a[k]<a[k+1]) { continue; } else { a[k+1]=0; k++; counts++; } } } if(count<counts) { System.out.println(count); } else { System.out.println(counts); } } }
