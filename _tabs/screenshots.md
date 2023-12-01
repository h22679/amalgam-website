---
# the default layout is 'page'
icon: fas fa-camera
order: 3
---
<script src="https://cdnjs.cloudflare.com/ajax/libs/masonry/4.2.2/masonry.pkgd.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/imagesloaded/4.1.4/imagesloaded.pkgd.min.js"></script>

<script>
document.addEventListener('DOMContentLoaded', function() {
  var elem = document.querySelector('#gallery');
  var msnry = new Masonry(elem, {
    itemSelector: '.gallery-item',
    gutter: 16
  });
});
</script>

<style>
    .gallery {
  margin: 0 auto;
}

.gallery-item {
  width: 250px; /* This should match the columnWidth in Masonry options if set */
}
</style>

<div id="gallery" class="gallery">
  {% for image in site.data.gallery %}
    <div class="gallery-item">
      <img src="{{ image.url }}" alt="{{ image.title }}" />
    </div>
  {% endfor %}
</div>

<script>
window.addEventListener('load', function() {
  var elem = document.querySelector('#gallery');
  var msnry = new Masonry(elem, {
    itemSelector: '.gallery-item',
    gutter: 16
  });
});
</script>

<!--- > Add Markdown syntax content to file `_tabs/about.md`{: .filepath } and it will show up on this page.
{: .prompt-tip } --->
