---
layout: archive
title: "Curriculum Vitae"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
person_schema: true
---

{% include base_path %}

<style>
  .gcv-mobile {
    display: none !important;
  }

  .gcv-desktop {
    display: block !important;
  }

  @media screen and (max-width: 1024px) {
    .gcv-desktop {
      display: none !important;
    }

    .gcv-mobile {
      display: block !important;
    }

    .gcv-mobile-box {
      width: 100%;
      height: 95vh;
      overflow-y: scroll;
      overflow-x: hidden;
      -webkit-overflow-scrolling: touch;
    }

    .gcv-mobile-pdf {
      width: 100%;
      height: 4200px;
      border: none;
    }
  }
</style>



<div class="gcv-desktop">
  <div style="display: flex; justify-content: center;">
    <iframe
      src="{{ base_path }}/files/CV_Goeum_Cha_052026.pdf"
      width="90%"
      height="900px"
      style="border: none;">
    </iframe>
  </div>
</div>

<!-- Mobile -->

<div class="gcv-mobile">
  <div class="gcv-mobile-box">
    <iframe
      src="{{ base_path }}/files/CV_Goeum_Cha_052026.pdf"
      class="gcv-mobile-pdf"
      style="border: none;">
    </iframe>
  </div>
</div>