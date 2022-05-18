<div class="nav">
  <a href="/">
    <img src="/logo.svg" alt="Hyperfox Logo" />
    <h1>Hyperfox</h1>
  </a>
  <div class="fill" />
  <button on:click={() => (window.location.href = "/app")} class="btn">App</button>
  <button on:click={() => (window.location.href = "https://github.com/hyperfox-chat")} class="btn"
    >GitHub</button
  >
  <button on:click={() => (window.location.href = "https://docs.hyperfox.uk")} class="btn"
    >Docs</button
  >
</div>

<style lang="scss">
  .nav {
    background-color: $col-bg-light;
    height: 3rem;
    padding: 0 0.5rem;

    display: flex;
    align-items: center;
    flex-direction: row;

    a {
      display: flex;
      align-items: center;
      flex-direction: row;
      text-decoration: none;
      color: $col-text;
    }

    .btn {
      height: 3rem;
      background-color: #00000000;
      border: none;
      color: $col-text;
      padding: 0 1rem;
      font-size: 1rem;
    }

    .btn:hover {
      background-color: $col-bg-lighter;
    }

    img {
      height: 2.5rem;
      margin-right: 0.5rem;
    }

    h1 {
      font-size: 1.5rem;
    }
  }

  @media (min-width: 768px) {
    .nav {
      padding: 0 10%;
    }
  }
</style>
