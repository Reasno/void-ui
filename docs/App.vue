<template>
  <div id="app">
    <main-nav mode="router"></main-nav>
    <div class="vd-wrapper">
      <div class="vd-section vd-container">
        <keep-alive>
          <router-view></router-view>
        </keep-alive>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
// Learn more:
// https://github.com/vuejs/vue-class-component
// https://github.com/kaorun343/vue-property-decorator
import {
  Component,
  Emit,
  Inject,
  Model,
  Prop,
  Provide,
  Vue,
  Watch,
} from 'vue-property-decorator';
import VoidUI from 'void-ui';
Vue.use(VoidUI);

import MainNav from 'docs/components/MainNav.vue';

@Component({
  components: {
    MainNav,
  },
})
export default class Main extends Vue {
  @Watch('$route')
  changePageTitle() {
    document.title = this.$route.name || 'Void-UI';
  }
}
</script>
