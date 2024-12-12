# Code-Convention
코드 컨벤션(Code Convention) : 코드의 일관성과 가독성을 높이고, 유지보수를 쉽게 하기 위해 사용하는 표준화된 규칙

## 1. Code Style
### (1) 들여쓰기(Indentation)
- 보통 4칸의 공백 사용(스페이스 4개 또는 탭).
- 모든 블록({ }) 내부 코드는 한 단계 들여쓰기.
```
if (condition) {  
    // 들여쓰기 예시  
    statement;  
}
```
### (2) 줄바꿈(Line Breaks)
- 한 줄의 길이는 보통 80~120자를 넘지 않도록 제한.
- 긴 줄은 적절한 위치에서 줄바꿈 처리.
```
int result = function_call_with_many_parameters(param1, param2,
                                                param3, param4);
```
### (3) 중괄호 스타일(Brace Style)
- K&R 스타일(권장): 중괄호를 조건문이나 함수의 끝에 붙임.
```
if (condition) {
    statement;
} else {
    statement;
}
```
- Allman 스타일(대안): 중괄호를 새 줄에 작성.
```
if (condition)
{
    statement;
}
else
{
    statement;
}
```
## 2. 네이밍 규칙(Naming Conventions)
### (1) 변수 및 함수 이름
- Camel Case(예: myVariableName) 또는 Snake Case(예: my_variable_name) 사용.
- 변수: 소문자로 시작 (예: count, total_sum).
- 함수: 명확하고 동사로 시작 (예: getData(), setValue()).
### (2) 상수 이름
- 모두 대문자와 언더스코어 사용 (예: MAX_LENGTH, DEFAULT_VALUE).
### (3) 접두사 사용
- 전역 변수는 접두사를 붙여 구분 (예: g_, s_).
- 포인터 변수는 p로 시작 (예: pData).

## 3. 주석(Commenting)
### (1) 단일 라인 주석
- // 사용. 간단한 설명 작성.
```
// 입력 값을 검증하는 함수
void validateInput(int input);
```
### (2) 멀티라인 주석
- /* ... */ 사용. 블록 단위 설명에 적합.
```
/*
 * 이 함수는 입력 값을 검증하고
 * 조건에 따라 결과를 반환합니다.
 */
int validateInput(int input);
```
## 4. 공백 사용(Spacing)
- 연산자 주변: 가독성을 위해 공백 추가.
```
int result = a + b;  // Good
int result=a+b;      // Bad
```
- 함수 정의와 호출: 괄호와 함수명 사이에 공백 없음.
```
void myFunction(int param);  // Good
void myFunction (int param); // Bad
```
## 5. 파일 구조
### (1) 헤더 파일
- 보호 매크로 또는 #pragma once 사용.
```
#ifndef HEADER_FILE_NAME_H
#define HEADER_FILE_NAME_H

// 헤더 파일 내용

#endif // HEADER_FILE_NAME_H
```
### (2) 파일 정리
- 관련 함수 및 선언은 논리적으로 그룹화.
- 불필요한 포함 지양, 필요한 헤더만 포함.
```
#include <stdio.h>
#include <stdlib.h>
```
## 6. 기타
### (1) 매크로 사용
- 매크로 대신 가능하면 const 또는 inline 사용.
```
#define MAX_LENGTH 100   // Avoid
const int MAX_LENGTH = 100;  // Prefer
```
### (2) Magic Number 지양
- 의미 있는 이름의 상수를 정의해 사용.
```
const int PI = 3.14
int calculateArea(int width, int height) {
    // return 3.14 * width * height; // Magic Number 사용 지양
    return PI * width * heigt;
}
```


