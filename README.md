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
minheap.pop(); // also return the top element

minheap.add(2);
```

### int to double
```java
int x = 1;
int y = 2;
double res = ( x+ 0.0 + y )/2;
```
