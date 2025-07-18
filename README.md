# KBLiMP
* Paper: [KBLiMP: 언어모델은 한국어 통사 현상을 얼마나 이해하는가?](https://www.kci.go.kr/kciportal/ci/sereArticleSearch/ciSereArtiView.kci?sereArticleSearchBean.artiId=ART003175225)
* Authors: 송상헌/Sanghoun Song, 노강산/Kang San Noh, [박은아/Park Eunah](https://github.com/eparkatgithub), [이수빈/Lee Subin](https://github.com/subin0929), [이예빈/Lee Yebin](https://github.com/nqn4iwin), [조은비/Cho Eunbi](https://github.com/EunB2)

## 개요
* KBLiMP : Korean-specific Benchmark of Linguistic Minimal Pairs
  * Korean-specific : 
  * Minimal Pairs : 
  * Syntactic Evaluation : 

## 데이터
* Period: 2024/01/01-2024/01/23
* Size: 100 sentences * 4 conditions * 10 phenomena = 4,000 sentences
* Dataset Construction
  | Type 	| Index 	| Var1 	| Var2 	| Sentence 	| Acceptability 	|
  |------	|-------	|------	|------	|----------	|---------------	|
  |관계절보조사|1|관계절+|주제표지+|그는 정부는 요구하는 활동을 설명했다.|0|
  |관계절보조사|2|관계절+|주제표지-|그는 정부가 요구하는 활동을 설명했다.|1|
  |관계절보조사|3|관계절-|주제표지+|정부는 활동을 요구했다.|1|
  |관계절보조사|4|관계절-|주제표지-|정부가 활동을 요구했다.|1|
  |격중출(주어)|1|소유-|격중출-|꽃의 장미가 예쁘다.|0|
  |격중출(주어)|2|소유-|격중출+|꽃이 장미가 예쁘다.|1|
  |격중출(주어)|3|소유+|격중출-|꽃의 색깔이 예쁘다.|1|
  |격중출(주어)|4|소유+|격중출+|꽃이 색깔이 예쁘다.|1|
  |격중출(목적어)|1|소유-|격중출-|현우가 토끼의 산토끼를 잡았다.|0|
  |격중출(목적어)|2|소유-|격중출+|현우가 토끼를 산토끼를 잡았다.|1|
  |격중출(목적어)|3|소유+|격중출-|현우가 토끼의 귀를 잡았다.|1|
  |격중출(목적어)|4|소유+|격중출+|현우가 토끼를 귀를 잡았다.|1|
  |내포절시제|1|세계지식+|과거+|수진이는 베이징이 중국의 수도였다고 말했다.|0|
  |내포절시제|2|세계지식+|과거-|수진이는 베이징이 중국의 수도라고 말했다.|1|
  |내포절시제|3|세계지식-|과거+|수진이는 베이징에 가고 싶었다고 말했다.|1|
  |내포절시제|4|세계지식-|과거-|수진이는 베이징에 가고 싶다고 말했다.|1|
  |내핵관계절(주어)|1|주절주어+|HUMAN+|민지가 달리던 것이 멈추었다.|0|
  |내핵관계절(주어)|2|주절주어+|HUMAN-|나뭇잎이 떨어지던 것이 멈추었다.|1|
  |내핵관계절(주어)|3|주절주어-|HUMAN+|민준이는 민지가 달리던 것을 붙잡았다.|1|
  |내핵관계절(주어)|4|주절주어-|HUMAN-|민준이는 나뭇잎이 떨어지던 것을 붙잡았다.|1|
  |내핵관계절(목적어)|1|주절주어+|HUMAN+|트럭이 소녀를 세게 친 것이 경찰에 의해 병원으로 옮겨졌다.|0|
  |내핵관계절(목적어)|2|주절주어+|HUMAN-|트럭이 중앙분리대를 세게 받은 것이 경찰에 의해 신속히 복구되었다.|1|
  |내핵관계절(목적어)|3|주절주어-|HUMAN+|경찰은 트럭이 소녀를 친 것을 병원으로 옮겼다.|1|
  |내핵관계절(목적어)|4|주절주어-|HUMAN-|경찰은 트럭이 중앙분리대를 세게 받은 것을 신속히 복구했다.|1|
  |복합명사구제약|1|섬+|내포절공백+|새우를 현우는 의사에게 민지가 먹었다는 사실을 이야기했니?|0|
  |복합명사구제약|2|섬+|내포절공백-|현우는 의사에게 민지가 새우를 먹었다는 사실을 이야기했니?|1|
  |복합명사구제약|3|섬-|내포절공백+|새우를 현우는 의사에게 민지가 먹었다고 이야기했니?|1|
  |복합명사구제약|4|섬-|내포절공백-|현우는 의사에게 민지가 새우를 먹었다고 이야기했니?|1|
  |비교구문|1|정도성-|비교표지-|민준이는 민지보다 먹었다.|0|
  |비교구문|2|정도성-|비교표지+|민준이는 민지보다 더 먹었다.|1|
  |비교구문|3|정도성+|비교표지-|민준이는 민지보다 예쁘다.|1|
  |비교구문|4|정도성+|비교표지+|민준이는 민지보다 더 예쁘다.|1|
  |'설득하다' 구문|1|전위-|여격-|민지가 법대에 가도록 선생님께서 민지에게 설득하셨다.|0|
  |'설득하다' 구문|2|전위-|여격+|민지가 법대에 가도록 선생님께서 민지에게 설득하셨다.|1|
  |'설득하다' 구문|3|전위+|여격-|민지가 법대에 가도록 선생님께서 민지에게 설득하셨다.|1|
  |'설득하다' 구문|4|전위+|여격+|민지가 법대에 가도록 선생님께서 민지에게 설득하셨다.|1|
  |수여구문|1|수령수혜자-|주다-|현우는 민지에게 그림을 그렸다.|0|
  |수여구문|2|수령수혜자+|주다-|현우는 민지를 위해 그림을 그렸다.|1|
  |수여구문|3|수령수혜자-|주다+|현우는 민지에게 그림을 그려 주었다.|1|
  |수여구문|4|수령수혜자+|주다+|현우는 민지를 위해 그림을 그려 주었다.|1|

## Reference

## Citation

## License
