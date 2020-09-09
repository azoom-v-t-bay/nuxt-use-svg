<template>
  <div class="container mx-auto">
    <div class="p-10">
      <label>Use img tag</label>
      <img src="~/assets/icons/bell.svg" alt="" />
    </div>
    <div class="p-10">
      <label>Use object tag</label>
      <object
        :data="require('~/assets/icons/bell.svg')"
        type="image/svg+xml"
      ></object>
    </div>
    <div class="p-10">
      <label>Use svg tag</label>
      <svg class="icon-bell">
        <use xlink:href="~/assets/icons/bell.svg#bell"></use>
      </svg>
    </div>
    <div class="p-10">
      <label>Use symbol for performance</label>
      <svg>
        <use xlink:href="~/assets/icons/icons.svg#bell"></use>
      </svg>
      <svg>
        <use xlink:href="~/assets/icons/icons.svg#right"></use>
      </svg>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style>
.icon-bell {
  fill: red;
}
.icon-bell:hover {
  fill: green;
}
</style>
