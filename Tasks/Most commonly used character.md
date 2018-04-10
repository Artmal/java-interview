## Max chars problem
Given a string, return the character that is most commonly used in the string. 
Examples:
maxChar("abcccccd") => 'c'

My solution:

    public static char findMostCommonlyUsedCharacter(String str) {  
        Map<Character, Integer> occurrences = new HashMap<>();  
      
	    char[] chars = str.toCharArray();  
	    for(int i = 0; i < chars.length; i++) {  
	        if(!occurrences.containsKey(chars[i])) {  
                occurrences.put(chars[i], 1);  
	    } else {     
	        Integer previousNumberOfOccurrences = occurrences.get(chars[i]);  
		    occurrences.put(chars[i], previousNumberOfOccurrences + 1);  
	    }  
     }  
      
        char mostCommonlyUsedCharacter = 0;  
	    int maxNumberOfOccurrences = 0;  
      
	     for(Map.Entry<Character, Integer> entry : occurrences.entrySet()) {  
            Integer numberOfOccurrences = entry.getValue();  
      
		    if(numberOfOccurrences > maxNumberOfOccurrences) {  
                maxNumberOfOccurrences = numberOfOccurrences;  
			    mostCommonlyUsedCharacter = entry.getKey();  
		    }  
        }  
      
        return mostCommonlyUsedCharacter;  
    }

