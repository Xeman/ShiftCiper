# ShiftCiper

/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */
package quiz;

/**
 *
 * @author student
 */
import java.util.*;
public class ShiftCipherApp {
    public static void main(String[] args){

	Scanner sc = new Scanner(System.in);
	int shift;
	String message;

	System.out.println("Shift Cipher Algorithm Quiz");
	System.out.println("===========================");
	System.out.print("How many shifts would you want to use? ");
	try {
		shift = sc.nextInt();
		sc.nextLine();
	} 

	catch (Exception e) {
		System.out.println("That is not an integer.");
		System.exit(0);
		return;
	}
	System.out.println("Please enter a message to hit enter to encrypt it.");
	message = sc.next();
	sc.close();
	
        ShiftCipher ci = new ShiftCipher(message, shift);
        ci.cipher();
        System.out.print( ci.getCiphered());
        ci.decipher();
        System.out.print("\n" + ci.getDeciphered() + "\n");
    }
}
