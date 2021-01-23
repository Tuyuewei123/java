# java
import java.util.Scanner;
//选择排序
public class XuanZe {

    public static void main(String[] args) {

        Scanner sc = new Scanner (System.in);
        int[] arr = new int [10];
        for (int i = 0; i < arr.length; i++) {
            arr[i]=sc.nextInt();
        }
        for (int i = 0; i < arr.length; i++) {
            for (int j = 1; j < arr.length; j++) {
                int temp=0;
                if (arr[i]>arr[j]) {
                    temp=arr[i];
                    arr[i]=arr[j];
                    arr[j]=temp;
                }
            }
        }
        for (int i = 0; i < arr.length; i++) {
            System.out.print(arr[i]+" ");
        }
    }
}
//冒泡排序
import java.util.Scanner;
public class MaoPao {
    public static void main(String[] args) {
        Scanner sc=new Scanner(System.in);
        int[] arr=new int[10];
        for (int i = 0; i < 10; i++) {
            arr[i]=sc.nextInt();
        }
        for (int i = 1; i <arr.length ; i++) {
            for (int j = 0; j <arr.length-1 ; j++) {
                if (arr[j]>arr[j+1]) {
                    int temp=0;
                    temp=arr[j];
                    arr[j]=arr[j+1];
                    arr[j+1]=temp;
                }
            }
        }
        for (int i = 0; i < arr.length; i++) {
            System.out.print(arr[i]+" ");
        }
    }
}
//杨辉三角
public class YangHui {
    public static void main(String[] args) {
        int[][] arr=new int[10][];
        for (int i = 0; i <10 ; i++) {
            arr[i]=new int[i+1];
            arr[i][0]=1;
            arr[i][i]=1;
        }
        for (int i = 2; i <10 ; i++) {
            for (int j = 1; j <arr[i].length-1 ; j++) {
                arr[i][j]=arr[i-1][j-1]+arr[i-1][j];
            }
        }
        for (int i = 0; i < 10; i++) {
            for (int j = 0; j < arr[i].length; j++) {
                System.out.print(arr[i][j]+"  ");
            }
            System.out.print("\n");
        }
    }
}
