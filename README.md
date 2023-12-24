
Credit card numbers follow certain patterns. A credit card number must have between 13 and 16 digits. It must start with

    4 for Visa cards
    5 for Master cards
    37 for American Express cards
    6 for Discover cards

In 1954, Hans Luhn of IBM proposed an algorithm for validating credit card numbers. The algorithm is useful to determine whether a card number is entered correctly, or whether a credit card is scanned correctly by a scanner. Credit card numbers are generated following this validity check, commonly known as the Luhn check or the Mod 10 check, which can be described as follows (for illustration, consider the card number 4388576018402626):

    Double every second digit from right to left. If doubling of a digit results in a two-digit number, add up the two digits to get a single-digit number.
    Article on Luhn check: https://www.geeksforgeeks.org/luhn-algorithm/
    Now add all single-digit numbers from Step 1.
    4+4+8+2+3+1+7+8=37 display style 4 plus 4 plus 8 plus 2 plus 3 plus 1 plus 7 plus 8 equals 37
    Add all digits in the odd places from right to left in the card number.
    6+6+0+8+0+7+8+3=38 display style 6 plus 6 plus 0 plus 8 plus 0 plus 7 plus 8 plus 3 equals 38
    Sum the results from Step 2 and Step 3.
    37+38=75 display style 37 plus 38 equals 75
    If the result from Step 4 is divisible by 10, the card number is valid; otherwise, it is invalid. For example, the number 4388576018402626 is invalid, but the number 4388576018410707 is valid.

Write a program that prompts the user to enter a credit card number as a long integer. Display whether the number is valid or invalid. Design your program to use the following methods:

     /** Return true if the card number is valid */
     public static boolean isValid(long number) 

     /** Get the result from Step 2 */
     public static int sumOfDoubleEvenPlace(long number) 

     /**
     * Return this number if it is a single digit, otherwise, return the sum of the
     * two digits
     */

     public static int getDigit(int number)

     /** Return sum of odd place digits in number */
     public static int sumOfOddPlace(long number)

    /** Return true if the number d is a prefix for number */
    public static boolean prefixMatched(long number, int d)

    /** Return the number of digits in d */
    public static int getSize(long d)


    /**
     * Return the first k number of digits from number. If the number of digits in
     * number is less than k, return number.
     */
    public static long getPrefix(long number, int k)


