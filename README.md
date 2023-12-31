# quizProgram

2023 애니그마 활동용 프로그램 코드입니다.

    <프로그램 기능>
1.도입부에서 랭킹을 볼지 퀴즈를 바로 시작할지 선택

1-1.만약 랭킹 출력을 선택했다면 랭킹 출력 후 바로 프로그램을 종료할지 퀴즈를 시작할지 선택

2.퀴즈 시작시 학번과 이름을 입력, 입력 후 퀴즈 부문 선택

2.각 퀴즈에 대한 설명 안내

3.랜덤 순서로 퀴즈 배치

4.문제를 맞힐 때마다 1점 획득

5.모든 문제 풀이 후 최종 스코어 표시

6.기록을 txt형태의 파일로 저장, 원한다면 랭킹 출력


    <각 헤더파일 설명>
#include <stdio.h>:메인 헤더파일

#include <stdlib.h>:난수 생성을 위한 헤더파일

#include <time.h>:시간값을 통한 완전난수 생성을 위한 헤더파일

#include <string.h>:구조체 형성을 위한 헤더파일

#include <stddef.h>:NULL, EOF 연산자 정의를 위한 헤더파일

#include <windows.h>:Sleep 명령어를 통한 딜레이 연출을 위한 헤더파일일

    <각 변수 설명>
int quizType:퀴즈 부문 선택 시 값을 입력받는 변수로, 입력된 정수에 따라 해당 퀴즈를 출력합니다.

int studentID:사용자의 학번을 저장하는 변수입니다.

char playerName:사용자의 이름을 저장하는 변수입니다.

char questions[]:퀴즈 문제들을 저장한 문자열 배열입니다.

int collects[]:각 퀴즈 문제의 정답 번호를 저장한 정수 배열입니다.

char answers[][4]:각 문제에 제공되는 선지를 저장한 2차원 문자열 배열입니다.

int score:퀴즈 풀이 중 사용자의 점수를 저장하는 변수입니다.

int questionOrder:랜덤한 문제 출제 순서를 저장하는 배열입니다.

int randomNumber:랜덤한 숫자를 생성하여 저장하기 위한 변수입니다.

int exists:숫자의 중복을 방지하기 위해 형성한 변수입니다.

int questionIndex:현제 출제된 문제의 인덱스를 나타냅니다.

int userAnswer:사용자가 입력한 답안 번호를 저장하는 변수입니다.

int correctAnswer:올바른 답안 출력을 위해 현제 출제되는 문제의 정답 선지 인덱스를 나타내는 변수입니다.


    <정의된 함수 설명>
savePlayerInfoToFile:사용자의 정보를 지정된 경로의 player_scores.txt 파일에 저장하는 함수

loadPlayerInfoFromFile:사용자의 정보를 지정된 경로의 player_scores.txt 파일에서 읽는 함수

sortPlayerByScore:사용자의 점수를 기준으로 버블 정렬을 사용해 내림차순으로 정리하는 함수

messageOutput:글자 출력 연출을 위한 함수

displayRanking:정리된 랭킹을 출력하는 함수


    <주의사항>
1.구동 프로그램으로 Microsoft Visual Studio를 사용할 경우 맨 윗줄에 #define _CRT_SECURE_NO_WARNINGS 코드를 추가하여 주십시오. scanf_s 미사용 관련 오류를 무시합니다.

2.savePlayerInfoToFile, loadPlayerInfoFromFile 함수에서 scores.txt 파일의 경로를 지정할 때 주 드라이브 바로 밑으로 지정하지 마십시오. 다른 드라이브나 SSD 등의 경로를 지정하시기 바랍니다.

3.현재는 제작자의 SSD로 경로를 설정해놓은 상태입니다. 변경할 시 경로를 알맞은 드라이브로 변경하세요.    
