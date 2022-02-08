# java-notes
#### [Pass by value](https://stackoverflow.com/questions/12757841/are-arrays-passed-by-value-or-passed-by-reference-in-java/12757860)
### MAX, MIN
```java
System.out.println(Integer.MIN_VALUE);
System.out.println(Integer.MAX_VALUE);
```
### List
```java
List<Integer> res = new ArrayList<>();
res.add(0);
int sizee = res.size();
res.get(j); // res[j] in list
```
#### list to int[]
```java
int [] arr = ...
List<Integer> res = new ArrayList<>();
for(int i: arr){
    res.add(i);
}
return res.stream().mapToInt(i->i).toArray(); 
//or

int[]resArr = new int[arr.size()];
for(int i = 0; i < arr.size();i++){
  resArr[i] = res.get(i);
}
```

### int to double
```java
int x = 1;
int y = 2;
double res = ( x+ 0.0 + y )/2;
```

### HashMap
```java
public boolean isIsomorphic(String s, String t) {
  if(s.length()!=t.length()) return false;
  Map<Character, Character> mapping_map = new HashMap<Character, Character> ();
  for(int i = 0; i <s.length();i++){
      if(!mapping_map.containsKey(s.charAt(i)))
          mapping_map.put(s.charAt(i), t.charAt(i));
      else{
          if(mapping_map.get(s.charAt(i))!= t.charAt(i))
             return false;
      }
  }
  int [] arr = new int[266];
  for(int i = 0; i <t.length();i++){
      int value = s.charAt(i);
      int value2 = t.charAt(i);
      if(arr[value2]==0) arr[value2] = value+1;
      else{
          if( arr[value2] != value+1) return false;
      }
  }
   return true;
}
```
```java
for (Map.Entry mapElement : hm.entrySet()) {
    String key = (String)mapElement.getKey();

    // Add some bonus marks
    // to all the students and print it
    int value = ((int)mapElement.getValue() + 10);

    System.out.println(key + " : " + value);
    }
```

```java
map.put(num, map.getOrDefault(num, 0)+1);
map.put(num, map.get(num)-1);
```

#### Map to List
```java
//Put value and key into list
List<Integer> listOfValue = new ArrayList<Integer>(map.values());
List<String> listOfKeys = new ArrayList<String>(map.keySet());
```

```java
List<Map.Entry<String, Integer> > list = new LinkedList<Map.Entry<String, Integer>>(map.entrySet());
//Sort by the value
Collections.sort(list, (a,b) ->{
    return b.getValue()-a.getValue();
});
```

### HashSet
```java
Set<Integer> hash_set = new HashSet<Integer>();
hash_set.add(x);
hash_set.contains(x);
//Conver hashset to arraylist
ArrayList<String> arr = new ArrayList<>(hash_set)
```

### Array
```java
int rank[] = new int[26];
Arrays.fill(rank, -1);
Arrays.sort(rank);
Integer[] peo = new Integer[people.length];
for(int i=0; i <people.length; i++){
    peo[i]=people[i];
}
Arrays.sort(tas, Collections.reverseOrder());
return new int[] {-1,-1};

int [][]ar = new int [3][4];
// Fill each row with 10. 
for (int[] row : ar)
    Arrays.fill(row, 10);
```
```java
Integer[] arrI = new Integer[arr.length];
for(int i = 0; i < arr.length; i++){
    arrI[i] = arr[i];
}
Arrays.sort(arrI, Comparator.comparingInt(Math::abs));
```

#### Sorting Array
```java
Comparator<Node> comp = (a, b) -> 
    (a.start==b.start) ? (a.end-b.end):(a.start-b.start);

Arrays.sort(node, comp);
```

### Array of ArrayList
```java
ArrayList<Integer> [] graph = new ArrayList[A.length];
for (int i = 0; i < A.length; i++) {
    graph[i] = new ArrayList<Integer>();
}
```

#### List of Pair
```java
List<Pair<Integer, Integer>> directions = new ArrayList<>();
directions.add( new Pair<Integer, Integer>(-1, 0));
directions.add( new Pair<Integer, Integer>(1, 0));
directions.add( new Pair<Integer, Integer>(0, -1));
directions.add( new Pair<Integer, Integer>(0, 1));
```

#### List of List
```java
List<List<Integer>> res =new ArrayList<>();
List<Integer> tmp = new ArrayList<>();
res.add(new ArrayList(tmp));
```

#### 2D Array
```java
int [][] dirs = new int[][] { {0, -1}, {-1, 0}, {0, 1}, {1, 0} };
```

### Sort
```java
List<Character> A = new ArrayList<>();
for(char c : s.toCharArray()){
    A.add(c);
}
Collections.sort(A, (a, b) -> { // list A 
    return rank[a - 'a'] - rank[b - 'a'];
});
```

#### Sort string
```java
 for (String str: strs) {
    char [] c = str.toCharArray();
    Arrays.sort(c);
    String sorted = new String(c);
}
```

### String builder to String
```java
StringBuilder str = new StringBuilder();
for(char c : A){
    str.append(c);
}
return str.toString();
```

#### traverse String (use ``.toCharArray()``)
```java
for(char c : s.toCharArray()){
    A.add(c);
}
StringBuilder strB = new StringBuilder(dominoes);
strB.charAt(current);
strB.setCharAt(current[1],'R');
```

### Queue
```java
 Queue<Integer> q = new LinkedList<>();
 q.add(i);
 // To remove the head of queue.
 
 // Removing Elements: In order to remove an element from a queue, we can use the remove() method. 
 // If there are multiple such objects, then the first occurrence of the object is removed. 
 // Apart from that, poll() method is also used to remove the head and return it. 
 int removedele = q.remove();

 pq.poll();
 // To view the head of queue
 int head = q.peek();
 int size = q.size();
```

#### int[] in queue
```java
Queue<int[]> q = new LinkedList<>();
q.add(new int[]{1, 2});
```

### Heap / Priority Queue
```java
PriorityQueue<E> pq = new PriorityQueue<E>();
pq.add(2);
System.out.println(pQueue.poll());
// Printing the top element again
System.out.println(pQueue.peek());

PriorityQueue<Integer> maxPQ = new PriorityQueue<>((a,b) -> a - b); // 1 2 3 4
PriorityQueue<Integer> maxPQ = new PriorityQueue<>(Collections.reverseOrder()); 
PriorityQueue<Integer> maxPQ = new PriorityQueue<>((a,b) -> b.compareTo(a)); 
PriorityQueue<Integer> maxPQ = new PriorityQueue<>((a, b)->{ // 4 3 2 1
  return b-a; 
});
```
```java
  PriorityQueue<Pair<Integer, Integer>> maxPQ = new PriorityQueue<>(
    (a,b)-> {
    if(b.getKey() == a.getKey()) return b.getValue()- a.getValue();
    return  b.getKey()-a.getKey();
    }
); 
 ```

### LinkedList
```java
ListNode dummy = new ListNode(0, head);
ListNode current = head;
```

### Pair
```java
Pair<Integer, String> pair = new Pair<>(1, "One");
Integer key = pair.getKey();
String value = pair.getValue();
```

## String replace
```java
//Keep letter and numbers
String ns = s.replaceAll("[^a-zA-Z0-9]", "");

//Also keep the space
String ns = s.replaceAll("[^a-zA-Z0-9\\s]", "");

//Replace all a to b
String ns = s.replace("a", "b");
```
