# Wheel-of-fortune
/**
 * Write a  which simulates a simple Wheel of Fortune style word game. 
 * Your program will prompt the user for phrase, 
 * then create and print a puzzle with blanks in place of letters, and punctuation filled in.
 * 
 * @author Sean Gray 
 * @version 9/28/2015
 * I received help for one part of my program from the website Stack Overflow with my for loop
 * to make use of CharArray
 * 
 */

import java.util.Scanner;
public class Wheel
{
    public static void main(String []args)
    {
        //due thursday Oct 1
        Scanner in = new Scanner(System.in)'
        
        String guesses = " ";//how many quesses the user takes
        int count = 0;
        Boolean notDone = true;
          
        System.out.println("Enter a phrase:");
        String hiddenPhrase = in.next();
        while (true)
        {
            notDone = false;
            for (char hiddenLetter : hiddenPhrase.toCharArray())
            {
                if (guesses.indexOf(hiddenLetter) == -1)
                {
                    System.out.print('-');//used to cover the letters
                    notDone = true;
                }
                else
                { 
                    System.out.print(hiddenLetter);
                }
            }
            if(! notDone)
            {
                break;
            }
            System.out.print("\nEnter your guess!");
            String letter = in.next();
            guesses +=letter;
            count = count + 1;
        }
        System.out.println("\nCongratulations! It took you " + count + " guesses");
    }
}
