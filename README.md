# Hexadecimal-to-Decimal-
This is the code for conversion of hexadecimal to decimal in JAVA. 


import java.util.Scanner;
public class Conversion {
    public static void main(String[] args){
        Scanner scanner = new Scanner(System.in);
        String hexString = scanner.nextLine();

        //Check if the hex string has exactly one character
        if (hexString.length() !=1) {
            System.out.println("You must enter the exactly one character");
            System.exit(1);
        }

        //Display decimal value for the hex digit
        char ch = hexString.charAt(0);
        if (ch <= 'F' && ch >= 'A') {
            int value = ch - 'A' + 10;
            System.out.println("The decimal value for hex digit" + ch + " is " + value);
        }
        else if (Character.isDigit(ch)) {
            System.out.println("The decimal value for hex digit" + ch + " is " + ch);
        }
        else {
            System.out.println(ch + "  Bis an invalid input");
        }
    }
}
