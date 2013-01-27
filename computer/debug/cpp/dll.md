# 존재하는 DLL을 LoadLibrary하는데, null을 return한다.
 1. 상대주소로 적은 경우 dll이 경로에 없다.
  * dll의 검색 순서는
   1. exe파일의 경로
   1. 현재 디렉토리
   1. %Systemroot%system32
   1. %Systemroot%
   1. 환경변수 PATH에 추가된 위치.
 1. 절대주로 적을때 "C:\tmp"에 있다면 "C:\\\\tmp"라고 해야한다.
 1. argument로 TEXT를 넘겨야 한다.
  * 예를들어 "a.dll"이 아니라TEXT("a.dll")을 인자로 넘겨야 한다.
