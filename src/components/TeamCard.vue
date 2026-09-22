<!-- <script setup>
defineProps(['nama', 'jabatan', 'foto'])
</script>

<template>
  <div class="team-card">
    <div class="avatar">
      <img v-if="foto" :src="foto" :alt="nama" />
      <span v-else>{{ nama.charAt(0) }}</span>
    </div>
    <h3>{{ nama }}</h3>
    <p>{{ jabatan }}</p>
  </div>
</template>

<style scoped>
.avatar {
  width: 80px;
  height: 80px;
  border-radius: 50%;
  overflow: hidden;
  display: flex;
  align-items: center;
  justify-content: center;
  /* warna background & font sesuaikan sendiri */
}
.avatar img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
</style> -->

<script setup>
// Menerima data dari luar (dari AboutPage.vue) lewat props
// Pola ini sama seperti yang dipakai di ProductCard.vue
defineProps({
  nama: {
    type: String,
    required: true
  },
  jabatan: {
    type: String,
    required: true
  },
  foto: {
    type: String,
    default: '' // kalau tidak ada foto, kita tampilkan inisial
  }
})

// Fungsi kecil untuk mengambil inisial dari nama, dipakai kalau foto kosong
function ambilInisial(nama) {
  return nama
    .split(' ')
    .map(kata => kata.charAt(0))
    .join('')
    .toUpperCase()
    .slice(0, 2)
}
</script>

<template>
  <div class="team-card">
    <img
      v-if="foto"
      :src="foto"
      :alt="nama"
      class="team-card__avatar"
    />
    <div v-else class="team-card__avatar team-card__avatar--inisial">
      {{ ambilInisial(nama) }}
    </div>

    <h3 class="team-card__nama">{{ nama }}</h3>
    <p class="team-card__jabatan">{{ jabatan }}</p>
  </div>
</template>

<style scoped>
.team-card {
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
  padding: 20px;
  border-radius: 12px;
  background-color: white;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.08);
}

.team-card__avatar {
  width: 90px;
  height: 90px;
  border-radius: 50%; /* supaya bulat */
  object-fit: cover;
  margin-bottom: 12px;
}

.team-card__avatar--inisial {
  display: flex;
  align-items: center;
  justify-content: center;
  background-color: #f3eef5fa; /* sesuaikan dengan warna tema toko */
  color: #ae8dbb;
  font-weight: bold;
  font-size: 1.4rem;
}
/* #340041fa */
.team-card__nama {
  margin: 0;
  font-size: 1.05rem;
  color: plum;
}

.team-card__jabatan {
  margin: 4px 0 0;
  font-size: 0.9rem;
  color: #000000;
}
</style>