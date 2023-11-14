[[Java] 입출력 BufferedReader / BufferedWriter](https://itkjspo56.tistory.com/178)

[Scanner와 BufferedReader / BufferedWriter의 차이점과 사용법](https://juno-juno.tistory.com/99)



stringBuilder 

[[JAVA] BufferedReader, BufferedWriter, StringBuilder](https://chb2005.tistory.com/73)

1. 문자열 연결
   
   ```java
   StringBuilder sb = new StringBuilder();
   sb.append("Hello");
   sb.append(" ");
   sb.append("world");
   String result = sb.toString(); // result는 "Hello world"
   ```

2. 반복문에서 문자열 빌드
   
   ```java
   StringBuilder sb = new StringBuilder();
   for (int i = 0; i < 10; i++) {
       sb.append(i).append(" ");
   }
   String result = sb.toString(); // result는 "0 1 2 3 4 5 6 7 8 9 "
   ```

3. 문자열 삽입
   
   ```java
   StringBuilder sb = new StringBuilder("Hello world");
   sb.insert(5, ", "); // "Hello, world"로 변경
   ```

4. 문자열 역순으로 변경
   
   ```java
   StringBuilder sb = new StringBuilder("Hello");
   sb.reverse(); // "olleH"로 변경.
   ```

5. 문자열 삭제
   
   ```java
   StringBuilder sb = new StringBuilder("Hello");
   sb.delete(2, 4); // "Heo"로 변경.
   ```

6. 문자열 대체
   
   ```java
   StringBuilder sb = new StringBuilder("Hello");
   sb.replace(2, 4, "p"); // "Help"로 변경.
   ```
