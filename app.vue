<script>
import FormInput from "./components/Form.vue";
import StudentList from "./components/StudentList.vue";

export default {
  components: {
    FormInput,
    StudentList,
  },
  data() {
    return {
      dataSiswa: [],
    };
  },

  methods: {
    infoSiswaHandling(form) {
      this.dataSiswa.push(form);
    },
  },
};
</script>

<template>
  <div class="lg:container mx-auto">
    <FormInput @infoSiswa="infoSiswaHandling" />
    <StudentList :dataSiswa="dataSiswa" />
  </div>
</template>
