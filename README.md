## KoWordSpacing

- Korean Word Spacing with bidirectional LSTM and Linear CRF. 


![](lstm.png)

### Requirement(R package) 

- `tensorflow`
- `hashmap`
- `wordVectors`
- `caret`
- `stringr`
- `stringi`
- `data.table`
- `reshape2`


- Detail was dicussed on [this blog link(Korean)](http://freesearch.pe.kr/archives/4617).

### Request Model Results with REST API

```
> library(reticulate)
> requests <- import('requests')

> requests$put('http://35.201.156.140:8080/spacing', 
      data=list(sent="나머지인생을설탕물이나팔면서보내고싶습니까,아니면세상을바꿔놓을기회를갖고싶습니까?"))$json() 
$sent
[1] "나머지 인생을 설탕물이나 팔면서 보내고 싶습니까, 아니면 세상을 바꿔놓을 기회를 갖고 싶습니까? "

```




