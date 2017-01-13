---
title: Liquid의 변형
description: Liquid의 다른 버전의 설치에 대한 개요와 사용방법에 따라 Liquid가 어떻게 바뀔 수 있는지에 대해 설명합니다.
---

Liquid는 유연하며, 안전한 언어이고 다양한 환경에서 사용됩니다. Liquid는 [Shopify](https://www.shopify.com) 스토어에서 사용하기 위해 만들어 졌으며, 또한 [Jekyll](https://jekyllrb.com) 웹사이트들에서도 광범위하게 사용됩니다. 시간이 흐르면서 Shopify와 Jekyll은 각각 그들만의 객체, 태그 및 필터를 Liquid에 추가했습니다. 가장 유명한 Liquid 버전은 **Liquid**, **Shopify Liquid**, 그리고 **Jekyll Liquid**입니다.

이 사이트는 베타와 RC(release candidates)를 포함한 최신 버전의 **Liquid**를 문서화하고 있습니다 - 즉, Shopify와 Jekyll의 확장을 포함하지 않은 Liquid. 만약 Liquid 저장소를 다운받거나 [gem](https://rubygems.org/gems/liquid)으로 설치하면, 당신이 선택한 Liquid의 버전에 맞는 객체, 태그 및 필터에 접근할 수 있습니다.

## Shopify

Shopify는 항상 최신 버전의 Liquid를 기본으로 사용하지만, 스토어에서 사용하기 위한 많은 객체, 태그 및 필터가 추가되어 있습니다. 여기에는 스토어, 제품 및 고객 정보를 표현하기 위한 객체들과 스토어의 데이터를 표시하고 제품의 이미지와 같은 스토어의 자산을 조작하기 위한 필터들이 포함됩니다.

Liquid의 Shopify 버전은 [Shopify Help Center](https://help.shopify.com/themes/liquid)에 설명되어 있습니다. Shopify 버전의 Liquid를 사용하려면, [Shopify 무료 평가판을 시작](https://www.shopify.com/signup)하거나 [DropPen](http://droppen.org/)와 같은 샌드박스를 이용하세요.

## Jekyll

[Jekyll](https://jekyllrb.com)은 정적 사이트 생성기로, 컨텐츠와 템플릿을 합쳐서 웹사이트를 생성하는 명령줄 도구입니다. Jekyll은 템플릿 언어로 Liquid를 사용하며, 약간의 객체, 태그 및 필터를 추가했습니다. 여기에는 페이지의 컨텐츠를 표현하는 객체와 컨텐츠 스니펫을 포함하는 태그, 그리고 문자열과 URL을 조작하기 위한 필터가 포함됩니다.

또한 Jekyll은 Github 저장소에 컨텐츠를 푸시하여 결과 웹사이트를 게시할 수 있게 해주는 웹 호스팅 서비스인 [GitHub Pages](https://pages.github.com/)를 지원합니다. 이 웹사이트 역시 GitHub Pages를 사용하여 제작되었습니다.

Jekyll은 최신 버전의 liquid를 사용하지 않을 수 있습니다. 즉, 이 사이트에 설명된 태그나 필터가 Jekyll에서 동작하지 않을 수도 있습니다. Jekyll 프로젝트는 베타 버전이나 RC 버전 대신 안정된 Liquid 버전을 필요로 합니다. 사용중인 Liquid Jekyll의 버전을 확인하려면, [Jekyll's gem page](https://rubygems.org/gems/jekyll)의 **runtime dependencies** 섹션을 체크하세요.

[Jekyll 문서(한글)의 템플릿 섹션](http://jekyllrb-ko.github.io/docs/templates/)에 Jekyll의 Liquid 버전에 대한 설명이 있습니다. Jekyll의 Liquid 버전을 시험해보고 싶다면 Jekyll 프로젝트를 clone 하거나 gem으로 Jekyll을 설치하고 정적 사이트에서 Liquid를 테스트 할 수 있습니다.