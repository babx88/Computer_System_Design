SUN을 JAVA 프로젝트
=================
**목차**:

[TOC]

----
1. 조원
---

10조 SUN을 JAVA
조원: 유현상(yoo2616), 김호연(guymode), 황인철(babx88)

----
2. 필요성
---

내용 작성

----
3. 개요
---
하루 동안의 사용자의 UV 노출정도를 측정하여 사용자가 집에서 생활을 할 때, 사용자의 부족한 UV양을 분석하여 사용자에게 충분한 UV양을 줄 수 있도록 UV등의 기능과 일반 등의 기능을 동시에 가지는 등을 개발한다.


----
4. 기능적 요구사항
---

- 웨어러블 디바이스를 착용한 사람을 감지하여 램프 컨트롤러가 자외선 램프의 동작 여부를 결정한다.
- 사용자의 생활 패턴 분석 결과를 기반으로 자외선 램프의 UV의 세기와 방사 시각을 결정한다.
- 웨어러블 디바이스는 자외선의 하루 총 조사량을 가지고 있어야 한다.
- 웨어러블 디바이스는 현재의 시간을 알 수 있어야 한다.
- 자외선 램프가 동작 시에는 일반 등도 같이 동작한다.
- 자외선 측정량이 사람의 하루 허용 범위를 미만일 경우에만 자외선 램프를 동작한다.


----
5. 비기능적 요구사항
---

- 웨어러블 디바이스는 탈부착이 쉽고 가벼워야 한다.
- 웨어러블 디바이스는 화장실이라는 특정 공간에서 사용해야 하기 때문에 방수 기능을 가지고 있어야 한다.
- 자외선 방사량이 사람의 UVB 하루 권장 기준치의 오차 범위 20%를 넘지 않도록 해야 한다.
- 사람들이 다수일 경우에는 한사람(특정사용자)에게만 부족한 UV를 줄 수 있도록 한정할 수 있어야 한다.
- 폭포수 모델 개발 방법론을 사용하여 제품을 구현한다.
- 웨어러블 디바이스와 램프 컨트롤러는 적외선을 통해서 통신한다.
- 램프 컨트롤러와 물체 인식 센서 간 통신은 MQTT 통신 방법을 활용한다.
- 램프 컨트롤러를 통해서 저장된 생활 패턴은 RSA 방식으로 암호화하여 외부에 유출되지 않도록 한다.
- 햇빛 알러지를 가지고 있는 사람에게는 사용을 제한한다.


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
7. 기존 사례
---

내용 작성

