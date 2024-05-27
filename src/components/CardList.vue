<template>
    <div class="q-pa-md">
      <div class="row q-col-gutter-md">
        <div class="col-12 text-h5 q-mb-md">FEATURED PRODUCT</div>
        <div class="col-6 col-md-3 col-sm-6" v-for="product in featuredProducts" :key="product.id">
          <q-card class="cursor-pointer" @click="navigateToProduct(product.slug)">
            <q-img
              :src="product.image"
              spinner-color="primary"
              spinner-size="82px"
              class="rounded-borders"
              style="height: 200px"
            />
            <q-card-section>
              <div class="text-subtitle1 text-weight-bold">{{ product.name }}</div>
              <div class="text-caption text-grey">{{ product.category }}</div>
              <div class="text-subtitle2 text-weight-bold q-mt-sm">Rp{{ product.price.toLocaleString() }}</div>
            </q-card-section>
          </q-card>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        featuredProducts: [
          {
            id: 1,
            name: 'LENOVO THINKPAD P53 WORKSTATION GAMING',
            slug: 'produk-1',
            category: 'Laptop with the latest graphics card and high refresh rate screen for an immersive gaming experience. No more lag or frame drops!',
            price: 49000000,
            image: 'https://i.pinimg.com/564x/8c/56/c9/8c56c917b74d8211327b7bc918644ee4.jpg' // Memperbarui URL gambar untuk produk pertama
          },
          {
            id: 2,
            name: 'ASUS ROG GL552',
            slug: 'produk-2',
            category: 'This laptop comes with an elegant design and high quality materials. Equipped with security features and great battery life.',
            price: 33000000,
            image: 'https://i.pinimg.com/564x/fc/ba/e5/fcbae5e02653dba533d39dfd3b891a28.jpg' // Memperbarui URL gambar untuk produk kedua
          },
          {
            id: 3,
            name: 'ASUS ROG STRIX',
            slug: 'produk-3',
            category: 'Enjoy speed and efficiency with the latest processors and large storage capacities. Perfect for multitasking and unlimited creativity.',
            price: 38000000,
            image: 'https://i.pinimg.com/564x/c9/85/97/c9859714f6d488ec3b7a3489e9294d99.jpg' // Memperbarui URL gambar untuk produk ketiga
          },
          {
            id: 4,
            name: 'ROG ZEPHYRUS DUO G15',
            slug: 'produk-4',
            category: 'The brain of this laptop is AMD Ryzen which can be selected up to AMD Ryzen 9 5900HX combined with GeForce RTX up to the 3080 series.',
            price: 58000000,
            image: 'https://i.pinimg.com/564x/d2/30/e7/d230e7f0bd6ca83fe5df5dc6f552dab4.jpg' // Memperbarui URL gambar untuk produk keempat
          }
        ]
      }
    },
    methods: {
      navigateToProduct(slug) {
        // tambahkan logika untuk navigasi ke halaman produk
        console.log(`Navigasi ke produk ${slug}`)
      }
    }
  }
</script>