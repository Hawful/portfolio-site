<script lang="ts">
  import frame from "$lib/images/instantcameraframe.png";
  export let image: string;
  export let alt: string;
</script>

<div class="picture">
  <div>
    <img class="frame" src={frame} alt="Instant film frame" />
    <img class="photo" src={image} {alt} />
  </div>
</div>

<style>
  .picture {
    position: relative;
    height: 525px;
    width: 450px;
  }

  .frame {
    position: relative;
    max-width: 100%;
    max-height: 100%;
  }

  .photo {
    position: absolute;
    top: 25px;
    left: 30px;
    max-width: 85%;
    max-height: 100%;
    z-index: -1;
  }
</style>
