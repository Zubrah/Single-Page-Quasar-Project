<template>
  <q-page class="q-pa-lg full-width row wrap">
    <div class="divider">
      <div class="row no-wrap q-pr-xl q-pt-lg">
        <q-toolbar class="bg-transparent">
          <q-icon name="img:/iconlogo.svg" class="logo-size"></q-icon>
        </q-toolbar>

        <q-toolbar class="desktop-only">
          <q-space />
          <q-tabs v-model="tab" shrink class="tab-font">
            <q-tab no-caps name="tab1" label="Courses" />
            <q-tab no-caps name="tab2" label="Features" />
            <q-tab no-caps name="tab3" label="Support" />
          </q-tabs>
        </q-toolbar>

        <q-toolbar>
          <q-space />
          <q-btn flat round dense icon="img:/messageicon.svg" class="q-mr-sm">
            <q-badge
              floating
              rounded
              color="negative"
              class="q-mt-xs q-mr-xs q-px-xs badge-label"
              >3</q-badge
            >
          </q-btn>
          <q-avatar size="30px">
            <img src="../assets/profile.jpeg" />
          </q-avatar>

          <q-btn-dropdown rounded color="primary" class="mobile-only q-ml-sm drop-btn">
            <q-list>
              <q-item  >
                <q-item-section>
                  <q-item-label>Courses</q-item-label>
                </q-item-section>
              </q-item>

              <q-item  >
                <q-item-section>
                  <q-item-label>Features</q-item-label>
                </q-item-section>
              </q-item>

              <q-item  >
                <q-item-section>
                  <q-item-label>Support</q-item-label>
                </q-item-section>
              </q-item>
            </q-list>
          </q-btn-dropdown>
        </q-toolbar>
      </div>

      <div class="q-pa-xl q-mt-lg q-ml-xl force-pad">
        <div class="div-size">
          <p class="font-body">
            Study different areas of web design easily 
          </p>
          <p class="font-body">
            in 3 steps:
            </p>
        </div>

        <div class="q-my-lg">
          <q-list>
            <q-item v-for="item in listItem" :key="item.id">
              <q-item-section side left>
                <q-item-label class="font-side-left">{{
                  item.id
                }}</q-item-label>
              </q-item-section>

              <q-item-section>
                <q-item-label class="list-label">{{ item.title }}</q-item-label>
              </q-item-section>
            </q-item>
          </q-list>
        </div>

        <div>
          <q-btn
            unelevated
            no-caps
            color="primary"
            text-color="white"
            class="primary-btn"
            label="Sign In"
          />
        </div>
      </div>
    </div>

    <div class="img-divider">
      
      <div class="bg"></div>
    </div>
  </q-page>
</template>

<script>
export default {
  name: "PageIndex",
  methods: {
    onItemClick () {
      
    }
  },
  data() {
    return {
      tab: "",

      listItem: [
        {
          id: ".01",
          title: "Visit our website"
        },
        {
          id: ".02",
          title: "Sign Up"
        },
        {
          id: ".03",
          title: "Find the course you want"
        }
      ]
    };
  }
};
</script>

<style lang="scss">
@media only screen and (max-width: 600px) {
  .tab-font {
    font-family: "Century Gothic", "Montserrat";
    font-size: 10px;
    font-weight: 500;
    color: #001a26;
  }

  .badge-label {
    font-family: "Century Gothic", "Montserrat";
    font-size: 8px;
    font-weight: 700;
  }

  .force-pad{
    margin: auto;
  }

  .logo-size {
    width: 100%;
  }

  .font-body {
    font-family: "Century Gothic", "Montserrat";
    font-weight: 700;
    font-size: 30px;
    color: black;
  }

  .font-side-left {
    font-family: "Century Gothic", "Montserrat";
    font-weight: 700;
    font-size: 10px;
    color: #839eff;
  }

  .list-label {
    font-family: "Century Gothic", "Montserrat";
    font-size: 14px;
    font-weight: 400;
    color: #001a26;
  }

  .primary-btn {
    font-family: "Century Gothic", "Montserrat";
    font-size: 15px;
    font-weight: 700;
    border-radius: 33px;
    padding: 0.5% 10% 0.5% 10%;
    box-shadow: 0px 16px 0px -12px rgba(197, 209, 255, 1);
    -webkit-box-shadow: 0px 16px 0px -12px rgba(197, 209, 255, 1);
    -moz-box-shadow: 0px 16px 0px -12px rgba(197, 209, 255, 1);
  }

  .bg {
    background: url("../assets/left_backgroundpics.png") no-repeat;
    background-size: contain;
    background-position: center;
    width: 500px;
    height: 500px;
  }

  .drop-btn{
      width: 30px;
      height: 30px;
  }
}

@media only screen and (min-width: 600px) {
  .tab-font {
    font-family: "Montserrat", sans-serif;
    font-size: 12px;
    font-weight: 500;
    color: #001a26;
  }

  .divider {
    width: 60%;
  }

  .img-divider {
    width: 40%;
  }

  .badge-label {
    font-family: "Montserrat", sans-serif;
    font-size: 10px;
    font-weight: 700;
  }

  .logo-size {
    width: 100%;
  }

  .font-body {
    font-family: "Niramit", sans-serif;
    font-weight: 700;
    font-size: 40px;
    color: black;
  }

  .font-side-left {
    font-family: "Mukta", sans-serif;
    font-weight: 700;
    font-size: 12px;
    color: #839eff;
  }

  .list-label {
    font-family: "Montserrat", sans-serif;
    font-size: 18px;
    font-weight: 400;
    color: #001a26;
  }

  .primary-btn {
    font-family: "Montserrat", sans-serif;
    font-size: 18px;
    font-weight: 700;
    border-radius: 33px;
    padding: 0.5% 10% 0.5% 10%;
    box-shadow: 0px 16px 0px -12px rgba(197, 209, 255, 1);
    -webkit-box-shadow: 0px 16px 0px -12px rgba(197, 209, 255, 1);
    -moz-box-shadow: 0px 16px 0px -12px rgba(197, 209, 255, 1);
  }

  .div-size {
    width: 65%;
  }

  .bg {
    background: url("../assets/left_backgroundpics.png") no-repeat;
    background-size: contain;
    background-position: center;
    width: auto;
    height: 100%;
  }
}
</style>
