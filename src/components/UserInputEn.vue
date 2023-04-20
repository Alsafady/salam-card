<template>
<h3>Your Name in English</h3>
<input  type="text" class="form-control" aria-label="Sizing example input" aria-describedby="inputGroup-sizing-sm" :value="formDataEn.empNameEn"
@input="ChangeFormDataEn({empNameEn:$event.target.value})"
placeholder="Ex: Ahmed Saad"
/>
</template>
<script>
export default {
  name: 'UserInputEn',
  props:{
      formDataEn: Object,
  },
  methods:{
      ChangeFormDataEn(value){
        console.log(value);
        this.$emit("ChangeFormDataEn",value);
    },
  },
}
</script>


<style>
h3{
  color: #597163;
}

</style>