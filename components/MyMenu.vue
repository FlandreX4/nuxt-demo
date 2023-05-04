<template>
  <div style="width: 300px">
    <a-menu
      mode="vertical"
    >
      <template v-for="item in list">
        <a-menu-item v-if="!item.children" :key="item.key">
          <a-icon type="pie-chart" />
          <span>{{ item.title }}</span>
        </a-menu-item>
        <MySubMenu v-else :key="item.key" :menu-info="item" />
      </template>
    </a-menu>
  </div>
</template>

<script>
export default {
  props: {
    list: {
      type: Array,
      default: () => [],
    },
  },
  name: "",
  data() {
    return {
    };
  },
  components: {},
  mounted() {},
  methods: {
  },
};
</script>