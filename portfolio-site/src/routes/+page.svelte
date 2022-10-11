<script lang="ts">
  import layer1 from "$lib/images/Vista/RedwoodVista_0000_Layer1.png";
  import layer2 from "$lib/images/Vista/RedwoodVista_0001_Layer2.png";
  import layer3 from "$lib/images/Vista/RedwoodVista_0002_Layer3.png";
  import layer4 from "$lib/images/Vista/RedwoodVista_0003_Layer4.png";
  import layer5 from "$lib/images/Vista/RedwoodVista_0004_Layer5.png";
  import layer6 from "$lib/images/Vista/RedwoodVista_0005_Layer6.png";
  import layer7 from "$lib/images/Vista/RedwoodVista_0006_Layer7.png";
  import layer8 from "$lib/images/Vista/RedwoodVista_0007_Layer8.png";
  import carsonBlock from "$lib/images/test garbo/CarsonBlock.png";
  import pinkLady from "$lib/images/test garbo/PinkLady.png";
  import oldCarsonMansion from "$lib/images/test garbo/OldCarsonMansion.png";
  import skywalk from "$lib/images/test garbo/Skywalk2.png";
  import fisherman from "$lib/images/test garbo/Fisherman.png";

  import { Parallax, ParallaxLayer, StickyLayer } from "svelte-parallax";
</script>

<svelte:head>
  <title>Michael Hoff</title>
</svelte:head>

<Parallax sections={5} config={{ stiffness: 0.2, damping: 0.3 }}>
  <ParallaxLayer
    rate={0}
    span={3}
    style="background-image:
    linear-gradient(
      white, #a8a8a2);"
  />

  <ParallaxLayer
    offset={0.5}
    rate={-0.2}
    style="display:flex; justify-content:center;"
  >
    <div class="text-container">
      <h1 class="small">Hi I'm</h1>
    </div>
  </ParallaxLayer>
  <StickyLayer
    offset={{ top: 0.75, bottom: 1.75 }}
    style="display:flex; justify-content:center;"
  >
    <div class="text-container">
      <h1 class="medium">Michael</h1>
    </div>
  </StickyLayer>
  <StickyLayer
    offset={{ top: 1, bottom: 1.75 }}
    style="display:flex; justify-content:center;"
  >
    <div class="text-container">
      <h1 class="massive">Hoff</h1>
    </div>
  </StickyLayer>

  <ParallaxLayer rate={-0.55} offset={1.35}>
    <img src={layer1} alt="Horizon Ridgeline covered in trees" />
  </ParallaxLayer>
  <ParallaxLayer
    rate={-0.6}
    offset={2.3}
    style="display:flex; justify-content:center;"
  >
    <div class="text-container">
      <h2 class="medium white">A Developer and Designer</h2>
    </div>
  </ParallaxLayer>
  <ParallaxLayer rate={-0.5} offset={1.35}>
    <img src={layer2} alt="Far fog layer in front of trees" />
  </ParallaxLayer>
  <ParallaxLayer rate={-0.45} offset={1.35}>
    <img src={layer3} alt="Pin" />
  </ParallaxLayer>
  <ParallaxLayer rate={-0.35} offset={1.35}>
    <img src={layer4} alt="Pin" />
  </ParallaxLayer>
  <ParallaxLayer rate={-0.25} offset={1.35}>
    <img src={layer5} alt="Pin" />
  </ParallaxLayer>
  <ParallaxLayer
    rate={-0.6}
    offset={2.45}
    style="display:flex; justify-content:center;"
  >
    <div class="text-container">
      <h2 class="large white">Located in Eureka, CA</h2>
    </div>
  </ParallaxLayer>
  <ParallaxLayer rate={-0.2} offset={1.35}>
    <img src={layer6} alt="Pin" />
  </ParallaxLayer>
  <ParallaxLayer rate={-0.1} offset={1.35}>
    <img src={layer7} alt="Pin" />
  </ParallaxLayer>
  <ParallaxLayer rate={-0.1} offset={1.35}>
    <img src={layer8} alt="Pin" />
  </ParallaxLayer>
  <ParallaxLayer
    rate={0}
    offset={2.75}
    style="background-image: linear-gradient(#070201,#6CB4EE);"
  />
  <ParallaxLayer
    rate={0}
    offset={2.75}
    style="display:flex; justify-content:center;"
  >
    <div class="text-container">
      <h3 class="large white no-margin">An Engineer</h3>
      <h3 class="medium white center no-margin">with the heart</h3>
      <h3 class="large white right no-margin">of a Creative</h3>
    </div>
  </ParallaxLayer>

  <ParallaxLayer rate={0} offset={3.75} style="background-color: #6CB4EE;" />
  <ParallaxLayer rate={0} offset={4} style="background-color: #6CB4EE;" />

  <StickyLayer
    offset={{ top: 3, bottom: 5 }}
    style="display:flex; justify-content:center;"
  >
    <div class="text-container">
      <p class="small center white">
        Endlessly inspired by the natural and architectural wonder around me.
      </p>
    </div>
  </StickyLayer>
  <ParallaxLayer
    rate={0.6}
    offset={4.25}
    style="display:flex; justify-content:center;"
  >
    <div>
      <div class="picture-spread justify-center">
        <img src={fisherman} alt="Pin" />
      </div>
    </div>
  </ParallaxLayer>
  <ParallaxLayer
    rate={-2}
    offset={4.25}
    style="display:flex; justify-content:center;"
  >
    <div>
      <div class="picture-spread justify-right">
        <img src={pinkLady} alt="Pin" />
      </div>
    </div>
  </ParallaxLayer>
  <ParallaxLayer
    rate={1}
    offset={4.3}
    style="display:flex; justify-content:center;"
  >
    <div>
      <div class="picture-spread justify-left">
        <img src={oldCarsonMansion} alt="Pin" />
      </div>
    </div>
  </ParallaxLayer>
  <ParallaxLayer rate={-0.4} offset={4}>
    <img src={carsonBlock} alt="Carson Block Turret" />
  </ParallaxLayer>
  <ParallaxLayer
    rate={0.5}
    offset={4}
    style="display:flex; justify-content:right;"
  >
    <img src={skywalk} alt="Pin" />
  </ParallaxLayer>
</Parallax>

<style lang="scss">
  .picture-spread {
    min-width: 1500px;
    display: flex;
  }
  .justify-left {
    justify-content: left;
  }
  .justify-center {
    justify-content: center;
  }
  .justify-right {
    justify-content: right;
  }

  .text-container {
    min-width: 800px;
    // background-repeat: no-repeat;
    // background-size: cover;
    h1 {
      color: black;
      margin: 2rem;
      text-align: left;
    }
    .first-name {
      font-size: 4rem;
    }
    .last-name {
      font-size: 20rem;
    }

    .white {
      color: white;
    }
    .small {
      font-size: 2rem;
    }
    .medium {
      font-size: 4rem;
    }
    .large {
      font-size: 6rem;
    }
    .massive {
      font-size: 20rem;
    }
    .right {
      text-align: right;
    }
    .center {
      text-align: center;
    }
    .no-margin {
      margin: 0;
    }
  }

  @media (max-width: 600px) {
    .text-container {
      min-width: 320px;
      .small {
        font-size: 1rem;
      }
      .medium {
        font-size: 2rem;
      }
      .large {
        font-size: 3rem;
      }
      .massive {
        font-size: 10rem;
      }
    }
  }

  @media (max-width: 800px) {
    img {
      max-width: 1000px;
      height: auto;
    }
  }
</style>
