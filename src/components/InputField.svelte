<script lang="ts">
  let value = '';
  export let name: string;
  export let label: string;
  //todo, write a couple functions to check input and add filled class to label
</script>

<div class="field">
  <label class:filled={value.length > 0} for={name}
    >{label}<span aria-hidden="true">*</span></label
  >
  <input type="text" {name} id="username" required bind:value />
</div>

<style type="scss">
  .field {
    position: relative;
    display: block;
    &:focus-within {
      label {
        top: -0.5rem;
        font-size: 0.7em;
        z-index: 2;
      }
    }
  }

  label {
    position: absolute;
    margin: 0;
    padding: 0;
    left: 0.8rem;
    top: 0.4rem;
    transition: all 0.5s ease-in-out;
    z-index: -1;
    background-color: #f2f2e7;
  }
  input {
    font-size: 1.25rem;
    padding: 0.4rem;
    margin-left: 0.5rem;
    margin-right: 0.5rem;
    margin-bottom: 0.5rem;
    background: transparent;
    z-index: 1;
    border: none;
    border-bottom: 2px solid black;
  }
  .filled {
    z-index: 2;
    top: -0.5rem;
    font-size: 0.7em;
  }
</style>
