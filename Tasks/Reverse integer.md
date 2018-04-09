## Reverse integer
My solution:

    public static int reverse(int number) {  
        String str = String.valueOf(number);  
        String s = new StringBuilder(str).reverse().toString();  
        
        return new Integer(s);  
    }

