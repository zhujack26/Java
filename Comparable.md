

sort(단일기준) vs Comparable (정렬 기준이 여러 개) 



//영어 점수가 높은 학생 순으로 정렬하되 영어 점수가 같으면 수학점수가 높은 학생을 선순위로 정렬하기



step1. 점수 클래스 생성하기

```java
Class Score {
    int english;
    int math;

    public Score(in english, int math) {
    super();
    this.english = english;
    this.math = math;
}
//오른쪽 마우스 클릭 -> source -> Generate Constructor using Fields
@Override
public String toString() {
    return "Score [english= " + english + ", math = " + math + "]";
}
//오른쪽 마우스 클릭 -> source -> Generate to String()
}
```

step2. implement Comparable

```java
Class Score implements Comparable <score> {
    int english;
    int math;

    @Override
    public int compareTo(Scroe o) {
    //TODO Auto-generated method stub
    return 0;
}
}
```



step3. compareTo 함수 구현하기

```java
@Override
public int compareTo(Score o){
    //영어 점수로 정렬
    if(this.english != o.english){
    return o.english - this.english;
}
return o.math- this.math;
}
//영어 점수가 같지 않을 때만 동작
/*return 값이 양수인지 음수인지만 중요
매개변수 데이터가 더 클 때 음수 리턴 -> 오름차순, 양수 리턴 -> 내림차
```



step4. 정렬하기

```java
ArrayList<Score>A = new ArrayList<>();


A.add(new Scroe(80, 100));
A.add(new Scroe(100, 100));
A.add(new Scroe(70, 80));
A.add(new Score(100, 90));


Collections.sort(A);

for(int i = 0; i < A.size(); i++){
    System.out.println(A.get(i).toString());
}
```
