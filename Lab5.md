### I/O Redirection : 
-Standard Output(기본 출력) : 기본적으로 출력은 스크린으로 뜨나 이를 조정 가능, ‘>’, ‘>>’는 이미 있는 파일 뒤에 추가하여 저장  
ex) ls –lh > file_list.txt -> ls –lh 내용이 file_list.txt에 저장됨  
** cat file_list.txt -> 특정 파일의 내용을 보여줌 ** 

-Standard Input : 파일을 입력하기 위해서 사용 ex) sort < words.txt > sorted_words.txt와 같이 동시에 사용 가능  
   Pipelines : ‘|’, 연결하는 것으로 ‘command1 | command2‘의 형태라면 command1에서 나온 출력이 command2로 바로 들어가게 됨  
**less : 출력이 다른 곳에서 됨, wc –l : 파일 개수를 알려줌 이 두 개를 ls –lh | ~의 형태로 사용*   
   Expansion : 특수한 문자는 쉘 명령에서 의미가 확장됨, echo *은 모든 파일의 이름을 출력, ~는 현재 사용자의 home directory를 ~’이름‘은 특정 유저의 home directory를 출력  
**echo : 뒤에 문자를 출력*   
  
Backslash : ’ \‘, 커맨드가 추가되면서 너무 길어질 경우 이를 나누어 쓸 수 있게 해줌
ex) ls –l \
     --reverse
**-는 약식 명령어 ’--‘는 풀네임을 의미**  
  
Permission(권한) : -rwxrwxrwx 
- '-' : 파일 타입으로 '-'는 파일, 'd'는 directory를 의미  
- 'rwx' : r(read)w(write)x(excute)로 각각 읽고 쓰고 작동(프로그램)의 권한을 의미, 이를 팔진수 0~7로 표현(7 -> 111, 6 -> 110), rwx가 세 묶음이 있는데 각각 파일 소유자, 소유자와  
 같은 그룹의 멤버 그리고 외부의 사람의 권한을 의미, 이 세명의 권한을 세자리의 팔진수로 표시 ex) 777(모두 모든 권한), 700(소유자 외에는 모두 권한 없음)   
   
 chmod ’세자리 숫자‘ ’file_name’ : 세자리 숫자는 권한을 의미하는 것으로 600 -> 110 000 000으로 팔진수를 이진수로 변환하여 권한 설정(즉 777이 모든 유저 모든 권한)  
  
 Superuser(관리자) : sudo some_command, 사용시 주의(변경해서는 안되는 파일을 수정할 수 있게 되기 때문)  
  
TextEditors : Linux에서 텍스트 에디터를 설정 가능  
  
Shell Script : 미리 명령어를 저장해 단축키나 특정 문자를 통해 꺼낼 수 있음, nano myscript.sh -> 이후 텍스트를 입력하는 것과 같이 명령어를 입력(sh 확장자 파일이 만들어짐), sh myscript.sh를 통해 실행 가능  
**history : 지금까지 입력한 모든 명령어를 보여줌**
