# Machine_Learning
  1. 시계열 분석(예측)
    1) ARIMA(Autoregressive Integrated Moving Average)
       : AR과 MA를 섞은 ARMA에 Integrated 라는 개념을 추가한 모델. ARMA 모델 역시 불규칙적 시계역 데이터를 제대로 예측하지 못하는 한계가 있기          때문에 관측치 사이의 차분(Difference) 즉, 과거의 데이터가 지니고 있던 추세까지 반영... 너무 어렵다...
       
      - AR(Autoregression) : 자기 회귀 모델, 자기 자신의 과거를 사용하기 때문, 이전의 자신의 관측값 이후의 자신의 관측값에 영향을 준다는 
                             아이디어의 모형으로 RNN의 아이디어와 매우 유사
                             Xt = (Xt-1*w)+b+(et*u)
                             
      - MA(Moving Average) : 이동 평균 모델은 트렌드(평균 혹은 y값)가 변화하는 상황에 적합한 회귀 모델
                             AR 모델과 비교하면 Xt-1이 et-1로 변경. 이전 값을 이용해 새로운 상태를 추론하는 것이 아닌 이전 항에서의 오차 또                              는 변동 값을 이용하여 현재 항의 상태를 추론(주식에 보면 지표로 있음..)
                             Xt = (et-1*w)+b+(et*u)
                             
      - ARMA : 과거의 상태와 오차 값을 사용해 현재의 산태를 예측하는 모델. AR 모델과 MA 모델을 섞은 것
               Xt = (Xt-1*w11)+(et-1*w21)+b+(et*u) <- 가장 단순한 ARMA(1,1) 모형
               Xt = (Xt-1*w11)+(Xt-2*w12)+(et-1*w21)+(et-2*w22)+b+(et*u) <- ARMA(2,2) 모형
           
