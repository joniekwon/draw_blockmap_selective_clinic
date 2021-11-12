# draw_blockmap_selective_clinic
코로나 선별 진료소 수와 행정구역 별 인구 수 데이터를 이용하여 블록맵 그리기

주소 좌표 변환 툴 다운로드: [Geocoder-Xr](http://www.gisdeveloper.co.kr/?p=4784)
***
* selective_clinic.py
  * 행정구역 이름 표준화 
  * 주소를 좌표값으로 변환할 때 데이터 100개 이상이 되면 속도가 너무 느려서 100개씩 분할하기 위한 코드
  * 변환된 좌표값을 이용하여 지도에 마커 찍기
  * 마커가 정위치에 안찍힘 확인필요 (제대로 찍히는것도 있고 아닌것도 있음)
***
* selective_blockmap.py
  *  블록맵 그리기위한 데이터 변환
  *  시도, 군구, 시도군구, 선별진료소 수(count), 인구대비 선별진료소 비율(MC_ratio)을 하나의 데이터프레임으로 병합
  *  블록맵 그리는 소스는 오픈소스 이용
  *  data_draw_korea에 미추홀구 데이터가 누락되어 dropna처리 --> 미추홀구가 이전 인천시 남구(남구를 모두 미추홀구로 통일해야함)
***
unique() 데이터를 비교해봤다면 인천광역시 남구와 미추홀구가 같다는 사실을 일찍 알아챘을지도 모르겠다는 생각이 듦..
