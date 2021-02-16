# Chapter 7 - String

### 7-(3)

아스키 코드 활용해서 알파벳 다루기

```java
import java.util.Scanner;

public class step7_3 {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String word = sc.nextLine();
        sc.close();
        for (int i = 97; i < 97+26; i++) {
            char C = (char)i;
            System.out.print(word.indexOf(C)+" "); 
        }
    }
}
```

### 7-(4) 문자열 반복

.nextInt() → 공백 → .nextLine()

nextLine을 받은 string의 0번째 인덱스에 공백이 추가됨 → .trim()으로 정리