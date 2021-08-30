<template>
  <div class="card">
    <div class="card-content">
      <h3 class="card-title">Get <span>insights</span> that help your business grow.</h3>

      <p class="card-text">Discover the benefits of data analytics and make better decisions regarding revenue, customer experience, and overall efficiency.</p>

      <div class="card-numbers">
        <div class="numbers-item">
          <p class="item-number">10k+</p>
          <p class="item-label">Companies</p>
        </div>

        <div class="numbers-item">
          <p class="item-number">314</p>
          <p class="item-label">Templates</p>
        </div>

        <div class="numbers-item">
          <p class="item-number">12M+</p>
          <p class="item-label">Queries</p>
        </div>
      </div>
    </div>
    <div class="card-img">
      <img :src="require(`@/assets/${cardImg}`)" alt="Card Image">
    </div>
  </div>
</template>

<script>
export default {
  name: "Card",
  computed: {
      cardImg() { return window.innerWidth < 651 ? 'header-mobile.jpg' : 'header-desktop.jpg' }
  },
  mounted() {
    window.addEventListener('resize', function() {
      this.cardImg = window.innerWidth < 651 ? 'header-mobile.jpg' : 'header-desktop.jpg'
    })
  }
}
</script>

<style lang="scss" scoped>
  @import '../themes/variables.scss';

  .card {
    position: relative;
    overflow: hidden;
    display: flex;
    align-items: stretch;
    width: 100%;
    max-width: 1110px;
    border-radius: 8px;
    background: #1b1937;
    box-shadow: 0 20px 20px -10px rgba(23, 25, 41, 0.203087);

    @media (max-width: 1110px) {
      margin: 48px;
    }

    @media (max-width: 651px) {
      flex-direction: column-reverse;
      margin: 24px;
    }

    .card-img {
      width: 100%;
      background: #ab5cdb;

      @media (max-width: 651px) {
        overflow: hidden;
        max-height: 240px;
      }

      img {
        display: block;
        width: 100%;
        height: 100%;
        mix-blend-mode: multiply;
        opacity: 0.75;
        object-fit: cover;
        object-position: top right;
      }
    }

    .card-content {
      text-align: center;
      padding: 71px 95px 59px 72px;

      @media (max-width: 768px) {
        padding: 35px 47px 29px 36px;
      }

      @media (max-width: 651px) {
        padding: 40px 31.5px 32px;
      }
    }

    .card-title {
      margin-bottom: 25px;
      font-family: $fontInter;
      font-style: normal;
      font-weight: bold;
      font-size: 36px;
      line-height: 44px;
      color: #ffffff;

      @media (max-width: 475px) {
        margin-bottom: 16px;
        font-size: 28px;
        line-height: 32px;
      }

      span {
        color: #ab5cdb;
      }
    }

    .card-text {
      margin-bottom: 72px;
      font-family: $fontInter;
      font-style: normal;
      font-weight: normal;
      font-size: 15px;
      line-height: 25px;
      color: #ffffff;
      mix-blend-mode: normal;
      opacity: 0.75;

      @media (max-width: 475px) {
        margin-bottom: 40px;
        font-size: 15px;
        line-height: 25px;
      }
    }

    .card-numbers {
      display: flex;
      align-items: stretch;

      @media (max-width: 651px) {
        justify-content: center;
      }

      @media (max-width: 475px) {
        flex-direction: column;
      }

      .numbers-item {
        margin-right: 60px;

        &:last-of-type {
          margin-right: 0;
        }

        @media (max-width: 475px) {
          margin-right: 0;
          margin-bottom: 24px;

          &:last-of-type {
            margin-bottom: 0;
          }
        }

        .item-number {
          margin-bottom: 2px;
          font-family: $fontInter;
          font-style: normal;
          font-weight: bold;
          font-size: 24px;
          line-height: 29px;
          color: #ffffff;
        }

        .item-label {
          font-family: $fontLexend;
          font-style: normal;
          font-weight: normal;
          font-size: 12px;
          line-height: 25px;
          letter-spacing: 1px;
          text-transform: uppercase;
          color: #ffffff;
          mix-blend-mode: normal;
          opacity: 0.6;
        }
      }
    }
  }
</style>
