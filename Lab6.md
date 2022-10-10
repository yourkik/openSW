### Version Control : 
시간에 따라 파일을 저장, "최종 수정"/"진짜 최종 수정"과 같이 이름을 다르게 하여 저장할 수도 있으나 불편하므로  
이를 관리하는 시스템을 활용, 2가지 구현 방식
1. Changes : base 파일에 변화를 따로 저장해 버전에 따라 덮어씌어 출력하는 방식  
2. Snapshots : 버전에 따른 파일을 모두 저장, Git이 사용  

Version Control를 3가지 사용 방식
1. Local : 개인 컴퓨터에서만 Version Control 사용, 외부 사람은 사용 불가
2. Centralized : 중앙 서버에서 Version Control 관리, 중앙 서버 다운 시 저장이 안 됨
3. Distributed : 중앙 서버, 개인의 컴퓨터가 중앙 데이터의 복사본을 가짐(복구 편리), Git이 사용  

Three States in Git : 
1. Modified : 디렉토리 변경(작업), 작업이 끝나 저장할 때 Staging Area로 보냄
2. Staged : 변경 내용을 점검
3. Comitted : 내용을 기록(Snapshot)

Git 구성 레벨 : 
1. System level : --system, 모든 사용자와 repository에 영향을 줌(관리자 권한 필요), file:/etc/gitconfig(저장 경로)
2. Global(user) level : --global, 현 유저 모든 repository에 영향, file:~/.config/git/config
3. Local level : --local, 현 repository에만 영향, file:.git/gitconfig
 
Git command :
 $git init($는 명령어라는 의미) : 새로운 git repository 생성
 $git status : 현재 respository가 어떤 status인지 확인  
 $git add . : 모든 repository를 Staging Area로 올림  
 $git rm —cached filename : Staging Area에서 내림(cached를 붙여야 사라지지 않고 내려옴)  
 $nano(editor) .gitignore : 입력된 파일을 무시(추천), !로 시작시 파일을 포함  
 $git commit –m “commit message” : 파일을 commit(저장)  
 $git branch –m master main : 현재 branch를 master -> branch로  
