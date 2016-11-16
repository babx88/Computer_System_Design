SUN을 JAVA 프로젝트
=================
----
1. 조원
---

10조 SUN을 JAVA<br>
조원: 유현상(yoo2616), 김호연(guymode), 황인철(babx88)

----
2. 필요성
---

#### **부족 측면**
1. 비타민 D3 결핍증 진료 인원이 2007년 약 1천 800명에서 2011년 약 1만 6천명으로 5년 간 약 1만 4천 200명이 증가하였다.
2. 비타민 D3가 부족하면 뼈 약해지고 휘어진다.
3. 비타민 D3는 심대사질환의 발병 위험을 낮추며, 우울증 예방, 칼슘 흡수를 촉진하여 피로감 극복에 좋다.
4. 이러한 비타민 D3가 부족할 경우, 대사 증후군의 위험이 4.3배 높다는 연구 결과가 나와 많은 사람들이 주목하고 있다. 최근 고려대 구로 병원 가정의학과에서 초등학생 1천600명을 대상으로 조사한 결과, 비타민 D3가 부족한 아이가 대사 증후군에 걸릴 위험이 4배 이상 높은 것으로 나타났다.
5. 날이 흐리거나, 신체의 노출 정도가 약한 겨울에는 햇빛을 온전히 받기 어려우며, 자외선이 강한 오전 10시부터 오후 2시까지는 야외에서 활동하는 것을 자제해야 한다. 이런 제약 조건 속에 부족한 일조량을 채워주기 위한 대안이 필요하다.
6. 자외선이 생물학적인 작용을 통해 정신 건강에 긍정적 영향을 주고 있다는 연구도 있으며 정신 건강 그 자체 또한 매우 중요하게 인식되고 있다.
7. 비타민 D3는 UV로부터 생성할 수 있다. 정확히는 햇빛으로부터 받은 자외선의 도움을 받아 피부세포에 존재하는 ‘7-하이드로콜레스테롤’이 프리비타민 D3(비타민 D3의 전구체)가 된다. 이 프리비타민 D3는 약 50%는 2시간 내에 온도에 의해 비타민 D3로 변한다.  


#### **과잉 측면**
1. 자외선의 과잉으로 피부에게 주는 단기적인 해로움은 홍반과 색소 침착이 있다. 햇빛이 강한 여름의 태양 광선을 30분 이상 피부에 쬐이면 피부에 홍반이 나타난다.
2. 장기간에 걸쳐 피부가 자외선에 노출되면 피부의 노화가 촉진된다. 피부가 얇아지고 주름이 생기고 거칠어지며 피하출혈이 발생한다. 주근깨 또한 악화될 수 있다.
3. 자외선 중 UVB를 많이 쬘 수록 피부 암 발병률이 증가한다. 따라서 올바른 햇빛 만큼을 피부에 쬐주는 것이 중요하다.
4. 백내장은 자외선 등에 의해 유발되며, 자외선이 수정체단백질, 지방, 핵산에 산화적 손상을 주어 수정체 상피, 전부 피질, 핵, 후낭하 부위의 혼탁을 유발시키는 것으로 알려져 있다.

----
3. 개요
---
하루 동안의 사용자의 UV 노출정도를 측정하여 사용자가 집에서 생활을 할 때, 사용자의 부족한 UV양을 분석하여 사용자에게 충분한 UV양을 줄 수 있도록 UV등의 기능과 일반 등의 기능을 동시에 가지는 등을 개발한다.


![readme_img](/static/img/readme_img1.jpg "**Figure 1 구성도**")
----
4. 기능적 요구사항
--- 

- 웨어러블 디바이스는 사용자의 하루 UV 흡수 량을 수집한다.
- 웨어러블 디바이스는 오전 0시 일 경우 UV 데이터를 초기화한다.
- 램프 컨트롤러는 웨어러블 디바이스를 착용한 사람을 감지하여 UV 등의 동작 여부를 결정한다.
- 램프 컨트롤러는 사용자의 생활 패턴 분석 결과를 기반으로 UV 등의 방사 시각을 결정한다.
- 램프 컨트롤러는 사용자의 생활 패턴을 내부 DB에 저장한다.
- 램프 컨트롤러는 웨어러블 디바이스의 UV의 하루 총 측정 량을 통해 UV 등의 방사 세기를 결정한다.
- 램프 컨트롤러는 웨어러블 디바이스의 UV 측정 량이 사람의 하루 권장량 미만일 경우에만 UV 등을 동작한다.


----
5. 비기능적 요구사항
---

- 웨어러블 디바이스는 탈 부착이 쉽고 가벼워야 한다.
- UV 등은 UVB만을 방사한다.
- 램프 세트(램프 컨트롤러, UV 등, 일반 등)는 단일 사용자에게만 UVB를 방사하기 위해 화장실에 설치한다.
- 웨어러블 디바이스는 방수 기능을 가지고 있어야 한다.
- 웨어러블 디바이스는 배터리로 동작하며 18시간 이상 충전 없이 사용할 수 있어야 한다.
- UV 등이 동작 시에는 일반 등도 같이 동작한다.
- UVB 방사 량이 사람의 UVB 하루 권장 량을 초과하지 않도록 한다.
- 폭포수 모델 개발 방법론을 사용하여 제품을 구현한다.
- 웨어러블 디바이스와 램프 컨트롤러는 적외선을 통해서 통신한다.
- 램프 컨트롤러를 통해서 저장된 생활 패턴은 RSA 방식으로 암호화하여 외부에 유출되지 않도록 한다.
- 햇빛 알레르기를 가지고 있는 사람에게는 본 제품의 사용을 제한한다.


----
6. 해결방안
---
 - 웨어러블 디바이스는 언제나 착용할 수 있고 가벼우며 UV 측정에 지장이 없는 손목에 착용하는 스마트 밴드 형태를 선정한다.
 - 단일 인원에게만 UVB 방사를 하기 위해 UV 방사 공간은 화장실로 한정한다.
 -  화장실에 들어온 사용자를 인식하기 위해서 화장실이라는 반경이 넓지 않은 소 공간, 통신 세기가 강하지 않아 벽 밖에 사용자는 인식하지 않는 적외선 통신을 사용한다.
 - 램프 컨트롤러는 사용자의 하루 동안의 화장실 사용 시각과 UV 측정 량 정보를 저장하여 생활 패턴을 분석한다.
 - UV 총 조사량의 산출 방법은 (UV 총 조사량) = (UV지수) * (조사받은 시간)으로 선정한다.

| 단계 | 지수 | 대책         |
| :------------ | :-----------: | -----------------------: |
| 낮음           | ~2           | 안전. 따로 대비하지않아도 무방|
| 보통           | 3~5           | 모자 선글라스 사용권장|
| 높음           | 6~7          | 1-2시간에 피부화상. 긴소매옷과 양산, 자외선 차단제 권장|
| 매우 높음           | 8~10           | 1시간 내로 피부화상. 한낮에는 외출자제 권장| 
| 위험           | 11+           | 수십분 정도로 피부화상. 가능한 실내활동.|


----
7. 기존 사례 및 특허
---
####**사례**

*  ‘**Sun Lamp**’라는 등(Light)을 통해 치료, 즉 비타민 D3의 합성을 목적으로 혹은 체내에 부족한UV를 보충 시켜 줄 수 있는 제품들이 상용화 된 제품이 있다.


####**특허**

* **자외선 방출 장치**  : 인버터를 통한 입력 전원의 조절로 자외선B 램프의 세기를 조절하여 최소한의 부작용으로 체내에서의 충분한 비타민D 합성이 일어날 수 있도록, 합성을 위한 적절한 시간인 10~15분 동안 자외선을 조사받을 수 있도록 하며, 최근 실내 활동의 증가로 인해 충분한 햇빛을 받지 못하는 현대인들에게 발생되는 비타민D 결핍현상을 감소시켜 건강을 증진 시키며, 생활수준을 높이는데 효과가 있다.

* **자외선 측정기** : 개인용 자외선 측정기에 관한 것이다. 인체 피부에 화상을 유발시키는 파장 280 ~ 320㎚의 자외선 B(UV-B)를 측정하는 제1의 센서 또는/및 인체 피부를 검게 태우는 파장 310 ~ 400㎚의 자외선 A(UV-A)를 측정하는 제2의 센서를 독립적으로 구비한 감지부와 상기 자외선 감지부에서 측정한 자외선의 세기를 자외선 지수(UV Index)로 표시하고, 자외선 차단지수(SPF 또는 PFA)를 계산하여 표시하고, 자외선 노출 가능시간을 표시하는 표시부와 상기 표시부에 표시되는 값을 계산하는 계산부와 상기 계산부에서 계산하고 표시부에 표시된 시간을 초과하기 전 자외선에 노출되는 경우 경고음을 내는 경고부를 포함한다.

* **자외선과 형광등 변환**  : 광촉매필터가 입혀진 자외선 램프를 형광등과 함께 설치하여 공기중의 각종 오염물질 및 세균 등을 살균 처리함과 함께 깨끗한 공기를 순환시킬 수 있도록 한 살균 및 향균 기능을 갖는 형광등 장치이다.