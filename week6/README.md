# Meta-Learning : Learning whit **Few Data** in Computer Vision
### Few-Shot Learning

  [Motivation]
  
  <img src="./img/An ideal scenario for a similarity measure in Few-Shot Learning.png">
  
  **Few shot learning**이란, *Few*한 데이터도 잘 분류할 수 있도록 하는 방법이다.
  하지만, *Few*한 데이터로 학습하는 것은 아니다. (적은 양의 레이블 데이터)
  
  
  <img src="./img/General overview of a Few-Shot Learning framework.png">
  
  - 기존의 지도학습(Supervised Learning) :
    Training set을 학습하여 학습한 클래스 내의 테스트를 한다.    
  - Few-Shot Learning은? :
    Training set을 학습하지만 테스트 시 학습한 클래스 이외의 클래스를 테스트한다. 
    대신, Few-Shot Learning은 Support set이 있으며 Support set의 클래스 개수와 샘플 수를 기준으로 k-way n-shot 이라는 표현을 쓴다.
    
  [학습방법]
  
  Few shot learning의 기본 학습 방법은 **유사성을 학습**하는 것
  
  <img src="./img/Overview of how a Few-Shot model makes a prediction.png">  
  
  1. 모델 아키텍처 선택

      Few-shot learning 모델은 일반적으로 적은 양의 데이터에서 작동할 수 있는 강력한 모델로 구성됩니다. 
      대표적인 예로는 siamese networks, prototypical networks, MAML (Model-Agnostic Meta-Learning) 등이 있습니다.
      
  2. 데이터 준비
  
      Few-shot learning에서는 주어진 클래스에 대해 매우 적은 수의 레이블 데이터가 있으므로, 일반적으로 각 클래스에서 몇 개의 데이터만 선택합니다. 
      선택된 데이터를 이용하여 모델을 학습시키는 것이 목표입니다.
    
  3. 학습
  
     선택된 데이터를 이용하여 모델을 학습시킵니다. 모델은 선택된 데이터에서 학습한 후, 새로운 클래스에 대한 인식을 수행할 수 있습니다. 
     학습 단계에서는 데이터의 특성을 모델이 학습할 수 있도록 데이터를 전처리하고, 데이터 증강 기술을 사용하여 데이터 샘플의 수를 늘릴 수도 있습니다. 
    
  4. 평가
    
      모델을 평가하고 결과를 분석합니다. Few-shot learning에서는 일반적으로 모델의 성능이 중요합니다. 
      모델의 성능이 높을수록, 적은 수의 레이블 데이터만으로도 새로운 클래스의 인스턴스를 인식할 수 있습니다.
        

  [Meta Learning 에서의 Few-Shot Learning]
  
 
  일단 여기서 **Meta Learning** 이란? 기계 학습의 한 분야로, 다른 학습 작업들을 수행하면서 학습 알고리즘을 향상시키는 방법이다.
  즉, meta-learning은 학습 알고리즘 자체를 학습시키는 것이다.

  Meta-learning은 보통 새로운 작업을 수행할 때 적은 양의 데이터만 사용할 수 있을 때 유용하다.
  
  - Metric-based

      새로운 작업에 대해 유용한 특성을 추출하기 위해 **거리(metric) 함수**를 사용하는 방법이다. 
      모델은 일반적으로 각 클래스의 평균 벡터를 학습하고, 새로운 샘플과 기존 클래스 간의 거리를 계산하여 새로운 샘플을 인식합니다.
      
  - Model-based

      **모델의 초기 가중치**를 조정하여 새로운 작업에 적응할 수 있는 모델을 학습하는방법이다.
      이를 위해 보통 *MAML (Model-Agnostic Meta-Learning) 알고리즘*이 사용됩니다. 
      이 알고리즘은 초기 가중치를 조정하기 위해 작은 수의 gradient step을 사용합니다.
      
  - Optimization-based

      **목표 함수 (objective function)을 최적화**하여 새로운 작업을 수행하기 위한 최적화 알고리즘을 학습하는 방법이다. 
      이를 위해 Reptile 알고리즘이 사용되며, 이 알고리즘은 몇 번의 optimization step을 사용하여 모델을 초기화하고, 
      그 다음 몇 번의 작은 gradient step을 사용하여 모델을 새로운 작업에 적응시킵니다.
      
### Video Frame Interpolation      

### MetaVFI

### Super Resolution

### Few-Shot Image to Image Translation
 
### Few-Shot Image Generation

### etc.
