<script>
export default {
  name: "student-list",
  props: {
    dataSiswa: {
      type: Array,
    },
  },
  computed: {
    calculateAverage() {
      if (this.dataSiswa.length === 0) return 0;
      const totalScore = this.dataSiswa.reduce((acc, item) => {
        return acc + parseInt(item.grade);
      }, 0);
      console.log(totalScore);
      const avg = totalScore / this.dataSiswa.length;
      return avg.toFixed(2);
    },
  },
};
</script>

<style>
.overflow-container {
  height: 300px;
  overflow-y: scroll;
}
</style>

<template>
  <div class="mt-10 container mx-auto">
    <div class="w-3/4 mx-auto">
      <p class="text-lg font-semibold">Jumlah Siswa: {{ dataSiswa.length }}</p>

      <div class="overflow-container">
        <table class="text-center mx-auto">
          <thead class="bg-lime-600 text-lg text-white">
            <tr>
              <th class="p-4">No</th>
              <th class="p-4">No Induk Siswa</th>
              <th class="p-4">Nama Siswa</th>
              <th class="p-4">Nilai Tugas</th>
            </tr>
          </thead>

          <tbody class="text-lg">
            <tr
              class="odd:bg-slate-200"
              v-for="(item, index) in dataSiswa"
              :key="index"
            >
              <td class="p-4">{{ index + 1 }}</td>
              <td class="p-4">{{ item.nis }}</td>
              <td class="p-4">{{ item.name }}</td>
              <td class="p-4">{{ item.grade }}</td>
            </tr>
          </tbody>
        </table>
      </div>
      <p class="text-lg font-semibold">
        Jumlah Rata-Rata Nilai: {{ calculateAverage }}
      </p>
    </div>
  </div>
</template>
