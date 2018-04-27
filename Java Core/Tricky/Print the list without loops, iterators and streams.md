## Print list of strings without loops, iterators, stream

Suppose you have:

    List<String> strings = new ArrayList<>();  
    strings.add("1");  
    strings.add("2");  
    strings.add("3");  
    strings.add("4");  
    strings.add("5");  
    strings.add("6");  
    strings.add("7");  
    strings.add("8");

Print the list without aforementioned constructs.

Solution:

    public static void print(List<String> strings, int index) {  
        if (index >= strings.size()) {  
            return;  
      }  
      
        System.out.println(strings.get(index));  
      print(strings, index + 1);  
    }

