# Challenge_03
## 비밀 다이어리

SharedPrefereces를 사용하여 사용자 기기에 비밀번호와 내용을 저장한다.

비밀번호는 NumberPicker로 3자리의 비밀번호를 지정하고, Button을 통해 입력할 수 있다.

비밀번호가 일치하지 않거나 비밀번호 변경하는 도중에 Button을 클릭하면 AlertDialog가 호출된다.

MainActivity에서는 비밀번호 변경 기능도 제공한다. unlock 하는 버튼 아래에 passwordchange 버튼이 있고

이 버튼은 NumberPicker로 맞춰져 있는 번호와 현재의 비밀번호가 일치할 경우에만 동작한다. 그렇지 않을경우엔 AlertDialog가 호출된다.

비밀번호 잠금을 해제한 뒤 DiaryActivity로 진입한다.

해당 Activity에서는 내용을 입력할 수 있고, 입력된 내용은 0.5초간 사용자의 입력이 없을 경우에 자동 저장된다.

## 학습 내용
* Layout
  * ConstraintLayout
  * Custom Font
* Handler 사용
  * 안드로이드에서 제공하는 Thread간의 통신을 엮어주는 기능
* SharedPreference의 속성들과 사용법
  * SharedPreferences를 사용하기 위해서는
    * getSharedPreferences(“Sharedprefereces의 이름”, “어떤 모드로 가져올지”)
    *	ex: val detailPreferences = getSharedPreferences(“diary”, Context.MODE_PRIVATE)
  * SharedPreferences의 데이터를 가져올 때
    *	detailPreferences.getString(“key”,”value”)
  *	SharedPreferences에 데이터를 저장할 때
    * Edit KTX function 사용
    *	저장할 때는 Commit 과 apply 두가지 방식이 존재한다.
    *	Commit은 UI 쓰레드를 잠시 블록한 뒤 실제 데이터가 저장될 때까지 기다리는 방식
    *	apply는 기다리지 않고 비동기적으로 저장하는 방식  
*	Theme
  *	NoActionBar
*	AlertDialog
*	Kotlin 문법
    * Android ktx로 SharedPreferences 사용 (Kotlin Android Extension)

