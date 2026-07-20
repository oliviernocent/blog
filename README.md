# blog
Testing Jekyll for a simple blog site

<button data-filter=".alternance">alternance</button>
<button data-filter=".stage">stage</button>
<div class="grid">
  <div class="element-item alternance">

## Alternance chez Decathlon

- Lieu : Lille
- Période : 01/09/2026 au 30/07/2027
    
  </div>
  <div class="element-item stage">

## Stage 

- Lieu : Reims
- Période : 01/01/2027 au 30/01/2027
    
  </div>
</div>

<!-- Optional JavaScript -->
  <!-- jQuery first, then Isotope (filtered items) -->
  <script src="https://code.jquery.com/jquery-3.2.1.slim.min.js"
    integrity="sha384-KJ3o2DKtIkvYIK3UENzmM7KCkRr/rE9/Qpg6aAZGJwFDMVNA/GpGFF93hXpG5KkN"
    crossorigin="anonymous"></script>
  <script src="https://unpkg.com/isotope-layout@3.0.6/dist/isotope.pkgd.min.js"></script>
  <script>
    /*
     * Isotope initialization
     *
     */

    $('.grid').isotope({
      // options
      itemSelector: '.grid-item',
      layoutMode: 'fitRows'
    });

    /*
     * Event callback for filters triggering
     *
     */
    $(".button").on("click", function () {
      $('.grid').isotope({ filter: $(this).attr("data-filter") });
      $(".button").removeClass("is-info");
      $(this).addClass("is-info");
    });
  </script>
