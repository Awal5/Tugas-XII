<script>
export default {
  name: "form-input",
  data() {
    return {
      form: {
        nis: "",
        name: "",
        grade: "",
      },
    };
  },
  methods: {
    handlesubmit() {
      this.$emit("infoSiswa", this.form);

      this.form = {
        nis: "",
        name: "",
        grade: "",
      };
    },
  },
};
</script>
<template>
  <div class="container mx-auto">
    <form
      class="form p-16 mx-auto flex flex-col justify-center bg-lime-300 w-2/6 mt-7 rounded-lg"
      @submit.prevent="handlesubmit"
    >
      <div class="flex flex-col gap-2">
        <label class="text-xl font-semibold"> No Induk Siswa </label>
        <input
          v-model="form.nis"
          type="text"
          class="focus:border border-black rounded"
          placeholder=" 2044212"
        />
      </div>
      <div class="flex flex-col gap-2">
        <label class="text-xl font-semibold"> Nama Siswa </label>
        <input
          v-model="form.name"
          type="text"
          class="focus:border border-black rounded"
          placeholder=" udin"
        />
      </div>
      <div class="flex flex-col gap-2">
        <label class="text-xl font-semibold"> Nilai Tugas </label>
        <input
          v-model="form.grade"
          type="text"
          class="focus:border border-black rounded"
          placeholder=" 100"
        />
      </div>
      <button
        type="submit"
        class="bg-lime-600 mt-7 p-2 rounded text-lg font-bold active:bg-lime-400 text-stone-100"
      >
        Submit
      </button>
    </form>
  </div>
</template>
