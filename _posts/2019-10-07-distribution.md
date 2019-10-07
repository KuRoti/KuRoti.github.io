---
title: "확률분포"
date: 2019-10-08 12:25:28 -0400
categories: math
tags : probability
layout: post
---

# Probability Distribution

\{toc:}

이전 포스팅에서 random variable과 PMF에 대해 정리했습니다. 이번 포스팅에서는 많이 쓰이는 Bernoulli distribution, Binomial distribution과 같은 확률 분포에 대해 다루겠습니다. 

확률 분포 X에 대해  random variable A가 확률 분포 X를 따른다는 것은 $$A\sim X(parameter)$$로 표기하며, X에 매개변수를 대입하면(ex. p,n) A가 특정 값을 가질 확률을 계산할 수 있다.

가장 기본이 되는 확률분포는 베르누이 분포로, 이 블로그에서 다루는 범위의 모든 확률분포는 베르누이 분포로 환원가능할정도로 기초적인 분포이다.

## Bernoulli distribution

### Definition

확률변수 $$X$$가 parameter $$p$$로 베르누이 분포를 따른다는 것은

- $$X_S=\{0,1\}$$ 이고 $$P(X=1)=p, P(X=0)=1-p$$를 만족한다.
- $$ X\sim Bern(p) $$로 표기한다.
- 가능한 상태가 두 개뿐인 모든 확률변수는 베르누이 분포를 따른다.
- '1'은 성공으로 간주, '0'은 실패로 간주한다.

이 정의에 대한 해석을 해보자면, 베르누이 분포는 단순히 확률변수가 0이나 1인 값을 가질 때 적용되는 확률분포라는 것이다. 딱 한 번의 시행을 거칠 때, 그 시행이 성공하거나 실패할 단 두 가지 경우밖에 존재하지 않으며, 시행의 성공 확률은 $$ p $$일때 우리는 베르누이 분포를 적용할 수 있다.

가장 단순한 만큼, 이 베르누이 분포에서 우리가 배울 여러 확률 분포 함수를 유도할 수 있으며, 확률과 관련된 많은 모델들을 접할 때 많이 듣게 될 용어이기도 하다.

### Indicator Random Variable

한편 베르누이 분포를 논할 때 Indicator Random Variable의 개념을 같이 짚고 넘어가는 것이 좋은데, 이 개념은 많이 언급되면서도 쉬운 개념이다.

사건 $$A$$의 *indicater random variable*은 $$I_A$$로 표기되며, $$A$$가 성공할 때는 1의 값을, 실패할 때는 0의 값을 갖는 함수이다.

수식으로 나타내면 $$I_A(s)=\begin{cases}\ 1\ \ \ s\in A\\\ 0\ \ \ s\notin A\end{cases}$$ 로 표기되며, $$p=P(A)$$일 때 $$ I_A\sim Bern(p) $$를 만족한다. 

이 수식에서는 엄밀한 정의를 따라 사건 A 내의 시행 s에 대해 표기했지만, 통상적으로 $$I(A)$$로 표기한 경우에도 $$A$$사건이 발생하면 1의 값, 발생하지 않으면 0의 값을 갖는 확률변수입니다. 	

##  Binomial distribution

베르누이 분포가 0과 1값만을 갖는 확률변수에 대한 분포였다면, Binomial 분포는 베르누이 분포를 따르는 시행을 n번, 서로 독립적으로 시행했을 때의 확률분포를 설명하는 함수입니다.

n번의 독립적인 베르누이 시행(성공 확률 $$p$$)을 행했을 때 성공하는 횟수를 $$X$$라고 하면, $$X$$의 분포는 binomial distribution으로 불리며, $$X\sim Bin(n,p)$$로 표기됩니다.

$$X\sim Bin(n,p)$$일 때 $$X$$의 PMF는 $$P(X=k)=\begin{pmatrix}n\\k\end{pmatrix}p^k(1-p)^{n-k}$$로 계산할 수 있습니다. 성공 확률이 $$p$$인 시행이 k번 성공하고, 총 n번의 시행 중에 이 k개의 성공시행을 분배하는 식으로 이해하면 이해가 쉽습니다.

### Hypergeometric distribution

Hypergeometric 분포는 생소한 이름인데요, 성공과 실패의 횟수가 한정되어 있고, replacement가 없는 상황에서 (예 : 제비를 뽑은 뒤 다시 집어넣지 않는 제비뽑기) n번의 시행에 대해 성공 시행의 수가 따르는 분포입니다.

$$X$$가 $$n$$번의 시행 중 성공 시행의 횟수를 나타내는 ramdom variable이고, $$w$$개의 성공할 경우의 수, $$b$$개의 실패할 경우의 수 아래 $$n$$번의 시행을 하고, 각 시행을 진행하고 난 후 시행 전의 상태로 돌아가지 않는(ex. 상자에서 공을 뽑고 다시 집어넣지 않는) 경우에, $$X$$의 분포는 Hypergeometrix distribution이라고 부르며, $$X\sim HGeom(w,b,n)$$으로 표기합니다.

$$X$$가 위와 같은 분포를 따를 때, $$X$$의 PMF는 $$P(X=k)=\frac{\begin{pmatrix}w\\k\end{pmatrix}\begin{pmatrix}b\\n-k\end{pmatrix}}{\begin{pmatrix}w+b\\n\end{pmatrix}}$$로 표기합니다.

고등학교 수준에서 나오는 상당수의 확률 문제나, 대체시행이 아닌 경우의 많은 확률 시행은 Hypergeometric 분포를 따르는 경우가 많으며, HGeom의 확률 질량 함수 공식은 기억해두면 유용하게 쓰입니다.
