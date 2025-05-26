---
layout: default
description: >-
  엔에이치는 X-ray, 광학비전 검사 장비 및 자동화 솔루션을 제조하는 전문업체입니다. 
  로봇 기술과 결합한 혁신적인 검사·측정·분석·가공 장비를 공급합니다.
keywords: 
  - X-ray 검사 장비
  - xray 검사 장비
  - 엑스레이 검사 장비
  - 엑스 레이 검사 장비
  - X레이 검사 장비
  - X-RAY 검사 장비
  - 자동화 솔루션
  - 광학비전 검사
  - 로봇 자동화
  - 검사 장비 제조
  - 측정 장비
  - 분석 장비
image: /assets/images/hero-image.jpg
---

<div class="hero-section">
  <div class="hero-image">
    <img src="/assets/images/hero-image.jpg" alt="">
  </div>
  <div class="overlay"></div>
  <div class="hero-content">
    <h1>X-ray 및 광학비전 검사의<br>혁신적인 솔루션</h1>
    <div class="bottom-content">
      <p>엔에이치는 엑스레이, 광학간섭계 등의 광학기술을 응용한<br>검사·측정·분석·가공 장비를 제작 공급하는 전문업체입니다.<br>로봇 기술과 결합하여 공정 자동화에 혁신을 가져옵니다.</p>
      <div class="hero-buttons">
        <a href="/products/" class="btn btn-primary">제품 보기</a>
      </div>
    </div>
  </div>
</div>

<div class="main-content">
  <section class="products-preview">
    <h2>주요 제품</h2>
    <div class="product-cards">
      {% assign featured_product_slugs = "PRD5022,PRI5700,LVI600" | split: "," %}
      {% for slug in featured_product_slugs %}
        {% assign product = site.products | where: "title", slug | first %}
        {% unless product %}
          {% assign product = site.products | where_exp: "item", "item.url contains slug" | first %}
        {% endunless %}
        {% if product %}
          <div class="product-card">
            <div class="image-container">
              {% if product.images and product.images.size > 0 %}
                <img src="{{ product.images[0].src }}" alt="{{ product.images[0].alt | default: product.title }}">
              {% else %}
                <img src="/assets/images/product-placeholder.jpg" alt="{{ product.title }}">
              {% endif %}
            </div>
            <h3>{{ product.title }}</h3>
            <p>{{ product.description }}</p>
            <a href="{{ product.url }}" class="btn btn-secondary btn-sm">자세히 보기</a>
          </div>
        {% endif %}
      {% endfor %}
    </div>
  </section>
  <section class="contact-section">
    <h2>문의하기</h2>
    <div class="contact-flex-container">
      <p>제품이나 서비스에 대해 궁금하신 점이 있으시다면 언제든지 문의해 주세요.</p>
      <a href="/contact/" class="btn btn-secondary">문의하기</a>
    </div>
  </section>
  
  <!-- SEO 키워드 섹션 (검색엔진용) -->
  <section class="seo-keywords" style="display: none;">
    <h2>X-ray 검사 장비 전문업체</h2>
    <p>NH는 X-ray, xray, 엑스레이, 엑스 레이, X레이, X-RAY 검사 장비를 전문으로 제조하는 업체입니다.</p>
    <p>엑스레이 자동화 장비, xray 자동화 시스템, X-ray 자동화 솔루션을 제공합니다.</p>
    <p>X레이 검사 시스템, 엑스 레이 검사 장비, X-RAY 검사 솔루션 전문 제조업체입니다.</p>
    <p>X레이 타겟 드릴, X-ray 타겟드릴, X-ray 가이드 홀 펀칭머신, 전문 제조업체입니다.</p>
  </section>
</div> 

  <!-- <section class="company-intro">
    <h2>회사 소개</h2>
    <p>엔에이치 주식회사는 최신 기술을 활용한 X-ray 자동화 장비를 제조하여 고객의 품질 관리 시스템을 혁신하고 있습니다.</p>
    <a href="/about/" class="btn btn-outline">회사 소개 더 보기</a>
  </section> -->