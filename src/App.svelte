<script>
  import InfoItem from './lib/InfoItem.svelte'
  import Navbar from './lib/Navbar.svelte'
</script>

<main>
  <Navbar />
  <div class="wrapper">
    <div>carousel</div>
    <InfoItem />
  </div>
</main>

<style lang="scss">
  @import './styles/mixins.scss';

  main {
    max-width: 1100px;
    margin-inline: auto;
    padding-inline: 1rem;
  }

  .wrapper {
    display: grid;
    align-items: center;
    gap: 4rem;

    @include media-breakpoint-up(md) {
      grid-template-columns: 0.8fr 1.2fr;
      padding: 4rem 2rem;
    }
  }
</style>
