<script>
export default {
  name: "student-list",
};
</script>

<template>
  <div class="mt-10 container mx-auto">
    <div class="w-3/4 mx-auto">
      <div class="text-lg font-semibold">
        <p>Jumlah Data:</p>
        <p>Jumlah Rata-Rata Nilai:</p>
      </div>

      <table class="table-auto text-center mx-auto mt-10">
        <thead class="bg-lime-600 text-lg text-white">
          <tr class="">
            <th class="p-4">No Induk Siswa</th>
            <th class="p-4">Nama Siswa</th>
            <th class="p-4">Nilai Tugas</th>
          </tr>
        </thead>
        <tbody class="text-lg">
          <tr class="odd:bg-slate-200">
            <td class="p-4">2103410</td>
            <td class="p-4">Udin</td>
            <td class="p-4">100</td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>
