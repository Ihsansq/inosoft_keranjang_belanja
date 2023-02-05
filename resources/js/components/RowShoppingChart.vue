<template>
  <tr>
    <td>{{ shopping_list.barang }}</td>
    <td>{{ shopping_list.quantity }}</td>
    <td>{{ shopping_list.price }}</td>
    <td>{{ shopping_list.quantity * shopping_list.price }}</td>
    <td>
      <button-component
        @emitclick="buttonClick"
        text="Hapus"
        style="padding: 12px 28px; background-color: #f44336"
      ></button-component>
    </td>
  </tr>
</template>
<script>
export default {
  props: {
    shopping_list: {
      type: Object,
      default: "",
    },
  },
  methods: {
    buttonClick() {
      this.$emit("emitclick");
    },
  },
};
</script>
