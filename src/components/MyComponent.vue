<template>
  <div>
    <label v-for="(condiment,objKey) in bananaCondimentObj" v-bind:key="condiment">
      <input
        type="checkbox"
        name="everyCondiment"
        v-bind:value="objKey"
        v-model="selectedCondiments"
      >
      {{condiment}}
    </label>

    <br>
    <label>array={{selectedCondiments}}</label>

    <li>香蕉配料
      <ul type="circle">
        <li
        v-for="condiment in selectedCondiments"
        v-bind:key="condiment"
        >{{bananaCondimentObj[condiment]}}</li>
      </ul>
    </li>
  </div>
</template>

<script>
export default {
  name: "MyComponent",
  data() {
    return {
      name: "Hello world",
      toggle: false,
      selectedCondiments: ["miso"],
      bananaCondimentObj: {
        chocolate: "巧克力醬",
        strawberry: "草莓醬",
        flax: "胡麻醬",
        miso: "味噌",
        chili: "辣椒",
        garlic: "大蒜",
        soy_sauce: "醬油",
        thick_soy_sauce: "醬油膏",
        herbal_cream: "百草膏"
      },
    };
  },
  methods: {
    handleAppendCharacterClick() {
      this.$data.name += "a";
    }
  }
};
</script>

