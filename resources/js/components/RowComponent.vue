<template>
  <tr>
    <td>{{ produk.barang }}</td>
    <td>{{ produk.deskripsi }}</td>
    <td>{{ produk.stock }}</td>
    <td>{{ produk.price }}</td>
    <td>
      <button-component
        @emitclick="buttonClick"
        text="Tambah"
        style="padding: 12px 28px; background-color: #008cba"
      ></button-component>
    </td>
  </tr>
</template>
<script>
export default {
  props: {
    produk: {
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
