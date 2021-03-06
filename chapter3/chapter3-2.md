# 뷰 컴포넌트

3-2-1 : 전역 컴포넌트 등록하기     

3-2-2 : 지역 컴포넌트 등록하기     

3-2-3 : 지역 컴포넌트와 전역 컴포넌트 등록하기

3-2-4 : 인스턴스 유효 범위와 지역 컴포넌트, 전역 컴포넌트 간 관계 확인하기

뷰에서는 웹 화면을 구성할 때 흔히 사용하는 내비게이션 바, 테이블, 리스트, 인풋 박스 등과 같은 화면 구성 요소들을 잘게 쪼개여 컴포넌트로 관리

<img src = "https://user-images.githubusercontent.com/59350891/108082488-805e7e80-70b5-11eb-9da4-93d355afbbc7.png" width ="65%">

## 컴포넌트 등록하기

1. 지역 컴포넌트 : 특정 인스턴스에서만 유효한 범위를 갖음
2. 전역 컴포넌트 : 여러 인스턴스에서 공통으로 사용 가능

### 전역 컴포넌트 등록

```vue
Vue.component('컴포넌트 이름', {
	// 컴포넌트 내용
});
```

컴포넌트 이름은 template 속성에서 사용할 HTML 사용자 정의 태그 이름을 의미한다

### 지역 컴포넌트 등록

전역 컴포넌트와 다르게 인스턴스에 components 속성을 추가하고 등록할 컴포넌트 이름과 내용을 정의

```javascript
new Vue({
	compoenets: {
		'컴포넌트 이름': 컴포넌트 내용
	}
});
```

## 지역 컴포넌트와 전역 컴포넌트의 차이

 **전역 컴포넌트**는 인스턴스를 새로 생성할 때마다 인스턴스에 components 속성으로 등록할 필요 없이 한 번 등록하면 어느 인스턴스에서든지 사용 가능

**지역 컴포넌트**는 새 인스턴스를 생성할 때마다 등록해줘야 함

