<template>
  <div>
    <MyMenu :list="list" />
  </div>
</template>

<script>
export default {
  name: "IndexPage",
  data() {
    return {
      list: [
        {
          key: "1",
          title: "Option 1",
        },
        {
          key: "2",
          title: "Navigation 2",
          children: [
            {
              key: "2.1",
              title: "Navigation 3",
              children: [{ key: "2.1.1", title: "Option 2.1.1" }],
            },
          ],
        },
      ],
    };
  },
};
</script>
