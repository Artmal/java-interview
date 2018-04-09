## Palindrome

Give a string, return true if the string is a palindrome or false if it is not. Palindromes are strings that form the same word if it is reversed. Examples: 
palindrome("abba") => true
palindrome("abc") => false

**My solution:**

    public static boolean palindrome(String input) {  
        String reversed = new StringBuilder(input).reverse().toString();  
	    return input.equals(reversed);  
    }

