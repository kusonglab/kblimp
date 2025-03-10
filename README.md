# KBLiMP
* Paper: [](https://www.kci.go.kr/kciportal/ci/sereArticleSearch/ciSereArtiView.kci?sereArticleSearchBean.artiId=ART003173761)
* Authors: [Park Eunah](https://github.com/eparkatgithub), [Song Sanghoun](http://corpus.mireene.com/)
* Contact: dmsdk1993@korea.ac.kr

## 개요
* Hate speech
  * Verbal or non-verbal expressions that propagate or promote prejudice or discrimination against minorities (groups with common identity who have relatively diminished political and social power), or denigrate, insult, or threaten individuals or groups based on their attributes as minorities, or incites discrimination, hostility, or violence against them (Hong, 2018)
* Context-dependent hate speech
  * Hate speech interpreted as hateful through contextual factors rather than explicit content alone
  * In other words, without context, the statement itself may appear neutral or even positive in interpretation
  * Examples
    |Context|Comment|Hate|
    |:---|:---|:---:|
    |여성 고용이 미흡해 정부가 불이익을 준 기업의 이름이 공개되었다.<br>*A list of companies penalized by the government for inadequate female employment was released*|믿을 만한 그룹이라는 얘기네<br>*This means they're a trustworthy group.*|1|
    |직원에게 높은 수준의 복지를 제공한 기업의 이름이 공개되었다.<br>*A list of companies that provide high-level welfare benefits to employees was released.*|믿을 만한 그룹이라는 얘기네<br>*This means they're a trustworthy group.*|0|

## 데이터 설명명
* Source: [Dcinside Real-time Best Gallery](https://gall.dcinside.com/board/lists/?id=dcbest)
* Period: 2024/06/02-23
* Size
  |Total|Type 1|Type 2|Type 3|
  |:---:|:---:|:---:|:---:|
  |2,005|539|539|927|
* Types and examples
  <table>
    <thead>
      <tr>
        <th></th>
        <th>Context</th>
        <th>Comment</th>
        <th>Hate</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <th rowspan="2">Type 1</th>
        <td>Actually written context A</td>
        <td>Actually written comment C</td>
        <td rowspan="2">1</td>
      </tr>
      <tr>
        <td>광주광역시의 맛있는 음식 다섯 가지를 소개했다.<br><i>Introduced five delicious foods from Gwangju Metropolitan City.</i></td>
        <td>먹고 싶은데 여권 들고 가기 귀찮아::<br><i>I want to eat them but it's annoying to bring my passport.</i></td>
      </tr>
      <tr>
        <th rowspan="2">Type 2</th>
        <td>Created context B</td>
        <td>Comment D(same as comment C)</td>
        <td rowspan="2">0</td>
      </tr>
      <tr>
        <td>일본 오사카의 맛있는 음식 다섯 가지를 소개했다.<br><i>Introduced five delicious foods from Osaka, Japan.</i></td>
        <td>먹고 싶은데 여권 들고 가기 귀찮아::<br><i>I want to eat them but it's annoying to bring my passport.</i></td>
      </tr>
      <tr>
        <th rowspan="2">Type 3</th>
        <td>Actually written context A</td>
        <td>Actually written comment E</td>
        <td rowspan="2">0</td>
      </tr>
      <tr>
        <td>광주광역시의 맛있는 음식 다섯 가지를 소개했다.<br><i>Introduced five delicious foods from Gwangju Metropolitan City.</i></td>
        <td>역시 광주다<br><i>That's Gwangju for you.</i></td>
      </tr>
    </tbody>
  </table>
* Columns
  <table>
    <thead>
      <tr>
        <th>Column</th>
        <th>Description</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <th>index</th>
        <td>Data index</td>
      </tr>
      <tr>
        <th>set</th>
        <td>Post index</td>
      </tr>
      <tr>
        <th>type</th>
        <td>Type number (1~3 labeling)</td>
      </tr>
      <tr>
        <th>date</th>
        <td>The date the DC Inside post was written</td>
      </tr>
      <tr>
        <th>link</th>
        <td>The link to the DC Inside post</td>
      </tr>
      <tr>
        <th>title</th>
        <td>The title of the DC Inside post</td>
      </tr>
      <tr>
        <th>context</th>
        <td>Summary of the DC Inside post content / Created context</td>
      </tr>
      <tr>
        <th>comment</th>
        <td>Comments collected from DC Inside</td>
      </tr>
      <tr>
        <th>hate speech</th>
        <td>Whether it is hate speech (0 or 1 labeling)</td>
      </tr>
      <tr>
        <th>gender</th>
        <td>Target: gender (0 or 1 labeling)</td>
      </tr>
      <tr>
        <th>disability</th>
        <td>Target: disability (0 or 1 labeling)</td>
      </tr>
      <tr>
        <th>race/nation</th>
        <td>Target: race/nation (0 or 1 labeling)</td>
      </tr>
      <tr>
        <th>region</th>
        <td>Target: region (0 or 1 labeling)</td>
      </tr>
      <tr>
        <th>age</th>
        <td>Target: age (0 or 1 labeling)</td>
      </tr>
      <tr>
        <th>note</th>
        <td>Ikiyano style (-no)</td>
      </tr>
    </tbody>
  </table>

## Reference
Hong, S. (2018). [*When Words Hurt*](https://scholarworks.sookmyung.ac.kr/handle/2020.sw.sookmyung/20524). Across.

## Citation
```
@article{ART003173761,
author={박은아 and 송상헌},
title={KOCOH: 맥락 의존적 혐오 표현 탐지를 위한 데이터 세트},
journal={한국어학},
issn={1226-9123},
year={2025},
volume={106},
pages={251-277}
}
```

## License
