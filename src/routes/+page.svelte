<script lang="ts">
  import photo from '$lib/images/manlookingtoside.jpg';
  import { beforeNavigate } from '$app/navigation';
  import { fade, fly } from 'svelte/transition';
  import ProjectCard from '../components/ProjectCard.svelte';
  import projectPhoto from '$lib/images/share1.png';
  import { onMount } from 'svelte';
  import InputField from '../components/InputField.svelte';
  import TextField from '../components/TextField.svelte';

  let loaded = false;
  let y = 0;

  let path: SVGGeometryElement;
  let pathLength: number;

  onMount(async () => {
    loaded = true;
    pathLength = path.getTotalLength();
    path.style.strokeDasharray = pathLength + ' ' + pathLength;
    path.style.strokeDashoffset = pathLength;
  });

  function drawSVG() {
    console.log('yeah');
    var scrollPercentage =
      (document.documentElement.scrollTop + document.body.scrollTop) /
      (document.documentElement.scrollHeight -
        document.documentElement.clientHeight);
    var drawLength = pathLength * scrollPercentage;

    path.style.strokeDashoffset = pathLength - drawLength;
  }
  const project = [
    {
      bgColor: '#1f3c37',
      fontColor: 'white',
      img: projectPhoto,
      title: 'A very cool project',
      text: 'This is a longer piece of text because I need to see how this looks and if the hover effect is even functional currently',
      alt: 'alt',
    },
    {
      bgColor: '#577e6b',
      fontColor: 'white',
      img: projectPhoto,
      title: 'A great project',
      text: 'This is a longer piece of text because I need to see how this looks and if the hover effect is even functional currently',
      alt: 'alt',
    },
    {
      bgColor: '#f2ba5d',
      fontColor: 'white',
      img: projectPhoto,
      title: 'An okay project',
      text: 'This is a longer piece of text because I need to see how this looks and if the hover effect is even functional currently',
      alt: 'alt',
    },
    {
      bgColor: '#df7d30',
      fontColor: 'white',
      img: projectPhoto,
      title: 'Something',
      text: 'This is a longer piece of text because I need to see how this looks and if the hover effect is even functional currently',
      alt: 'alt',
    },
  ];

  let word = 'Developer';
  const words = [
    'Code Monkey',
    'SQL Dev',
    'Script Kiddie',
    'Fullstack Dev',
    'Vite Fan',
    'Mongo Avoider',
    'Django Endjoyer',
    'Python Peruser',
    'Type Safe Zealot',
    'TypeScript Enjoyer',
    'Team Driven Professional',
    'Climate Activist',
    'Hot Take Haver',
    'Father',
    'Husband',
    'Artist',
    'Unicorn',
    'ServiceNow Expert',
    'JavaScript Tolerater',
    'Style Sheet Cascader',
    'Svelte Evangelist',
    'React Dev',
  ];

  function randomWord(): void {
    word = words[Math.floor(Math.random() * words.length)];
  }

  const interval = setInterval(randomWord, 2000);

  beforeNavigate(() => {
    clearInterval(interval);
  });
</script>

<svelte:head>
  <title>Michael Hoff</title>
</svelte:head>
<svelte:window on:scroll={() => drawSVG()} bind:scrollY={y} />

<div class="svg">
  <svg
    xmlns="http://www.w3.org/2000/svg"
    width="1000"
    height="1600"
    viewBox="0 0 860.78 1216.02"
  >
    <defs>
      <style>
        .a {
          fill: none;
          stroke: #1d653f;
          stroke-miterlimit: 10;
          stroke-width: 2px;
        }
      </style>
    </defs>
    <path
      bind:this={path}
      class="a"
      d="M829,109c-113,3-317.52-20-319,193.52L509,445l209,0,33.8.14c6.39,13.42,13.36,12.7,21.42,12.89s9.36,3.06,11.75,6.84,59.23-6.18,99.19,30.81C921,527.72,912.73,592.1,916.8,594s7.11,2.73,8.42,10.68.13,11.17,9.13,19.17l-1-173-122-2c25.2,7.36,62.11,18.12,79.66,39.68s36.91,60.33,37.34,77.32,0-93,0-93l-10,41-5-9,10-37-17,28-6-8,20-25-29,16-7.74-6.14,32.74-13.86-41,7-9-4,51-7h-67s-33.26-9.39-55.63-9.69-37.49,0-37.49,0L939.15,445v215.9l-859.85.42V877.18l181.92-.13s-15.12.3-37.49,0-55.63-9.7-55.63-9.7h-67l51-7-9-4-41,7,32.74-13.86-7.74-6.14-29,16,20-25-6-8-17,28,10-37-5-9-10,41s-.44-110,0-93,19.78,55.77,37.34,77.33S181.9,866,207.1,873.35l-122-2-1-173c9,8,7.82,11.21,9.13,19.17s4.34,8.84,8.41,10.68-4.22,66.23,32.61,98.3c40,37,96.79,27,99.19,30.81s3.69,6.66,11.75,6.85,15-.53,21.42,12.89l33.8.13,208.81-.1S632,877,633,921c1.82,80-23,77-38,92s-93,22-113,35-52,36-66,50-36,20-36,27c0,0-5,16,9,19s19.07,4,26,0,22-7,21-9-11-6-11-8-4-13-3-11,11,17,17,16,15-8,14-10-16-15-15-19,10,17,17,17,14-10,14-10-9-7-9-11,5,10,11,10,18-9,19,5-11,47-14,53-31,63-35,66-19,28-20,33-1,12,2,13,11,5,20-5,19-22,18-23-14-9-15-12,13,9,16,9,22-25,22-28-11-8-13-13,13,13,15,12,13-21.54,14-24.77S484,1182,483,1179s27.24,16.14,26.62,18.07S503,1202,506,1203s17,15,17,18-14-13-17-15-5-1.84-6,1.58S480,1234,480,1237s15,12,13,13-15-11-16-10-29,32-29,32,18-2,20-6-40,7-42,17-2,14-2,14-5,3-5,8-1,13,4,14,8.79,4,15.89,0S457,1305,457,1305s-20,3-24,0a22.28,22.28,0,0,1-6-7c-3-3,2,5-3-3s6,20,45,7,45-20,49-21-9,3-16,0-18-1-25-1-10-13-5-20,20-12,33-9,19,9,20,14-5-17-11-16,18-8,21-8,18,4,20,11-8-15-17-14,10-13,15-14,31,6,31,7-31-12-36-9a53,53,0,0,0-9,7,83.76,83.76,0,0,1-10-2c-3-1-9-4-13,1s-16,19.91-16,19.91S524,1221,524,1218s3-25,5-28-9-12,11-13,29-2,37,6,27,25,35,25,16,3,6,11-30,25-41,33-35,25-47,27,45-22,56-31,64-50,77-76,38-51,44-73,8-57,28-71,27,53-40,55-97-45-91-55,21,7,12,37-47,93.09-106,88,50-28,50,1,45,11,38,6-46-9-59,11"
      transform="translate(-78.3 -108)"
    />
  </svg>
</div>
<section>
  {#if loaded}
    <div class="hero-text">
      <div in:fly={{ y: 100, delay: 250, duration: 2000 }} class="text-box">
        <h1>Hi, I'm Michael Hoff 👋</h1>
        <h2 class="passions">
          A passionate
          {#key word}
            <span
              in:fade={{ delay: 250, duration: 300 }}
              out:fade={{ duration: 200 }}>{word}</span
            >
          {/key}
        </h2>
        <h2>Who wants to bring joy back to the web</h2>
      </div>
    </div>
    <div
      in:fly={{ y: 100, delay: 700, duration: 2000 }}
      class="portfolio-img-container"
    >
      <div class="img-wrapper">
        <img
          src={photo}
          alt="Man who is not me looking to the side"
          style={`transform: translate(0,${y * 0.35}px)`}
        />
        <div class="green" style={`transform: translate(0,${y * 0.4}px)`} />
        <div class="orange" style={`transform: translate(0,${y * 0.3}px)`} />
      </div>
    </div>
  {/if}
</section>
<section>
  <div class="grid">
    <div class="grid-item"><ProjectCard {...project[0]} /></div>
    <div class="grid-item"><ProjectCard {...project[1]} /></div>
    <div class="grid-item" />
    <div class="grid-item" />
    <div class="grid-item"><ProjectCard {...project[2]} /></div>
    <div class="grid-item"><ProjectCard {...project[3]} /></div>
  </div>
</section>
<section>
  <div class="form-container">
    <div class="row">
      <h1>Reach out about something exciting</h1>
    </div>
    <form
      target="_blank"
      action="https://formsubmit.co/me@michaelhoff.io"
      method="POST"
    >
      <div class="row">
        <InputField name="name" label="Full Name" />
        <InputField name="email" label="Email" />
      </div>
      <div class="text-area">
        <TextField name="message" label="Message" />
      </div>
      <div class="row">
        <button type="submit">Submit</button>
      </div>
    </form>
  </div>
  <span style="position:fixed;bottom:0;right:0;">{y}</span>
</section>

<style lang="scss">
  .svg {
    position: absolute;
    z-index: -1;
    top: 500px;
    left: 225px;
  }
  .form-container {
    display: flex;
    flex-direction: column;
  }
  .row {
    flex-direction: row;
    justify-content: center;
  }
  .text-area {
    flex-grow: 1;
  }
  img {
    border-radius: 0.3rem;
    width: 90%;
    box-shadow: 0 14px 28px rgba(0, 0, 0, 0.25), 0 10px 10px rgba(0, 0, 0, 0.22);
    z-index: 1;
  }
  .img-wrapper {
    position: relative;
    div {
      position: absolute;
      border: solid 0.3rem;
      width: 100%;
      height: 100%;
    }
    .green {
      border-color: #577e6b;
      top: 0.5rem;
      left: 0.5rem;
      z-index: 2;
      box-shadow: 0 14px 28px rgba(0, 0, 0, 0.25),
        0 10px 10px rgba(0, 0, 0, 0.22);
    }
    .orange {
      z-index: 3;
      border-color: #f2ba5d;
      top: -0.5rem;
      left: -0.5rem;
      box-shadow: 0 14px 28px rgba(0, 0, 0, 0.25),
        0 10px 10px rgba(0, 0, 0, 0.22);
    }
  }
  section {
    display: flex;
    height: 100vh;
    justify-content: space-around;
    align-items: center;
    div {
      display: flex;
      justify-content: center;
    }
    .text-box {
      display: flex;
      flex-direction: column;
      justify-content: left;
      * {
        margin: 0;
        padding: 0.2rem;
      }
      .passions {
        position: relative;
      }
      span {
        position: absolute;
        top: -0.1rem;
        left: 9.25rem;
        padding: 0.2rem 0.4rem;
        color: white;
        background-color: #1f3c37;
        border-radius: 0.3rem;
        box-shadow: 0 14px 28px rgba(0, 0, 0, 0.25),
          0 10px 10px rgba(0, 0, 0, 0.22);
      }
    }
    .portfolio-img-container {
      width: 25%;
    }
    .hero-text {
      width: 55%;
    }
  }
  .grid {
    display: grid;
    grid-template-columns: repeat(3, 25vw); /* 3 columns */
    grid-template-rows: repeat(2, 40vh); /* 3 rows  */
    gap: 5vh 5vw; /* 50 pixels of space added between rows and 30 pixels added between columns  */
  }

  .grid-item {
    padding: 10px;
  }

  button {
    background-color: transparent;
    border: solid black 0.1rem;
    border-radius: 0.1rem;
    padding: 1rem 3rem;
    margin: 2rem;
    transition: all 300ms ease-in-out;
    &:hover {
      background-color: #577e6b;
      color: white;
    }
  }
</style>
