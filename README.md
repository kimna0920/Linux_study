# Linux_study
<h3>01 디렉토리와 파일 관련 명령어</h3>
  <b>ls</b>
  <p>현재 디택토리의 파일 목록을 출력하는 명령어.'ls-l'은 자세히 보기</p>
  
  <b>pwd</b>
  <p>현재 위치하고 있는 디렉토리를 알려주는 명령어</p>
  
  <b>mkdir</b>
  <p>mkdir 새로 생성할 디렉토리명</p> 
  
  <b>cd</b>
  <p>cd 이동할 디텍토리의 경로명</p>
  
  <b>rm</b>
  <p>
    <li>
      rm 파일명
    </li>
    <li>
      rm-r 디텍토리명
    </li>
  </p>
  
  <b>--help/man</b>
  <p>명령어 뒤에 --help/ man를 붙이면 명령의 사용설명서가 출력됨</p>
  <p>
  <div>
  예
    <li>
      ls--help
    </li>
    <li>
      rm--help
    </li>
    <li>
      mkdir--help
    </li>
    <li>
      pwd--help
    </li>
  </div>
  <br>
  <div>
   man 매뉴얼 사용법
    <li>
      q키 - 나가기
    </li>
    <li>
      h키 - man 사용법 확인
    </li>
    <li>
      화살표키, 엔터키 - 한줄씩 넘기기
    </li>
    <li>
      스페이스바 - 한 페이지씩 넘기기
    </li>
  </div>
  </p>
  
<h3>02 리눅스 명령어 기초</h3>
<b>sudo (superuser do)</b>
<p>현재 계정에서 root 권한을 이용하여 명령어를 실행할 때 사용</p>
<li>
  sudo -i/sudo -s - root 계정으로 전환가능
</li>

<h3>03 Command Line Interface</h3>
<b>GUI vs CLI</b>
<li>
  GUI 윈도우 시스템, 아이콘, 메뉴, 포인팅 디바이스 등의 요소에 의해 구성되는 컴퓨터 조직 환경
</li>
<li>
  CLI 가상 터미널 또는 터미널을 통해 사용자와 컴퓨터가 상호 작용하는 방식
  <b>[GUI가 할 수 있는 모든 작업은 CLI로 할 수 있다]</b>
</li>

<h3>04 IO Redirection</h3>
<b>UNIX programs</b>
<li>
  <b>input:</b>
  <ul>
    program arguments(프로그램 인수)<br>
    [제어 정보 control information]
  </ul>
  <ul>
    environment variables(환경 변수)<br>
    [상태 정보 state information]
  </ul>
  <ul>
    standard input(표준 입력)<br>
    [데이터 data]
  </ul>
</li>

<li>
  <b>output:</b>
  <ul>
    return status code(반환 상태 코드)<br>
    [제어 정보 control information]
  </ul>
  <ul>
    standard out(표준 출력)<br>
    [데이터 data]
  </ul>
  <ul>
    standard error(표준 에러)<br>
    [에러 메세지 error messages]
  </ul>
</li>

<li>
  활용: 
  <ul>
    ls -la > result.txt
    ('>' 를 이용하면 모니터에 출력될 파일리스트를 result.txt라는 파일에 입력으로 넣을 수 있다)<br>
    rm result.txt 2> result2.txt
    (rm result.txt 에 대한 오류메세지가 result2.txt에 담긴다)
  </ul>
</li>
<b>Append</b>
<li>
  활용:
  <ul>
    ls -al >> result.txt
    (ls -al 실행결과가 result.txt에 담긴다)
    <br>
    mail ((이메일주소입력)) <<eot
    > i
    > want to go home...
    (이메일에 다음 내용이 전송됨)
    <br>
    ls -al > /dev/null
    (실행결과가 /dev/null로 리다이렉션된다,즉 실행결과 삭제된다)
  </ul>
</li>
