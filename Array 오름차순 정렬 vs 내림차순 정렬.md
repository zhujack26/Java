Array 오름차순 정렬 vs 내림차순 정렬



오름차순 정렬

```java
import java.util.Arrays;

int A[] = {5, 3, 2, 4, 1};
Arrays.sort(A);
```

O(n log n)  Array.sort() 팀 소트가 사용 된 것,   병합 정렬, 

O(n^2) 삽입 정렬(옆에 보다 빠를 수도), 선택 정렬, 버블 정렬







내림차순 정렬

```java
//방법 1
integer A[] = {5, 3, 2, 4, 1};
Arrays.sort(A, Collections.reverseOrder()); 
//객체의 형태에서만 가능해서 integer배열에서 사용
```

```java
//방법 2
int A[] = {5, 3, 2, 4, 1};
Integer[] tmp = Arrays.stream(A).boxed().toArray(Integer[]::new);
Arrays.sort(tmp, Collections.reverseOredr());
```

```java
int A[] = {-5, -3, -2, -4, -1}; 
//실제로는 5, 3, 2, 4, 1을 저장하고자 하지만 -1을 곱하여 저장

```


