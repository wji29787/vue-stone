<template>

  <div>
    <div class="page-header row-2 u-cross-center">
      <div class="page-header-left u-cross-center row-2">
        <router-link to="/" class="back-link">
          <span class="icon v-icon-pull-left page-header-icon"></span>返回
        </router-link>
      </div>
    </div>

    <v-panel>
      <div slot="header" class="c-panel-header row-1 u-cross-center">dayspicker</div>
      <div slot="body" class="c-panel-body row-5 u-cross-center">
        <v-dayspicker ref="dayspicker" v-model="dayspickerList">
        </v-dayspicker>
      </div>
    </v-panel>

  </div>
</template>

<script>

  export default {
    name: 'dayspicker',

    data() {
      return {
        dayspickerList: [1, 2, 3, 4, 5],
      };
    },

    mounted() {
      this.$refs.dayspicker.$on('change', (value) => {
        console.log(`当前的星期选择是: ${value}`);
      });
    },
  };
</script>

<style>
</style>
