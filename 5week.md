## 5주차 1차시 강의요약

### State의 개념, State Space Equation

#### State Variables

<img width="860" height="646" alt="image" src="https://github.com/user-attachments/assets/0bba7573-dfba-4955-97cb-bc6ecbf15587" />

이제까지는 시스템의 수식화에 집중했다면 지금부터는 State를 정의해서 시스템 안의 요소들을
중심으로 문제들을 풀자.  

이 State는 input에서 영향을 받으며 State끼리도 영향을 받을 수 있다.
Output은 input과 State의 조합으로 만들어진다.

<img width="767" height="607" alt="image" src="https://github.com/user-attachments/assets/80282a1c-39c8-4a5a-9800-e357188bb4a5" />

했던 것들로 예시를 들면 지금까지는 수식으로 만들고 풀면 끝이었으나,  
과정에 의미를 부여해 state 2개를 정의한다. 2차 미분 방정식이기 때문에 2개로 정의한다.
결국 미지수가 2개가 된 것과 마찬가지이다.

<img width="656" height="241" alt="image" src="https://github.com/user-attachments/assets/1803d001-d5e2-4b67-b68b-521fc9150aa3" />

이것을 보고 State Variable model의 효과는 2차 미분방정식 1개를 1차 미분방정식 2개를 바꿈으로써  
더 쉽게 풀 수 있다. 즉 효율적이다.

<img width="767" height="328" alt="image" src="https://github.com/user-attachments/assets/7470384f-2dd4-4fca-8c83-d68e3a562297" />

State는 정하기 나름인데, 두 개를 정의할 때 항등식이 되는 것은 피해야 하며,  
단순 상수배도 피해야한다. 즉, 독립적으로 정해야한다.

<img width="686" height="499" alt="image" src="https://github.com/user-attachments/assets/3b9b2719-cde9-45af-b4dd-70ea4d882309" />

왜 State를 만들어야 하는가? Ans :  
<img width="826" height="109" alt="image" src="https://github.com/user-attachments/assets/284513c1-f2a9-4476-bf30-e180cf761a15" />

이것을 정의하고 푼다고 했을 때 푼다고 하자.  
<img width="710" height="445" alt="image" src="https://github.com/user-attachments/assets/57f1dace-33af-48a2-893c-254d4b7431d5" />  

왼쪽 부분은 Φ(t)에 의해 바뀐 결과물, 오른쪽은 u(t)에 의해 바뀐 결과물 따라서 각 부분은 물리적인 의미를 갖게 된다.

다차 미분방정식에서의 State는 당연히 여러개이다. ex) 3차라면 3개가 될 것이다.  
<img width="681" height="649" alt="image" src="https://github.com/user-attachments/assets/e40e9bfb-0f63-4255-9ff0-90a547786e38" />

두 개의 1차 미분방정식이던게 1개의 행렬 1차 미분 방정식으로 바꿀 수 있다. 즉,  
<img width="370" height="147" alt="image" src="https://github.com/user-attachments/assets/460a9352-5905-4c85-a826-b17c5a99411b" />

이 식은  
<img width="316" height="149" alt="image" src="https://github.com/user-attachments/assets/8d907d5f-062d-45aa-9f30-11160c69a43e" />  
이 행렬을 이끌어내기 위함이다.  

<img width="747" height="165" alt="image" src="https://github.com/user-attachments/assets/ed9ec82e-e8a7-4fb5-9bbf-1ad79af3827e" />  
첫번째 줄 식에서 2번째 줄 식으로 넘어갈 때, a=>A로 바뀌며 상수가 행렬이 된다.  

문제 예시) 2차 미분방정식 2개이므로 4차 미분 방정식이 만들어지는데 이를 State space equation
적용하면 쉽게 풀 수 있음
<img width="618" height="431" alt="image" src="https://github.com/user-attachments/assets/7d644a29-c180-4b59-b38f-9cf66ef32107" />  

이것들을 책에 있는 상수값을 이용한 뒤 행렬 매트랩 코드를 작성하면 아래처럼 출력이 된다.  
코드: ss (state space equation) 행렬 4개 넣어주면 그걸 시스템으로 만들어주는 매트랩코드.  
<img width="892" height="648" alt="image" src="https://github.com/user-attachments/assets/0f0e2cea-ff8c-4b35-8fff-2ce9505f8c98" />
