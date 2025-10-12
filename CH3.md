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
