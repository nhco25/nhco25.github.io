---
layout: default
title: NH
---

<div class="hero-section">
  <div class="hero-image">
    <img src="/assets/images/hero-image.jpg" alt="X-ray 장비 이미지">
  </div>
  <div class="overlay"></div>
  <div class="hero-content">
    <h1>X-ray 및 광확비전의<br>혁신적인 솔루션</h1>
    <div class="bottom-content">
      <p>엔에이치는 X-ray와 광학비전을 통한 검사, 분석, 타공 장비,<br> PLC 공정 자동화 장비를 전문제작 합니다.<br>최신 기술로 공정 자동화에 혁신을 가져옵니다.</p>
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
</div> 

  <!-- <section class="company-intro">
    <h2>회사 소개</h2>
    <p>엔에이치 주식회사는 최신 기술을 활용한 X-ray 자동화 장비를 제조하여 고객의 품질 관리 시스템을 혁신하고 있습니다.</p>
    <a href="/about/" class="btn btn-outline">회사 소개 더 보기</a>
  </section> -->