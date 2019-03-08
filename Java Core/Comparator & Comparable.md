## Comparable & Comparator
We implement comparable interface for a class we want to compare if we know the natural ordering(usual ordering for the objects of the class). For example, we want to sort Players by rank:
```
public class Player implements Comparable<Player> {
    ...	
    
    @Override
    public int compareTo(Player otherPlayer) {
        return (this.getRanking() - otherPlayer.getRanking());
    }
    
}
```

It limits us with only way of comparing though. But we can define multiple classes which implements Comparator interface and provide different sorting order, for example:
```
public class PlayerRankingComparator implements Comparator<Player> {
  
    @Override
    public int compare(Player firstPlayer, Player secondPlayer) {
       return (firstPlayer.getRanking() - secondPlayer.getRanking());
    }
}
```
