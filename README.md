# project1
/*.Преобразовать строки матрицы таким образом, чтобы элементы, равные нулю, располагались после всех остальных*/

import java.util.*;
import java.util.Arrays;
import java.util.Random;

    public class Matrix {
    private static Scanner sc;
    public static void main(String[] args){
		sc = new Scanner(System.in);
		System.out.println("Enter n:");
		int n=sc.nextInt();
		int[][] arr= new int[n][n];
		fillRandom(arr,n);
		printArr(arr,n);
	    System.out.println("Нули сдвинуты вправо: ");
	    sort(arr);
	    printArr(arr,n);
	}
	
	
	public static void fillRandom(int arr[][],int n){
	      Random random = new Random();
           for (int i = 0; i < n; i++) {
                for (int j = 0; j <n; j++) {
                     arr[i][j] = random.nextInt(2*n+1) - n;
                      }
                  }
           }
	
	
	 public static void printArr(int[][]arr,int n){
		 for (int i = 0; i < n; i++) {
		        for (int j = 0; j <n; j++) {
		         System.out.print(arr[i][j] +  "  ");
		   }
		   System.out.println();
		}
	}
   
	
      public static void sort(int[][] b) {
	     for (int i = 0; i < b.length; i++) {
           int k = 0;
