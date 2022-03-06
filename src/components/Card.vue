<template>
  <Container class="max-w-md">
    <Box class="p-4">
    <slot></slot>
    </Box>
  </Container>
</template>
<script>
import Container from "./UI/Container.vue";
import Box from "./UI/Box.vue";
export default {
  name: "Card",
  components: { Container, Box },
};
</script>