#CH3 과제

###P3.1 그림 P3.1에 스프링-질량-감쇠기 시스템이 주어져있다. (a) 적당한 상태변수를 설정하라. (b) 상태변수로 표현된 1차 미분방정식을 구하라. (c) 상태미분방정식을 구하라.  
F(t) = M(d^2y/dt) - b(dy/dt) -ky => M(dx_2(t)/dt) = bx_2(t) + kx_1(t) + F(t)  
(a) x_1(t) = y(t), x_2(t) = dy/dt  
(b) dx_2(t)/dt = (b/M)*x_2(t) + (k/M)*x_1(t) + (1/M)*F(t)  
    dx_1(t)/dt = x_2(t)  
(c) \vec{x'} = [0, 1; k/M, b/M]* \vec{x} + [0; 1/M] * \vec{F(t)}  
  \vec{y(t)} = [0, 1] * \vec{x}  

###P3.3 그리몌3.3과 같은 RLC회로가 주어졌다. 상태변수 x_1(t) = i_L(t), x_2(t) = v_c(t)로 설정하고 상태미분방정식을 구하라.

L*(di_L/dt) - v_c + v_2 - v_1 = 0  
i_L = i_R - C*(dv_c(t)/dt), v_R = v_2 - v_c = (i_R)*R => i_R = (v_2 - v_c)/R  
C*(dv_c(t)/dt) = i_R - i_L => dv_c(t)/dt = (v_2 - v_c)/(R*C) - i_L/C, di_c(t)/dt = (v_c + v_1 - v_2)  
답: \vec{x'} = [0, 1/L; -1/C, -1/RC] * \vec{x} + [1/L, -1/L; 0, 1/RC] * \vec{v}

###P3.5 그림 P3.5에 폐루프 제어시스템이 주어져있다. (a) 페루프 전달함수 T(s) = Y(s)/R(s)를 구하라. (b) 상태변수 모델을 구하고 위상변수형 블록선도를 작성하라.  
(1 + (s+2)/{s * (s-3) * (s+8)] Y = (s+2)/{s * (s-3) * (s+8)} * R => Y/R = (s+2)/(s^3 + 5s^2 - 23s +2) = T(s)  
(a) T(s) = (s+2)/(s^3 + 5s^2 - 23s +2)  

T(s)의 분모와 분자에 Z(s)를 곱해주고 역라플라스변환을 하면 T(t) = (z' + 2z)/(z''' + 5z'' - 23z' + 2z)가 되므로  
y(t) = z'(t) + 2z(t), r(t) = z'''(t) + 5z''(t) -23z'(t) + 2z(t)가 되므로  
\vec{x} = [x_1; x_2; x_3] = [z; x'_1; x'_2] = [z; z'; z'']이고  
x'_3 = z'''(t) = -2z + 23z' - 5z'' + r(t) = -2x_1(t) + 23x_2(t) - 5x_3(t) + r(t)  
y(t) = x_2(t) + 2x_1(t)이므로  
(b) \vec{x'} = [0, 1, 0; 0, 0, 1; -2, 23, -5] * \vec{x} + [0; 0; 1] * \vec{r}  
\vec{y} = [2, 1, 0] * \vec{x}가 된다.  

###P3.12 전달함수가 Y(s)/R(s) = T(s) = 8*(s+5)/(s^3 + 12s^2 + 44s + 48)인 시스템에서 (a) 상태공간모델을 구하라. (b) 상태천이행렬 Φ(t) 를 구하라.  
a문제를 실행시키는 코드이며  

실행결과는 이와 같으므로  

(a)의 답은 \vec{x'} = [0, 1, 0; 0, 0, 1; -48 -44 -12] * \vec{x} + [0;0;1] * \vec{r},  
y(t) = [5, 8, 0] * \vec{x} 이다.  

상태천이를 구하는 코드는 이와 같으며  

실행결과는 이와 같다.  
(b)  


###P3.17 다음과 같은 상태변수 방정식으로 표현된 시스템이 있다.  \vec{x'} = [1, 1, 1; 4, 3, 0; -2, 1, 10] * \vec{x} + [0; 0; 4] * \vec{u(t)}  
\vec{y} = [1, 0, 0] * \vec{x}, G(s) = Y(s) / U(s)를 구하라.  
이를 실행시키는 코드는 이와 같으며  
<img align="left" width="100" height="100" src="https://postfiles.pstatic.net/MjAyNTEwMTJfMTY4/MDAxNzYwMjU3MDI5NDUz.qgL_koPzS0uKBfIt9bKYjuW9ADr3RkbgGCVwdvaip9wg.ET3alscUPJaDvSfXoXK6zbbiGbnnFrXSLEtvFvum_rYg.PNG/image.png?type=w773">
