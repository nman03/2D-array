import java.util.Scanner;

public class ArrayAverages {
	
	public static void main(String[] args) {
		@SuppressWarnings("resource")
		Scanner in = new Scanner(System.in);
		
		// Prompt
		System.out.print("Enter the number of rows: ");
		int w = in.nextInt();
		System.out.print("Enter the number of columns: ");
		int l = in.nextInt();
		
		System.out.println();
		int[][] table = makeArray(w, l);
		dispArray(table);
		avgArray(table);
		avgEachRow(table);
		avgEachCol(table);
		avgDiagonals(table);
	}
	
	public static int[][] makeArray(int x, int y) {
		int[][] array = new int[x][y];
		
		for (int row = 0 ; row < array.length ; row++) {
			for (int col = 0 ; col < array[row].length ; col++) {
				array[row][col] = (int)(Math.random() * 9);
			}
		} 
		
		return array;
	}
	
	public static void dispArray(int[][] array) {
		for (int row = 0 ; row < array.length ; row++) {
			for (int col = 0 ; col < array[row].length ; col++) {
				System.out.print(array[row][col] + " ");
			}
			System.out.println();
		} 
	}
	
	public static void avgArray(int[][] array) {
		int sum = 0;
		int count = 0;
		
		for (int row = 0 ; row < array.length ; row++) {
			for (int col = 0 ; col < array[row].length ; col++) {
				sum += array[row][col];
				count++;
			}
		} 
		
		System.out.printf("\nAverage of the entire array: %.2f", (double) sum / count);
	}
	
	public static void avgEachRow(int[][] array) {
		int sum = 0;
		int count = 0;
		
		for (int row = 0 ; row < array.length ; row++) {
			for (int col = 0 ; col < array[row].length ; col++) {
				sum += array[row][col];
				count++;
			}
			System.out.printf("\nAverage of row %d: %.2f", row + 1, (double) sum / count);
			sum = 0;
			count = 0;
		} 
	}
	
	public static void avgEachCol(int[][] array) {
		for (int col = 0 ; col < array[0].length ; col++){
			int sum = 0;
			int count = 0;
			for (int row = 0 ; row < array.length ; row++) {
				sum += array[row][col];
				count++;
			}
			System.out.printf("\nAverage of column %d: %.2f", col + 1, (double) sum / count);
		}
	}
	
	public static void avgDiagonals(int[][] array) {
		int majorSum = 0;
		int majorCount = 0;
		int minorSum = 0;
		int minorCount = 0;
		
		for (int row = 0 ; row < array.length ; row++) {
			for (int col = 0 ; col < array[row].length ; col++) {
				if (row == col) {
					majorSum += array[row][col];
					majorCount++;
				}
				if (row + col == array[row].length - 1) {
					minorSum += array[row][col];
					minorCount++;
				}
			}
		}	
		System.out.printf("\nAverage of the major diagonal: %.2f", (double) majorSum / majorCount);
		System.out.printf("\nAverage of the minor diagonal: %.2f", (double) minorSum / minorCount);
	}
	
}
