<script lang="ts">
  type Options = {
    large?: boolean;
  };

  export let url: string;
  export let options: Options;

  let styles = "";

  if (options.large) {
    styles += "width: 16rem;";
  }
</script>

<button on:click={() => (window.location.href = url)} style={styles}><slot /></button>

<style lang="scss">
  button {
    height: 3rem;
    width: 8rem;
    font-size: 1.5rem;
    background-color: $col-bg-light;
    border-radius: 0.5rem;
    border: none;
    color: $col-text;
  }

  button:hover {
    background-color: $col-bg-lighter;
    color: $col-text;
  }

  button:active {
    background-color: $col-bg-light;
    color: $col-text;
  }

  @media (max-width: 768px) {
    button {
      margin-top: 0.25rem;
    }
  }
</style>
