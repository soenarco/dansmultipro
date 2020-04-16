<template>
  <main id="site-content">
    <section v-show="isNotification" class="section-notification">
      <div class="row">
        <div class="col-sm-12 col-md-4 col-lg-4" />
        <div class="col-sm-12 col-md-4 col-lg-4 label-alert">
          <p>By accessing and using this website, you acknowledge that you have read and understand our <span>Cookie Policy, Privacy Policy,</span> and our <span>Terms of Service.</span></p>
        </div>
        <div class="col-sm-12 col-md-4 col-lg-4 btn-alert">
          <button type="button" class="btn" @click="handleNotification">Got it</button>
        </div>
      </div>
    </section>
    <section class="section-banner">
      <div class="content-banner">
        <div class="row">
          <div class="col-sm-12">
            <img class="logo" src="~assets/img/home/y-logo-white.png" alt="cermati.com">
          </div>
        </div>

        <div class="row greeting">
          <div class="col-sm-12">
            <p class="note-first">Hello! I’m Sunarko</p>
            <p class="note-second">Consult, Design, and Develop Websites</p>
            <p>Have something great in mind? Feel free to contact me.</p>
            <p>I'll help you to make it happen.</p>
            <button type="button" class="btn btn-primary-outline">Let's Make Contact</button>
          </div>
        </div>
      </div>
    </section>

    <section class="section-highlights">
      <div class="row highlights">
        <div class="col-sm-12">
          <p class="title">How Can I Help You?</p>
          <p>Our work then targeted, best practices outcomes social innovation synergy.</p>
          <p>Venture philanthropy, revolutionary inclusive policymaker relief. User-centered</p>
          <p>program areas scale.</p>
        </div>
      </div>

      <div class="row programs">
        <div v-for="item in programs" :key="item" class="col-sm-12 col-md-6 col-lg-4 list-programs">
          <div class="items">
            <div class="header">
              <div class="column-left">{{ item.title }}</div>
              <div class="column-right"><i :class="item.icon" aria-hidden="true" /></div>
            </div>
            <p>{{ item.description }}</p>
          </div>
        </div>
      </div>
    </section>

    <section v-show="isArticle" class="section-article">
      <div class="row">
        <div class="col-sm-12 col-md-12 col-lg-12 close">
          <i class="fa fa-times" aria-hidden="true" @click="closeArticle" />
        </div>
      </div>
      <div class="row">
        <div class="col-sm-12 col-md-12 col-lg-12">
          <h1>Get latest updates in web technologies</h1>
          <p>Get latest updates in web technologies. I write articles related to web technologies, such as design trends, development tools, UI/UX case studies and reviews, and more. Sign up to my newsletter to get them all.</p>
        </div>
      </div>
      <div class="row">
        <div class="col-sm-12 col-md-8 col-lg-8">
          <input type="email" class="form-control" placeholder="Email Address">
        </div>
        <div class="col-sm-12 col-md-4 col-lg-4">
          <button type="submit" class="btn btn-email" @click="closeArticle">Count me in!</button>
        </div>
      </div>
    </section>
  </main>
</template>

<script>
export default {
  name: 'Homepage',

  data() {
    return {
      programs: [
        {
          title: 'Consult',
          icon: 'fa fa-comments-o',
          description: 'Co-create, design thinking; strengthen infrastructure resist granular. Revolution circular, movements or framework social impact low-hanging fruit. Save the world compelling revolutionary progress.',
        },
        {
          title: 'Design',
          icon: 'fa fa-paint-brush',
          description: 'Policymaker collaborates collective impact humanitarian shared value vocabulary inspire issue outcomes agile. Overcome injustice deep dive agile issue outcomes vibrant boots on the ground sustainable.',
        },
        {
          title: 'Develop',
          icon: 'fa fa-cubes',
          description: 'Revolutionary circular, movements a or impact framework social impact low-hanging. Save the compelling revolutionary inspire progress. Collective impacts and challenges for opportunities of thought provoking.',
        },
        {
          title: 'Marketing',
          icon: 'fa fa-bullhorn',
          description: 'Peaceful; vibrant paradigm, collaborative cities. Shared vocabulary agile, replicable, effective altruism youth. Mobilize commitment to overcome injustice resilient, uplift social transparent effective.',
        },
        {
          title: 'Manage',
          icon: 'fa fa-tasks',
          description: 'Change-makers innovation or shared unit of analysis. Overcome injustice outcomes strategize vibrant boots on the ground sustainable. Optimism, effective altruism invest optimism corporate social.',
        },
        {
          title: 'Evolve',
          icon: 'fa fa-line-chart',
          description: 'Activate catalyze and impact contextualize humanitarian. Unit of analysis overcome injustice storytelling altruism. Thought leadership mass incarceration. Outcomes big data, fairness, social game-changer.',
        },
      ],
      isArticle: true,
      isNotification: true,
    };
  },

  methods: {
    closeArticle() {
      this.isArticle = !this.isArticle;
    },

    handleNotification() {
      window.scrollTo(0, 0);
      this.isNotification = !this.isNotification;
    },
  },

  head() {
    return {
      title: 'Sunarko | Cermati.com Front-end Developer Entry Test',
      bodyAttrs: {
        class: 'page-home',
      },
    };
  },
};
</script>

<style lang="scss">
html {
  scroll-behavior: smooth;
}

.section-banner {
  background-image: url('~assets/img/home/work-desk__dustin-lee.jpg');
  height: 80%;
  margin: 0;
  width: 100%;

  p {
    margin: 0;
    font-size: 20px;
  }

  .content-banner {
    background-color: #004a75;
    opacity: 0.7;
  }

  .logo {
    margin: 2%  ;
    width: 5%;
    height: 50%;
  }

  .greeting {
    text-align: center;
    color: white;
    padding: 10% 0;

    .note-first {
      font-size: 40px;
    }

    .note-second {
      font-size: 28px;
      font-weight: bold;
    }
  }

  .btn-primary-outline {
    background-color: transparent;
    border:3px solid white;
    box-shadow: none;
    color: white;
    font-size: 18px;
    font-weight: bold;
    margin-top: 15px;
    padding: 10px 30px;
  }

  .btn-primary-outline:hover {
    background-color: white;
    border:3px solid #004a75;
    box-shadow: none;
    color: #004a75;
    font-size: 18px;
    font-weight: bold;
    margin-top: 15px;
    padding: 10px 30px;
  }
}

.section-highlights {
  text-align: center;

  p {
    margin: 0;
    font-size: 16px;
  }

  .title {
    font-size: 28px;
  }

  .programs {
    margin: 3%;
    align-items: center;

    .list-programs {
      padding: 1%;

      .items {
        border: 1px solid #e5e5e5;
        text-align: left;
        padding: 5%;
      }

      .header {
        font-size: 30px;
        display: flex;
        width: 100%;

        .column-left {
          width: calc(100% - 10%);
        }

        .column-right {
          width: calc(100% - 90%);
          text-align: right;
        }
      }
    }
  }
}

.section-notification {
  margin: 0;
  top: 0;
  left: 0;
  width: 100%;
  max-height: 20%;
  background-color: white;
  z-index: 100;
  text-align: left;
  position: fixed;
  padding: 2%;

  span {
    color: #007bc1;
    font-weight: bold;
  }

  button, button:hover {
    background-color: #007bc1;
    color: white;
  }

  p {
    margin: 0;
  }
}

.section-article {
  margin: 0;
  bottom: 0;
  left: 0;
  max-height: 100%;
  padding: 2%;
  position: fixed;
  border: 1px solid #007bc1;
  background-color: #007bc1;
  color: white;
  opacity: 0.8;

  .btn-email {
    background-color: #ff8000;
    color: white;
    font-weight: bold;
    width: 100%;
    margin: 1% 0;
    font-size: 100%;
  }

  h1 {
    font-size: 28px;
  }

  .close {
    text-align: right;
    margin: -2% 0 0 0;
    font-size: 20px;
  }

  // Small devices (landscape phones, 576px and up)
  @media (min-width: 576px) {
    max-width: 100%;
  }

  // Medium devices (tablets, 768px and up)
  @media (min-width: 768px) {
    max-width: 42%;
  }

  // Large devices (desktops, 992px and up)
  @media (min-width: 992px) {
    max-width: 42%;
  }

  // Extra large devices (large desktops, 1200px and up)
  @media (min-width: 1200px) {
    max-width: 42%;
  }
}
</style>
