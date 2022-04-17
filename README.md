# Typescript_Compiler
타입스크립트 컴파일과  tsConfig 공부


### Type System

-Structural Type System
  구조가 같으면, 같은 타입이다.
-Nominal Type System
  구조가 같아도, 이름이 다르면 다른타입이다.

### Type Compativility 타입 호환성 

- 같거나 서브 타입인 경우, 할당이 가능하다 => 공변
- 함수의 매개변수 타입만 같거나 슈퍼타입인 경우, 할당이 가능하다. => 반병

### Type Ailas 타입 별칭 

interface 랑 비슷하다.
Primitive, Union Type, Tuple, Function
기타 직접 작성해야하는 타입을 다른 이름을 지정할수 있다.
만들어진 타입의 refer로 사용하는 것이지 타입을 만드는것은 아니다.

### 최상위 프로퍼티 property

- compileOnSave	 
  파일을 세이브 하면 컴파일 하겠다는 설정
- extends			 
  설정이 들어있는 파일을 추가할수 있다. 
- files 			
  가장 센 파일 선정, 상대 혹의 절대 경로의 리스트 배열
- include			
  컴파일 할때 포함 한다.			
- exclude	 
  컴파일 할때 제외 한다.

### compileOptions

type
typeRoots		// 노드 모듈 안에 설치해준다 npm i --save-dev @types/react
references

- target 과 lib 
  target : 빌드의 결과를 어떤 버전에서 할것인가
  lib : 기본 type definition 라이브러리를 어떤 것을 사용할 것인가

- outDir, outFile, rootDir 
  outFile		모듈이 시스템 혹은 AMD 로 지원되야지만 하나의 파일로 만들어진다.
  rootDir 	타입 스크립트의 위치
  outDir		출력 결과의 위치


### Strict 
엄격한 타입 체킹 옵션

- nolmplicitAny		
    명시적이지 않게 any 타입을 사용하여, 표현식과 선언에 사용하면, 에러
- nolmplicitThis		
    명시적이지 않게 any 타입을 사용하여, this 표현식에 사용하면 에러
- structNullChecks		
    체크를 하지 않으면 Null, undefined 가 포함된 형태를 뛰게 된다.
- strictFunctionTypes		
    함수 타입에 대한 매개변수 검사를 한다.
- strictPropertyInitialization	
    정의되지 않은 클래스의 속성이 생성자에서 초기화 되었는지 확인.
- strictBindcallApply		
    bind,call,apply 에 대한 더 엄격한 검사 수행
- alwaysStrict		
    각 소스 파일에 대해 JavaScript의 strict mode 로 코드를 분석하고, "엄격하게 사용"dmf gowp

