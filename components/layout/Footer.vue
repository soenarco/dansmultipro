<template>
  <footer id="site-footer">
    <!-- COPYRIGHT -->
    <div class="section-footer-copyright">
      <div class="container">
        <div class="row justify-content-center">
          &copy; {{ year }} Sunarko. All rights reserved.
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
import moment from 'moment';

export default {
  asynData() {
    return {
      year: moment().format('YYYY'),
    };
  },

  data() {
    return {
      year: '2020',
    };
  },
};
</script>

<style lang="scss">
#site-footer {
  z-index: 2;
  background-color: #004a75;
  padding: 2%;

  .section-footer-sitemap {
    padding: 2% 20%;
    background-color: $grey;

    .row {
      margin: 2% 0;
    }

    div {
      margin: 1% 0;
    }

    input {
      width: 80%;
      height: 25%;
      border-radius: 25px;
    }

    span {
      button {
        width: 12%;
        height: 60%;
        border-radius: 10px;
        font-size: 12px;
      }
    }

    .payment {
      margin: 0 0;
    }
  }
}
</style>
