<template>
  <button class="gap-2 btn" :class="context[variant]" @click="$emit('click')">
    <slot />
  </button>
</template>

<script>
  export default {
    name: "BaseButton",
    props: {
      variant: {
        validator: function (value) {
          return ["primary", "secondary", "outline", "ghost", "icon-ghost"].includes(value);
        },
      },
    },
    data() {
      return {
        context: {
          ["primary"]: "btn-primary text-neutral-100",
          ["secondary"]: "bg-neutral-100 text-neutral-900 hover:text-neutral-100",
          ["outline"]: "btn-outline text-primary hover:bg-primary hover:text-neutral-100 hover:border-primary",
          ["ghost"]: "btn-ghost text-neutral-900",
          ["icon-ghost"]:
            "btn-circle bg-transparent border-none text-secondary rounded-full hover:text-neutral-100 lg:hover:bg-neutral-100 lg:hover:text-neutral-900",
        },
      };
    },
  };
</script>

<style></style>
