# java-notes

### List
```java
List<Integer> res = new ArrayList<>();
res.add(0);
int sizee = res.size();
res.get(j); // res[j] in list

```
### Heap
```java
PriorityQueue<Integer> minheap = new PriorityQueue<>(); // 1 2 3 4

PriorityQueue<Integer> maxheap = new PriorityQueue<>((a, b)->{ // 4 3 2 1
  return b-a; 
});

minheap.peek();
minheap.poll(); // also return the top element 

minheap.add(2);
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

### HashSet
```java
Set<Integer> hash_set = new HashSet<Integer>();
hash_set.add(x);
hash_set.contains(x);
```
### Array
```java
int rank[] = new int[26];
Arrays.fill(rank, -1);
Arrays.sort(rank);
return new int[] {-1,-1};
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
```
