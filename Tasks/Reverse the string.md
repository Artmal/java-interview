## Reverse the string
My language agnostic solution:

    public static String reverse(String input) {  
     char[] chars = input.toCharArray();  
      
     for(int i = 0; i < chars.length / 2; i++) {  
          char tmp = chars[i];  
      
		  chars[i] = chars[chars.length - 1 - i];  
	      chars[chars.length - 1 - i] = tmp;  
      }  
	      return new String(chars);  
    }

