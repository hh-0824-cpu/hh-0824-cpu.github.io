---
layout: page
title: "고딕 소설 비교"
permalink: /gothic/
---

# 고딕 소설 비교

<!-- Q1: 두 고딕 소설의 상위 30개 단어 비교 -->

<h2>Frankenstein vs. Dracula – 상위 30개 단어</h2>

<div style="display: flex; gap: 1em;">

<div style="flex: 1;">

<h3>Frankenstein (Shelley, 1818)</h3>

<div style="height: 600px;">
<canvas id="chart-frankenstein"></canvas>
</div>

</div>

<div style="flex: 1;">

<h3>Dracula (Stoker, 1897)</h3>

<div style="height: 600px;">
<canvas id="chart-dracula"></canvas>
</div>

</div>

</div>

## 보고서

### 추가한 불용어와 근거

NLTK 기본 불용어 목록 외에 `said`, `would`, `could`, `one`, `i`를 `data/stopwords-custom.txt`에 추가하였다.

- `said`: 등장인물의 대화를 표시하는 표현으로 매우 자주 등장하지만 작품의 주제나 인물을 직접적으로 설명하지는 않는다.
- `would`: 문장의 문법적 기능을 수행하는 조동사로, 작품의 특징을 보여주는 단어라고 보기 어렵다.
- `could`: 가능성이나 능력을 나타내는 조동사로 여러 상황에서 반복적으로 사용되어 분석에 큰 의미를 주지 않았다.
- `one`: 매우 일반적인 표현으로 다양한 맥락에서 사용되지만 작품의 인물이나 주제를 파악하는 데에는 큰 도움이 되지 않았다.
- `i`: 두 작품 모두 1인칭 화자의 시점이나 기록 형식이 자주 사용되기 때문에 높은 빈도로 등장하지만, 특정 인물이나 사건을 드러내기보다는 서술 방식의 영향을 크게 받는다고 판단하였다.

이 단어들은 두 작품 모두에서 높은 빈도로 등장했지만 작품의 핵심 주제나 인물보다는 문체와 서술 방식의 특징을 반영하는 경우가 많다고 생각하여 추가 불용어로 제거하였다.

### 두 작품의 단어 빈도가 들려주는 이야기

- **공통으로 도드라지는 단어**

  두 작품 모두에서 `man`, `night`, `saw` 같은 단어가 비교적 자주 등장하였다. 특히 `night`는 고딕 소설 특유의 어둡고 불안한 분위기를 보여 주며, `man`은 두 작품이 결국 초자연적 존재를 통해 인간과 인간성의 문제를 다루고 있음을 시사한다고 생각한다.

- **Frankenstein에서만 도드라지는 단어와 그 의미**

  Frankenstein에서는 `life`, `mind`, `father`, `eyes` 등의 단어가 눈에 띄었다. 이는 작품이 단순한 괴물 이야기가 아니라, 생명의 창조와 인간 존재의 의미, 그리고 창조자와 피조물의 관계를 탐구하는 이야기라는 점을 보여 준다고 생각한다.

- **Dracula에서만 도드라지는 단어와 그 의미**

  Dracula에서는 `mina`, `jonathan`, `lucy`, `helsing`, `count`와 같은 인물 이름이 두드러졌다. 이는 작품이 여러 인물의 기록과 증언을 통해 전개되며, 드라큘라라는 존재보다도 그를 둘러싼 인물들의 협력과 추적 과정에 큰 비중을 두고 있음을 보여 준다.

{% include chartjs.html %}
<script src="/assets/js/analysis.js"></script>
<script src="/assets/js/gothic.js"></script>