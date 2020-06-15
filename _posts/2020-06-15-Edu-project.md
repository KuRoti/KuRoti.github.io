---

title: "Edu_project"
subtitle : "Aiducation"
date: 2020-06-15 10:26:28 -0400
categories: Edu_project
layout: post

---

# Education-Project

졸업프로젝트로 진행한 교육프로젝트입니다. 

마음, 두뇌, 교육 교과목에서부터 제안했던 AI로 지식의 망각을 예측해 실제 학습률에 최대한 가깝게 교과과정을 관리하는 체계를 프로젝트의 주제로 선정했습니다.

<style>.embed-container { position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; } .embed-container iframe, .embed-container object, .embed-container embed { position: absolute; top: 0; left: 0; width: 100%; height: 100%; }</style><div class='embed-container'><iframe src='https://www.youtube.com/embed//TqlwWsZdM5I' frameborder='0' allowfullscreen></iframe></div>

발표 영상입니다. 

pyQG Gui로 구현하였고, 각 사용자별 online-learning에 사용될 파라미터들은 json으로 저장하는 방식으로 구현했습니다. 아직 gui를 다듬는 중이라 추후 github에 업로드할 계획입니다.

아직 제가 생각했던대로 NLP의 semantic embedding과 같은 기능을 넣지 못해 추후 이와 관련된 연구를 진행하고 싶습니다. 인지과학에서는 A->B라는 사전지식이 있을 때 A'->C로의 새로운 정보의 입력에 간섭을 일으킨다는 것을 확인하였고, 저는 이 A와 A' 의 유사도를 개념의 semantic한 거리로 표상하고 B와 C 사이의 semantic 거리를 변수로 넣어 기억 체득의 효율을 예측하는 연구를 진행해보고자 합니다. 장기적으로는 duolingo의 연구가 ACT-R 인지모델에 기반한 분석을 제시했던 것처럼, 제가 개발 중인 해윰 모델의 기억 인출 모델을 기반으로 HLR을 수행하는 프로젝트를 진행하는 것이 목표입니다.

제가 진행하는 개발/연구 외에도, 교육계에서 AI 관련 혁신이 활발하게 일어나 청소년들이 양질의 교육 서비스를 쉽게 접할 수 있는 환경이 구축되길 기원합니다. 

reference

Settles, B., & Meeder, B. (2016, August). A trainable spaced repetition model for language learning. In *Proceedings of the 54th annual meeting of the association for computational linguistics (volume 1: long papers)* (pp. 1848-1858).

Mihaylov, T., Clark, P., Khot, T., & Sabharwal, A. (2018). Can a Suit of Armor Conduct Electricity? A New Dataset for Open Book Question Answering. EMNLP.