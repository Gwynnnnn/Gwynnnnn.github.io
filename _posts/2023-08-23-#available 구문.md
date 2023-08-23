---
layout: post
tags: swift
categories: swift

---

### available 구문

```swift
if #available (<플랫폼이름 버전>, <...>, <*>){
  <해당 버전에서 사용할 수 있는 API구문>
}else{
  <API를 사용할 수 없는 환경에 대한 처리 
}
```

이 구문을 사용하는 이유는 OS버전마다 API구문이 다르게 지원되거나 업데이트 이후 더이상 지원하지않는 OS버전을 위해 사용한다. 



이 구문을 사용할 때 호출 연산자 () 를 통해 플랫폼 이름과 버전 등의 인자값을 이용할 수 있는데 이때 플랫폼 이름과 버전 사이는 공백으로 구분한다. 



버전값의 나열이 끝나면 마지막은 *로 마감하고 괄호를 닫아주면 된다. 



예를 들면

```swift
if #available(iOS 9, OSX 10.10, watchOS 1,*) {
  // iOS 9 용 구문, OSX 10.10 용 API구문, watchOS 1 API 구문 
} else {
  // API를 사용하지 못했을 때에 대한 실패 처리
}
```

이런 형식으로 사용된다. 
