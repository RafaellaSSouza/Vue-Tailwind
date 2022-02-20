<template>
  <button class="btn" :type="type">
    <slot></slot>
    </button>
</template>
<script>
export default {
    name: "Button",
    props:["type"],

    methods(){
      
    }
}

</script>
<style lang="postcss" >
.btn {
  @apply 
    h-10 
    w-40 
    box-border
    rounded-md 
    font-semibold 
    inline-flex
    items-center
    justify-center
    bg-gray-200
}
</style>