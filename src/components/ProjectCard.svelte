<script lang="ts">
  export let title: string;
  export let text: string;
  export let img: string;
  export let alt: string;
  export let bgColor: string;
  export let fontColor: string;
</script>

<div
  class="container"
  style={`background-color: ${bgColor};color: ${fontColor}`}
>
  <div class="title"><h1>{title}</h1></div>
  <img src={img} {alt} />
  <div class="text">{text}</div>
</div>

<style lang="scss">
  div {
    display: flex;
    flex-direction: column;
    width: 27vw;
    height: fit-content;
    border-radius: 1rem 1rem 1rem 1rem;
    transition: all 1s ease-in-out;
    z-index: 2;
    .title {
      display: flex;
      justify-content: left;
      padding: 0 0.5rem;
    }
    img {
      max-width: 100%;
      border-radius: 0.5rem;
    }
    .text {
      align-items: center;
      overflow: hidden;
      max-height: 0;
      padding: 0.25rem 0.75rem;
    }
    &:hover {
      width: 33vw;
      z-index: 10;
      & .text {
        max-height: 5rem;
      }
    }
  }
  .container {
    transition: all 1s ease-in-out;
    padding: 0.5rem;
    box-shadow: 0 1px 3px rgba(0, 0, 0, 0.12), 0 1px 2px rgba(0, 0, 0, 0.24);
    &:hover {
      box-shadow: 0 14px 28px rgba(0, 0, 0, 0.25),
        0 10px 10px rgba(0, 0, 0, 0.22);
    }
  }
</style>
