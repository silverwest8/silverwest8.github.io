# Chapter 3 - for

## ⭐️  빠른 입출력

- Scanner 는 느림!!!!!
- Java를 사용하고 있다면, `Scanner`와 `System.out.println` 대신 `BufferedReader`와 `BufferedWriter`를 사용할 수 있다. `BufferedWriter.flush`는 맨 마지막에 한 번만 하면 된다.
- BufferedWriter 외에도, StringBuilder로 출력을 모아 놓았다가 그 String을 System.out.println하는 방법도 있습니다.

```java
import java.io.BufferedReader;
import java.io.BufferedWriter;
import java.io.IOException;
import java.io.InputStreamReader;
import java.io.OutputStreamWriter;
import java.util.StringTokenizer;

public class step3_4 {
    public static void main(String[] args) {
        try {
            BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
            BufferedWriter bw = new BufferedWriter(new OutputStreamWriter(System.out));
            int T = Integer.parseInt(br.readLine());
            StringTokenizer st = null;
            for (int i = 0; i < T; i++) {
                st = new StringTokenizer(br.readLine(), " ");
                bw.write( Integer.parseInt( st.nextToken() ) + Integer.parseInt( st.nextToken() ) + "\n");
            }
            bw.flush();
            br.close();
            bw.close();
        } catch (IOException e) {
            e.printStackTrace();
            System.out.println(e.getMessage());
        }
    }
}
```

*** 참고

[[백준] 15552번 : 빠른 A+B - JAVA [자바]](https://st-lab.tistory.com/30)

[20210121.zip](Chapter%203%20-%20for%20da6d6e5c3f5745eb8d365c6f572696db/20210121.zip)