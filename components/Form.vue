<template>
  <div class="container mx-auto">
    <form
      class="p-16 mx-auto flex flex-col justify-center bg-lime-300 w-2/6 mt-7 rounded-lg"
    >
      <div class="flex flex-col gap-2">
        <label class="text-xl font-semibold"> No Induk Siswa </label>
        <input
          type="text"
          class="focus:border border-black rounded"
          placeholder=" 2044212"
        />
      </div>
      <div class="flex flex-col gap-2">
        <label class="text-xl font-semibold"> Nama Siswa </label>
        <input
          type="text"
          class="focus:border border-black rounded"
          placeholder=" udin"
        />
      </div>
      <div class="flex flex-col gap-2">
        <label class="text-xl font-semibold"> Nilai Tugas </label>
        <input
          type="text"
          class="focus:border border-black rounded"
          placeholder=" 100"
        />
      </div>
      <button
        class="bg-lime-600 mt-7 p-2 rounded text-lg font-bold active:bg-lime-400 text-stone-100"
      >
        Submit
      </button>
    </form>
  </div>
</template>
<script>
export default {
  name: "form-input",
};
</script>
