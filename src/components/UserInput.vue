<template>
  <h3 >اسمك بالعربي</h3>
  <input
    type="text"
    class="form-control"
    aria-label="Sizing example input"
    aria-describedby="inputGroup-sizing-sm"
    :value="formData.empName"
    @input="ChangeFormData({ empName: $event.target.value })"
    placeholder="مثال: أحمد سعد"
    dir="rtl"
  />
</template>
<script>
export default {
  name: 'UserInput',
  props: {
    formData: Object,
  },
  methods: {
    ChangeFormData(value) {
      console.log(value);
      this.$emit('changeFormData', value);
    },
  },
};
</script>

<style>
h3 {
  color: #597163;
}
</style>
