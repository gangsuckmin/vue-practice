<!-- ParentComponent.vue -->
<template>
  <div>
    <ChildComponent
        :message="parentMessage"
        @custom-event="handleEvent"/>
  </div>
</template>

<script>
import ChildComponent from './ChildComponent.vue';

export default {
  name: "E05ParentComponent",
  data() {
    return {
      parentMessage: 'Hello from parent'
    };
  },
  methods: {
    handleEvent(data) {
      console.log(data);
    }
  },
  components: {
    ChildComponent
  }
};
</script>
