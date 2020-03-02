# Installing
## user 종류
### admin
- app을 설치할 수 있으며, user를 위한 object를 설정 혹은 만들 수 있음
### power
- user를 위한 object를 설정 혹은 만들 수 있으며 realtime 검색이 가능함
### user
- user 자신이 소유한 object만 볼 수 있으며 object를 공유할 수 있음


# Getting data
## ingest data
- 오직 admin 유저만 데이터를 넣을 수 있음
- data를 넣기 위한 방법으로 3가지 방법이 존재
    1. upload file        
        - admin 유저의 로컬 pc에서 파일을 올리는 방식
        - index가 한번 생성되고 이후에는 추가적으로 생성되지 않음
    2. monitor
       - 지속적인 변화를 관찰하기 위한 입력 방식
       - 파일, 이벤트, tcp/udp 또는 script를 관찰할 대상으로 설정할 수 있음
       - 입력 데이터의 종류는 다음과 같을 수 있음
        ```
        - event logs
        - file system changes
        - active directoy
        - network information
        ```       
    3. forward
        - 외부 포워더를 통해 데이터를 입력받음
        - production 상황에서 가장 많이 쓰이는 방식
## upload 과정
- 파일의 구조(ex)cvs) 를 확인한 수 자동으로 sourcetype를 생성
- sourcetype이 생성된 방식이 마음에 들지 않을 경우 재설정 가능
- 미리 설정된 sourcetype을 통하여 입력되는 정보를 분할할 수 있음
- sourcetype을 볼 수 있는 tab에 hostname과 host 정보가 있는데, host는 입력한 host의 정보, hostname은 어디서 입력이 왔는지를 의미함
## 인덱스 분할의 이유
- 검색 속도를 향상시킬 수 있음
- admin이 user가 볼 수 있는 index를 제한시킬 수 있음
- custom된 접근 제한을 index별로 설정할 수 있음
## monitoring
- 디렉토리를 target으로 지정할 경우, black_list와 white_list를 설정할 수 있음


# Basic Search
## search and report app
- 7개의 컴포넌트 존재
- splunk bar, app bar, search bar, "how to search" panel, "what to search" panel, search history menu 
- sources 가 의미하는 바는 어디서 데이터가 생산되었는가 이다
- host 는 주로 ip, domain name, 혹은 데이터가 생산 된 머신의 정보
## using search bar
- 시간으로 필터하는 것이 가장 효과적인 방법
- pattern tab 에서 raw 데이터를 확인할 수 있음
## search job
- search job
    - search job의 결과는 기본으로 10분 동안 유지되게 설정되어 있음
    - 10분이 지난 이후, splunk는 새로운 결과를 얻기 위해 검색을 다시 실시함    
- shared search job
    - Shared search job 은 7일 동안 같은 데이터가 유지됨
    - 모든 유저가 같은 데이터를 확인하게 됨
## search mode
- fast search
    - 반환되는 필드의 숫자를 줄여서 검색 속도를 향상시킴
    - field discovery mode 는 사용이 불가능함
- verbose mode
    - 유저가 원하는 만큼의 필드를 전부 반환함
- smart mode
    - 입력된 검색어를 기반으로 검색 mode를 변환함 
## zoom in and zoom out
- zoom in 을 할 경우 검색된 데이터를 그대로 사용
- zoom out 을 할 경우 새로운 검색을 실시
## transforming
- commands that create statistics and visualizations are called transforming commands
- 통계 정보 혹은 차트를 위한 정보를 만드는 명령어를 transforming 이라 함
## timezone format
- 데이터에 date 정보가 들어있을 경우 user의 timezone 세팅을 기준으로 해당 시간을 표시함
## search term
- NOT, OR, AND 명령어를 boolean operation 이라 함
- boolean operation 이 검색 키워드에 존재하지 않을 경우 기본은 AND로 설정됨
- boolean operation 의 우선순위는 NOT -> OR -> AND 순서임
- 괄호를 이용하여 우선 순위를 변경할 수 있음
## quiz 
- 모든 이벤트가 날짜 기준으로 정렬되어 반환되는 것은 아님


# Using field
## fields sidebar
### selected fields
- selected fields 에 속한 field 는 상대적으로 user 에게 중요하지 않다는 의미  
- 필드를 선택함으로써 결과에서 보여지는 데이터를 제한할 수 있음
### interesting fields
- interesting fields 에 보여지는 필드들은 전체 이벤트 중 최소 20%의 이벤트에 데이터가 존재한다는 의미
### search
- field name 은 대소문자 구별
- search value 은 대소문자 구별하지 않음
- 'IN' 명령어 지원 
### NOT 명령어와 '!='의 차이
- '!='은 데이터가 정확히 일치하지 않는 이벤트를 반환 
- NOT 명령어는 데이터가 일치하지 않거나 데이터가 존재하지 않는 이벤트를 반환


# Basic Practice 
## base practice in search
- 시간에 기반한 필터가 가장 효과적인 필터 방법
- index, source, host, sourcetype 으로 필터하는 방법이 차선책
- index, source, host, sourcetype 은 인덱스 할 때 결정되기 때문에 해당 필드로 필터하는 것이 성능이 좋음
- inclusion 이 exclusion 보다 일반적으로 성능이 좋음
## best practice in using time
- realtime 검색이 현재 일어나고 있는 상황을 관찰하기 위해 사용됨
- realtime 검색은 일정 주기로 일정 기간이 지난 이벤트들을 삭제하고 최신 이벤트들을 새로 넣음
- "@" 표시는 표시 앞에 있는 시간을 표시 뒤에 있는 시간 기준으로 반올림하기 위해 사용됨
## best practice in using indexes  
- admin 유저는 user 의 index 접근을 제한할 수 있음


# The Splunk Seach Language
## Search Terms
## Commands
- Commands 는 검색결과를 이용하여 어떤 추가 작업을 할 것인지를 나타냄
- Commands 는 차트 생성, 통계 계산 등의 명령을 수행함 
## Functions
- Functions explain how we want to chart, compute and evaluate the result
## Arguments
- Arguments are the variables that we want to apply to the function
## Clauses
- clauses explain how we want results grouped, or defined
## pretty
- Ctrl + \ format SPL more readable
## field command
- only selected field will be shown on search result
- negative sign means that field with negative sign will be excluded on search result
- field extraction is one of the most costly parts of searching in splunk
- field inclusion happens before field extraction and can improve performance
## table command
- retains searched data in a tabulated format
- this command is to make search result more easy to understand
- the result of this command will be shown in table
## rename command
- Once renamed, original name is not available to subsequent search commands
## dedup command
- dedup command removes events with duplicate values
## sort command
- numeric field will be displayed in ascending order
- plus mark('+') after sort command means ascending order, minus means descending order
- if there is no space between plus mark and field name, the operation only affects the field directly behind it
- limit operation can be available after sort command  