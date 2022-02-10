# Android & Kotlin
#### ! 난생 처음이라 잘못 이해 했을 가능성 농후하나 프로젝트가 끝나면 다시 개념을 짚어가며 수정해보자!
> 22.02.10 안드로이드 스튜디오 구성 이해하기
* activitly_main.xml : 사용자가 보는 Main화면
  - 웹에서 HTML와 CSS의 역할을 한다고 생각했다.
* MainActivity.kt 파일 : Main화면(activitly_main.xml)안에서 쓸 동작, 기능들을 작성할 파일
  - 웹에서 JavaScript의 역할을 한다고 생각했다.
> > MainActivity.kt 파일
```kotlin
package com.example.basic1 
// package : class들을 묶은거
// basic1 : 어플이름, basic1이라는 이름의 패키지 선언

import androidx.appcompat.app.AppCompatActivity 
import android.os.Bundle
// import : 사용할 내장된 기능들 가져오기
// !!..순서는 헷갈리니까 나중에 다시 공부하기!!

class MainActivity : AppCompatActivity() { 
// Class: 값과 함수(method())로 구성할 수 있는 틀(붕어빵틀), Object(객체): class(틀)로 만들어낸 것(붕어빵),인스턴스라고도 함.
// 내가 이해한 object와 Instance의 차이 : class1로 만든 객체를 O1, class2로만든 객체를O2라고 하면 
//                                      01는 class1의 인스턴스, 02는 class2의 인스턴스, 즉 ((관계))를 설명해줌
//                                      O1과 O2모두 값이 할당되어 있으니까 둘다 객체라고 부름.
// MainActivity : AppCompatActivity라는 class를 상속받은 새로운 class의 이름(이름 바꿀수 있음)
// AppCompatActivity: 안드로이드 하위버전을 지원하는 Activity (compatibiliAty : 호환성)
    override fun onCreate(savedInstanceState: Bundle?) { 
// override : 부모위 클래스의 함수를 재정의
// override fun onCreate() : AppCompatActivity class내의 onCreate()라는 함수의 내용을 변경
// onCreate() : Android의 생명주기는 Activity launched -> OnCreate()->순서, On이 붙으면 콜백 : 해당시점에 실행되는 함수
// !!(savedInstanceState: Bundle?)의 의미는 나중에 찾아보겠다. ?는 null을 허용한다는 의미
        super.onCreate(savedInstanceState)
        // super: 상위클래스의 매서드, 프로퍼티, 생성자를 사용하겠다는 의미
        // this: 해당클래스의 매서드, 프로퍼티, 생성자를 사용하겠다는 의미
        // 생성자 : 클래스 이름과 동일한 이름의 매서드
        // super.onCreate() : 상위 클래스인 AppCompatActivity 클래스의 onCreate()함수를 사용하겠다.
        setContentView(R.layout.activity_main)
        // activity_main.xml 화면을 보여주는 함수 (!! 이게 안드로이드 내의 API인가??? )
    }
}
```


