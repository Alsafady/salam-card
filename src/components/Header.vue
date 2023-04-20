<template>
  <nav class="navbar navbar-custom">
    <!-- <div> Test</div> -->
    <div class="container-fluid justify-content-center">
      <div class="navbar-brand" href="#">
        <!--<span id="page-title" class="pt-5" >{{title}}</span>-->
        <img src="https://cdn.jsdelivr.net/gh/Alsafady/salam-card@main/src/assets/logo.png" height="100" class="d-inline-block pt-n5" />
      </div>
    </div>
  </nav>
</template>
<script>
export default {
  name: 'Header',
  props: {
    title: String,
  },
};
</script>

<style>
.navbar-custom {
  background-color: #597163;
  border-top: 5px solid #a56433;
  color: #fff !important;
}

#page-title {
  color: #d1ccbd;
}
</style>
