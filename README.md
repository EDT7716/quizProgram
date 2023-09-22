# quizProgram

2023 애니그마 활동용 프로그램 코드입니다.

<프로그램 기능>\n
1.도입부에 닉네임 입력, 퀴즈의 부문 선택

2.각 퀴즈에 대한 설명 안내
3.랜덤 순서로 퀴즈 배치
4.문제를 맞힐 때마다 1점 획득
5.모든 문제 풀이 후 최종 스코어 표시
6.기록을 txt형태의 파일로 저장, 원한다면 랭킹 출력

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