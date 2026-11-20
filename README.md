# 거래처 방문 · 주차 도우미

회사 내부용 거래처(병원·도매상) 방문, 주차 정보, 배송 코스 웹앱.

- 앱 주소: https://hi2han.github.io/client-app/
- `index.html`: 앱 본체
- `clients.json`: 회사 공용 거래처 목록. 직원 폰이 앱을 열 때마다 자동으로 받아감 (한 방향: 회사 → 직원)

## clients.json 규칙

- 저장소가 **공개**라 누구나 볼 수 있음. 담당자 이름 같은 민감 정보는 넣지 않음.
- `id`는 거래처마다 고정. 바꾸면 다른 거래처로 인식됨.
- 목록에서 빠진 거래처는 직원 폰에서도 지워짐. 직원이 직접 추가한 거래처는 유지됨.
- 직원 폰의 `내 메모`, `오늘 코스`는 업데이트로 지워지지 않음.

필드: `id, name, address, phone, category(hospital|wholesale|etc), dept, parking(easy|mid|hard|unk), building(yes|no|unk), freeTime, enforce[], parkingSpot, parkingNote, lat, lng`
