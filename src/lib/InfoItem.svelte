<script>
  import IconCart from '../assets/images/icon-cart.svg'

  const title = 'Fall Limited Edition Sneakers'
  const description =
    'These low-profile sneakers are your perfect casual wear companion. Featuring a durable rubber outer sole, theyll withstand everything the weather can offer.'
  const count = 0
</script>

<div class="info-item">
  <h6>Sneaker Company</h6>
  <h1>{title}</h1>
  <p>{description}</p>
  <div class="price">
    <div class="current-price">
      $125.00
      <span class="tag">50%</span>
    </div>
    <small class="original-price">$250.00</small>
  </div>
  <div class="buy-item">
    <div class="count-item">
      <button>-</button>
      <span>{count}</span>
      <button>+</button>
    </div>
    <button class="btn">
      <IconCart />
      Add to cart
    </button>
  </div>
</div>

<style lang="scss">
  @import '../styles/variables.scss';

  .info-item {
    h6 {
      font-size: 0.75rem;
      letter-spacing: 1px;
      text-transform: uppercase;
      color: $color-primary-400;
      margin-top: 0;
      margin-bottom: 0.75rem;
    }

    h1 {
      font-weight: $weight-700;
      margin-top: 0;
      color: $color-secondary-900;
    }

    p {
      color: $color-secondary-400;
      line-height: 1.4;
    }
  }

  .buy-item {
    display: grid;
    grid-template-columns: 0.75fr 1fr;
  }

  .count-item {
    display: flex;
    align-items: stretch;
  }

  .btn {
    background: $color-primary-400;
    border: 1px solid $color-primary-400;
    color: $white;
    font-weight: $weight-700;
    border-radius: 8px;
    padding: 0.75rem 1rem;
    display: inline-flex;
    align-items: center;
    justify-content: center;
    gap: 0.75rem;

    :global(svg path) {
      fill: currentColor;
    }
  }
</style>
