<template>
  <div>
    <c-box :p="5" shadow="md" border-width="1px">
      <c-heading>Task</c-heading>
      <c-text :mt="4">Vue makes front-end development a breeze.</c-text>
    </c-box>
  </div>
</template>

<script>
import { CText, CHeading, CBox } from '@chakra-ui/vue'

export default {
  name: 'task-card',
  components: { CText, CHeading, CBox }
}
</script>
