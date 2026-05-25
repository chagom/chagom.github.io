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
  .cv-pdf-wrap {
  display: flex;
  justify-content: center;
}

@media screen and (max-width: 1024px) {

  .cv-pdf-wrap {
    display: block;
    width: 100%;
    height: 95vh;
    overflow: auto;
    -webkit-overflow-scrolling: touch;

  }

  .cv-pdf {
    width: 100%;
    height: 95vh;
    border: none;
  }

}
</style>



<div class="cv-pdf-wrap">
  <!-- <div style="display: flex; justify-content: center;"> -->
    <iframe
      src="{{ base_path }}/files/CV_Goeum_Cha_052026.pdf"
      width="90%"
      height="900px"
      style="border: none;">
    </iframe>
  <!-- </div> -->
</div>
