<script lang="ts">
  import Nav from "../components/common/Nav.svelte";
  import GoButton from "../components/common/GoButton.svelte";
  import { authenticated } from "../logic/stores";

  let isAuthenticated: boolean;

  authenticated.subscribe((value) => {
    isAuthenticated = value;
  });
</script>

<svelte:head>
  <title>Home - Hyperfox</title>
</svelte:head>

<Nav />

<div class="content">
  <h1>Hyperfox</h1>
  <h2>A real-time, open source chat platform.</h2>

  <div class="app-redirect">
    {#if isAuthenticated}
      <GoButton url="/app" options={{ large: true }}>Go to App</GoButton>
    {:else}
      <GoButton url="/auth?type=login" options={{ large: true }}>Login</GoButton>
      <GoButton url="/auth?type=login" options={{ large: true }}>Sign Up</GoButton>
    {/if}
  </div>
</div>

<style lang="scss">
  .content {
    text-align: center;
  }

  h1 {
    font-size: 4rem;
  }

  h2 {
    font-size: 2rem;
  }

  .app-redirect {
    margin-top: 4rem;
  }
</style>
