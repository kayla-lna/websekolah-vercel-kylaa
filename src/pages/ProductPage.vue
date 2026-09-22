

<script setup>
import ProductCard from '../components/ProductCard.vue'
const daftarProduk = [
 { id: 1, nama: 'Red Beaded Mermaid Evening Gown with Feather Shawl ', harga: 25000000, gambar:
'https://i.pinimg.com/736x/6c/27/8d/6c278d9818d97878362da10a9473d38e.jpg' },
 { id: 2, nama: 'Luxury Burgundy Tulle Ball Gown with Corset Bodice', harga: 50000000, gambar:
'https://i.pinimg.com/736x/03/6e/64/036e64a50b3db39328a9d9cd75a6fecc.jpg' },
 { id: 3, nama: 'Luxury Strapless Satin Wedding Dress', harga: 67000000, gambar:
'https://i.pinimg.com/736x/cf/8e/64/cf8e64a557c934d4e36e37fdcf57cc35.jpg' },
{ id: 4, nama: 'Off Shoulder Satin Wedding Dress', harga: 98000000, gambar:
'https://i.pinimg.com/736x/6f/e0/dc/6fe0dc1aefae425a0dec3bcddd16e78c.jpg' },
{ id: 5, nama: 'Luxury Sculpted Strapless Wedding Gown', harga: 73000000, gambar:
'https://i.pinimg.com/1200x/bc/39/a9/bc39a99096500ca7c1b6b7be7050f50c.jpg' },
{ id: 6, nama: 'Off Shoulder Mermaid Wedding Dress', harga: 29000000, gambar:
'https://i.pinimg.com/736x/d5/19/bc/d519bc56e26dc0de9190d0834c79b888.jpg' },
{ id: 7, nama: 'Elegant White Floral Cocktail Dress', harga: 20000000, gambar:
'https://i.pinimg.com/736x/4f/f6/33/4ff63376400136ee48fdb9133a2e184b.jpg' },
{ id: 8, nama: 'Blue and White Floral Ruffle Gown', harga: 35000000, gambar:
'https://i.pinimg.com/736x/54/27/00/54270066287f051106f7407c372c9338.jpg' },
{ id: 9, nama: 'Royal White Evening Gown', harga: 80000000, gambar:
'https://i.pinimg.com/736x/88/00/0c/88000c2b75469180d2a14587b1b1dc09.jpg' },
{ id: 10, nama: 'wedding gown', harga: 29000000, gambar:
'https://i.pinimg.com/736x/7a/f9/5e/7af95e606a2d1f55b5bad56cac82b080.jpg' },
{ id: 11, nama: 'DresMidnight Blue & White Princess Ball Gown ', harga:90000000, gambar:
'https://i.pinimg.com/736x/c7/85/df/c785dfb193a8aa0e54c7e1b93b7b210f.jpg' },
{ id: 12, nama: 'Sparkling Ice Princess Couture Gown', harga: 78000000, gambar:
'https://i.pinimg.com/736x/f7/18/64/f71864049fec89ac649a1e0490987329.jpg' },

]
</script>
<template>
    <main>
        <h1>Produk Kami</h1>
        <div class="grid">
            <ProductCard
 v-for="produk in daftarProduk"
 :key="produk.id"
 :nama="produk.nama"
 :harga="produk.harga"
 :gambar="produk.gambar"
 />
 </div>
 </main>
</template>
<style scoped>
main {
 display: flex;
 flex-direction: column;
 align-items: center;
 padding: 20px;
}

.grid {
 display: grid;
 grid-template-columns: repeat(4, minmax(260px, 1fr));
 gap: 24px;
 justify-items: center;
 justify-content: center;
 max-width: 1300px;
 width: 100%;
}
</style>