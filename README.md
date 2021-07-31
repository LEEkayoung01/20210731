# 20210731

1. Greedy Algorithm : 탐욕적인 알고리즘
   : 미래를 내다보지 않고 당장 눈 앞에 있는 것 중 가장 좋은 것을 택함.
   
   1) 장점: 구현하기 간단하고 빠름
      단점: 최적의 답이라 보장할 수 없음
      쓰임: 다른 방식이 너무 느릴 때, 꼭 최적의 답이 필요한 게 아닐 때
      - greedy algorithm이 최적의 답을 구해주는 문제들도 있음.
   
   2) 최적 부분 구조 (Optimal structure): 부분 문제들의 최적의 답을 이용해서 전체 문제의 최적의 답을 구할 수 있음
      탐욕적 선택 속성 (Greedy choice propertyy): 각 단계에서 탐욕스러운 선택을 하는 것이 최종 답을 구하기 위한 최적의 선택
      
#1 500원, 50원, 100원 10원: 최대한 적은 돈을 사용해서 거슬러 주기

- 100원, 70원, 10원 이라면?


def course_selection(course_dict):
  	# 끝나는 시간 빠른 순으로 정렬
  	sorted_dict = sorted(course_dict.items(), key=lambda x: (x[1], x[0]))
  	# 시간표 리스트
  	time_table = list()
  	# 전 수업이 끝나는 시간
  	finish_time = 0

  	for key, val in sorted_dict.items():
		# 첫 수업
		if key == sorted_dict[0]:
  	    	finish_time = val[1]
			time_table.append(key : val)
		# 다음 강의의 시작 시간이 전 강의 끝나는 시간보다 늦으면 추가
		elif lec[0] > finish_time:
			finish_time = val[1]
			time_table.append(key : val)

	return time_table




 


