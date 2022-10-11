<script lang="ts">
  import Frame from "./Frame.svelte";
  import { fly } from "svelte/transition";
  import { onMount } from "svelte";
  export let photos: Array<Photo>;

  let ready = false;
  onMount(() => (ready = true));

  type Photo = {
    id?: number;
    position?: string;
    image?: string;
    alt?: string;
  };
</script>

<div class="container">
  {#if ready}
    {#each photos as photo (photo.id)}
      <div
        transition:fly={{
          x: 250,
          y: 250,
          delay: 350 * photo.id,
          duration: 700,
        }}
        class="frame {photo.position}"
      >
        <Frame image={photo.image} alt={photo.alt} />
      </div>
    {/each}
  {/if}
</div>

<style>
  div.container {
    display: flex;
    justify-content: center;
  }
  @media (min-width: 300px) {
    div.container {
      flex-direction: column;
    }
  }
  @media (min-width: 800px) {
    div.container {
      flex-direction: row;
    }
  }
  div.frame {
    max-width: fit-content;
    max-height: fit-content;
  }

  div.left {
    transform: rotate(-23deg);
  }

  div.center {
    transform: rotate(-2deg);
  }

  div.right {
    transform: rotate(33deg);
  }
</style>
