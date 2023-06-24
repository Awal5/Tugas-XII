<script>
import FormInput from "./components/Form.vue";
import StudentList from "./components/StudentList.vue";

export default {
  components: {
    FormInput,
    StudentList,
  },
};
</script>

<template>
  <div class="lg:container mx-auto">
    <FormInput />
    <StudentList />
  </div>
</template>
