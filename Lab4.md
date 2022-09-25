Linux : Linux : 서버, 임베이드 시스템, 모바일 점유율이 높음, 개발자에게 널리 활용되는 플랫폼, 보완과 안정성이 뛰어남(코드가 오픈되어 개발자들이 이런 문제를 빠르게 개선,   
소프트웨어 설치/업데이트에 부팅이 필요 없음 -> 서버에 사용되는 이유), CLI 방식으로 동작 
Kernel : 하드웨어와 소프트웨어 연결하는 부분
Shell : 사용자가 필요한 명령어를 전달하는 툴 or 인터페이스, 커널을 직접적으로 다루지 않고 Shell을 통해 전달  

CLI(Command Line Interface) : 명령어를 외워야함, 키보드 위주, 상대적으로 빠름, 반복되는 작업의 자동화 가능, 기본적인 개발 환경(Linux)  
GUI(Graphic User Interface) : 명령어 X, 마우스 위주, 상대적 느림, 자동화 X(Window)  

---  
### Shell 

pwd : 현재 경로를 보여줌  
cd : change directory  
ls : list files and directories  
**Shell에서는 대, 소 문자가 구별됨**  
  
상대 경로 : 하나의 기준을 중심으로 상위, 하위 등의 개념을 통해 위치 지정, ‘.’은 현재 디렉토리를 의미하며 ‘..’은 상위 디렉토리를 의미   
절대 경로 : ex) home/gunwoo/file  

ls : 
- /name :  /name 안에 디렉토리 리스트를 보여줌
- -l(long format) : 더 상세한 정보를 추가(권한, 소유자, 크기, 생성 날짜)  
- -lh : 크기를 사람이 읽기 편한 k를 붙힘
- -la : 모든 파일을 long format으로 출력
**la처럼 option을 합쳐서 사용가능, 특정 디렉토리를 지정할 때 여러개도 가능 ex) ls /bin /etc**  

*권한 맨 앞에 –면 파일(아니면 폴더), 리눅스는 확장자가 없는 파일이 존재, tab를 통해 자동 완성 기능 사용 가능, 키보드 위 방향키를 통해 과거 명령어 사용 가능, clear : 화면을 깨끗하게* 
**리눅스는 여러 사람이 한 서버를 사용하는 것을 전제로 만들어졌기 때문에 권한의 설정이 중요**  

cp : copy files and directories ex) cp module.py backup_module  
- -i : 만약 복사하는 파일의 이름이 존재하면 덮어씌움  
- file1 dir1 : file1을 디렉토리안으로 복사(같은 이름)  
- -R dir1 dir2 : dirl1 -> dir2, dir2가 없으면 생성  

mv : move fils and directories of rename them  
- file1 file2 : file2가 없으면 file1 -> file2, file2가 있으면 대체됨 **(경고 메세지 X)**
- -i 겹치는 이름이 있을 때 덮어씌움(경고 메세지 O)
- file1 file2 dirl : file1과 file2를 dirl로 이동
- dir1 dir2 : 디렉토리에도 사용 가능(이름 변경)  

rm : delete files and directories, 지우면 휴지통의 개념 없이 **영구적으로 지워짐**  
- -i : 경고 메세지 출력
- -r dirl : 디렉토리 안에 모든 파일 삭제  

Wildcards
- \* : All filenames
- g\* : g로 시작하는 모든 파일 이름
- b\*.txt : b로 시작하고 .txt로 끝나는 파일 이름
- Data??? : Data 뒤에 3글자가 더있는 파일 이름  

**rm \*은 모든 파일 삭제로 특히 조심해서 사용** 

help command : help, man(manual, 없을 수도 있음)  

exit : terminal을 닫는 명령어, 윈도우 종료키와 동일  
