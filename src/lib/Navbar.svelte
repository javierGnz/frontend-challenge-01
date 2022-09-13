<script>
  import avatar from '../assets/images/image-avatar.png'

  import Logo from '../assets/images/logo.svg'
  import IconMenu from '../assets/images/icon-menu.svg'
  import IconCart from '../assets/images/icon-cart.svg'
</script>

<div class="navbar">
  <div class="navbar_left">
    <button class="menu-trigger">
      <IconMenu />
    </button>
    <div class="logo">
      <a href="/">
        <Logo />
      </a>
    </div>
    <div class="menu-list">
      <ul>
        <li><a href="/">Collections</a></li>
        <li><a href="/">Men</a></li>
        <li><a href="/">Women</a></li>
        <li><a href="/">About</a></li>
        <li><a href="/">Contact</a></li>
      </ul>
    </div>
  </div>

  <div class="navbar_rigth">
    <button class="shopping-cart">
      <IconCart />
    </button>
    <img class="avatar" src={avatar} alt="Avatar" />
  </div>
</div>

<style lang="scss">
  @import '../styles/variables.scss';
  @import '../styles/mixins.scss';

  .navbar {
    display: flex;
    align-items: baseline;
    justify-content: space-between;
    padding-block: 1rem;
    border-bottom: 1px solid $color-secondary-300;
    gap: 1rem;

    &_left {
      display: inline-flex;
      align-items: baseline;
      gap: 0.5rem;
    }

    &_rigth {
      display: inline-flex;
      gap: 1rem;
    }
  }

  .menu-trigger {
    background: none;
    padding: 0;
    margin: 0;
    border: none;
    display: inline-flex;
  }

  .menu-list {
    display: none;

    ul {
      display: flex;
      list-style: none;
    }
  }

  .shopping-cart {
    padding: 0;
    margin: 0;
    background: none;
    border: none;
  }

  .avatar {
    max-width: 1.625rem;

    @include media-breakpoint-up(md) {
      max-width: 2.5rem;
    }
  }
</style>
