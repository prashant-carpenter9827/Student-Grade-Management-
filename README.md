import java.util.Scanner;
 
public class Studentgradecalculator {
    public static void main(String[] args) {
        int j, i;
        float totalMarks = 0, percentage, average;
        
        Scanner sc = new Scanner(System.in);
 
        System.out.println("Enter Number of Subject");
        j = sc.nextInt();
 
        System.out.println("Enter Marks of " + j + " Subject");
        for (i = 0; i < j; i++) {
            totalMarks += sc.nextInt();
        }
         
        System.out.println("Total Marks : " + totalMarks);
      
        percentage = (totalMarks / (j * 100)) * 100;
 
        switch ((int) percentage / 10) {
        case 9:
            System.out.println("Grade : A+");
            break;
        case 7:
            System.out.println("Grade : A");
            break;
        case 6:
            System.out.println("Grade : B");
            break;
        case 5:
            System.out.println("Grade : C");
            break;
        default:
            System.out.println("Grade : D");
            break;
        }
    }
}
