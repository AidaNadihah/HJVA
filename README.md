/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */

/**
 *
 * @author USER
 */
import java.util.*;   
public class palidrome {  
    private static Scanner aida;

    public static void main(String[] args) {

        System.out.println("Please enter a Palindrome");
        aida = new Scanner(System.in);
        String input = aida.next(); // input character by user
        String original = input;
        input = input.replaceAll("[^a-zA-Z0-9]", ""); // replace the symbol

        System.out.println("************************");
        System.out.println("Input String: " + original);
       // System.out.println("String Reverse:" + " " + stringReverse(input));
        System.out.println(checkString(stringReverse(input), input));
    }

    public static String stringReverse(String a) {
        String result = "";

        for(int i = a.length()-1; i>=0; i--){
            result = result + a.charAt(i);
             
        }
        return result;
       
    }

    public static boolean checkString(String a, String b){
        if(b.equals(a)){
            return true;
        }
        else{
        return false;
        }
    }
}