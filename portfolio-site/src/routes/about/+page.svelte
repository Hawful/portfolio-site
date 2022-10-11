<script lang="ts">
  import FrameSet from "../../components/FrameSet.svelte";
  import oliviaHair from "$lib/images/me-and-olivia.jpg";
  import familyBoat from "$lib/images/family-on-boat.jpg";
  import oliviaFace from "$lib/images/OliviaFace.jpg";

  let photos = [
    { id: 1, position: "left", image: oliviaHair, alt: "Olivia and Michael" },
    { id: 2, position: "center", image: familyBoat, alt: "Family on Boat" },
    {
      id: 3,
      position: "right",
      image: oliviaFace,
      alt: "Olivia at top of slide",
    },
  ];
</script>

<svelte:head>
  <title>About</title>
</svelte:head>

<div class="container">
  <section>
    <div class="inner-container">
      <h2 class="title">I'm Michael Hoff 👋</h2>
      <div class="subtitle">
        <p>
          Software Engineer and a Technical Writer with a solid background in
          Computer Science, I'm passionate about making the web accessible for
          everyone. I design and develop visually compell ing applications with
          user-friendly interaction that drive business g owth and improve user
          experience. When I'm not solving problems, I love to create technical
          content for engineers and tech startups across the globe.
        </p>
        <FrameSet {photos} />
        <p>
          Creating magic daily on the internet. You can send me an email at <span
            class="info-text">me@michaelhoff.io</span
          >
        </p>
      </div>
    </div>
  </section>
</div>

<style>
  .container {
    margin: 0 80px 0 65px;
  }

  .title {
    font-size: 4.2rem;
    font-weight: bold;
    margin-top: 11rem;
  }

  .subtitle {
    margin-top: -2rem;
  }

  .subtitle > p {
    width: 60%;
    font-weight: normal;
    font-size: 1rem;
    line-height: 2rem;
  }

  .info-text {
    font-style: italic;
    font-weight: bold;
  }
</style>
