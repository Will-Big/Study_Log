
### 광원의 종류
- Ambient Light
- Directional Light 
	- 빛의 방향 벡터로 계산하기 때문에 위치와 관계 없음
- Point Light
	- 빛의 위치로 계산하기 때문에, 방향과 관계 없음
	- 위치 값의 차이로 생기는 벡터 값으로 계산


### 조명처리
- 확산광, 램버트의 코사인 법칙
	- N dot L
		- 정점별 조명(Per Vertex Light)
			- 고로 쉐이딩
		- 픽셀별 조명(Per Pixel Light)
			- 블린-퐁 쉐이딩
	- 물체의 기본적인 음영
- 주변광(Ambient)
	- 물체의 외곽선
- 반사광(Specular)
	- Reflection dot View
	- 반사광 값을 통해 물체의 재질을 표현함
	- <span style="color:yellow">짐블린의 하프 앵글벡터</span>
		- 기존 반사광의 공식이 당시 성능에 비해 무거웠기 때문에 생긴 공식
		- h = dot(Normal, normalize(Light + View ))


### BRDF
- PBR 을 구현하기 위해 필요한 기능
- 빛의 난반사를 계산하기 위한 마스킹, 쉐도잉,  <span style="color:yellow">미세면 분포도</span>에 대한 수식
	- 블린-퐁
	- 베크먼
	- GGX
- 관련 기능은 찬찬히 찾아보자

결과물 = 텍스처 + 디퓨즈 + 반사광(PBR)

### Disney Diffuse
- Diffuse 에도 PBR 을 적용할 수 없을까? -> 있다!
	- 근데 별 차이가 안난다.
