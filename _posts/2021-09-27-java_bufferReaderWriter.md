---
title: "[자바(JAVA)] BufferReader"
categories:
- JAVA
tags: 
- [JAVA, BufferReader, BufferWriter]
date: 2021-09-27
last_modified_at: 2021-09-27
toc: true
toc_sticky: true
toc_label: "BufferReader/Writer"
---

## 버퍼(Buffer)

데이터를 한 곳에서 다른 한 곳으로 전송하는 동안 일시적으로 메모리를 보관하는 임시 메모리 영역.
I/O 접근 빈도가 적어서 성능이 Scanner에 비해서 좋다.

## BufferReader

- 사용자로부터 데이터를 받을 때는 객체를 생성하여 입력을 받는다.
- Enter를 쳐야 입력의 마지막으로 인식한다.
- 예외처리를 반드시 해줘야한다! (try/catch 혹은 throws IOException)
- readLine의 return값은 String값이다. 다른 타입으로 받으려면 형변환 필요함!

```java
BufferReader 변수명 = new BufferReader(new InputStreamReader(System.in));
String s = 변수명.readLine();

[ex]
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        String s = br.readLine();
        int i = Integer.parseInt(br.readLint()) // String이 아닌 타입으로 입력을 받으려면 형변환 해줘야함!
        System.out.println(s);
    }
```

## BufferWriter

- flush()를 호출해서 남은 데이터를 호출해줘야한다.
- close() 를 호출해서 닫아주어야한다.
- 자동개행이 없어서 `\n`을 통해서 개행을 해야한다.

```java
BufferWriter 변수명 = new BufferWriter(new OutputStreamWriter(System.out));

[ex]
    public static void main(String[] args) throws IOException {
        BufferedWriter bw = new BufferedWriter(new OutputStreamWriter(System.out));
        String h = "Hello";
        String w = "World";
        bw.write(h+"\n"+w);
        bw.flush();
        bw.close();
    }
```
출력 결과   
![img](/image/java_bw.PNG)
