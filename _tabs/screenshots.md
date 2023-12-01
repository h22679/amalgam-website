---
# the default layout is 'page'
icon: fas fa-camera
order: 5
---

<div id="gallery" class="gallery">
  {% for image in site.data.gallery %}
    <div class="gallery-item">
      <img src="{{ image.url }}" alt="{{ image.title }}" />
    </div>
  {% endfor %}
</div>

<script>
  window.onload = function() {
    var elem = document.querySelector('#gallery');
    var msnry = new Masonry(elem, {
      // options
      itemSelector: '.gallery-item',
      // columnWidth: 200, // can be set to any size or left out for automatic sizing
      gutter: 16
    });
  };
</script>

<style>
    .gallery {
  margin: 0 auto;
}

.gallery-item {
  width: 250px; /* This should match the columnWidth in Masonry options if set */
}
</style>

<script src="https://cdnjs.cloudflare.com/ajax/libs/masonry/4.2.2/masonry.pkgd.min.js"></script>


<!--- > Add Markdown syntax content to file `_tabs/about.md`{: .filepath } and it will show up on this page.
{: .prompt-tip } --->
