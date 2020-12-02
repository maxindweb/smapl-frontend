<template>
  <v-container>
    <!-- <v-row>
      <p class="display-1">Visi dan Misi</p>
    </v-row>
    <v-row>
      <hr style="width:15%" color="success">
    </v-row> -->
    <v-row>
      <p class="display-1">Berita</p>
    </v-row>
    <v-row>
      <hr style="width:7%" color="success"> 
    </v-row>
    <v-row pa-1>
      <v-col cols="4">
        <v-card>
          <v-img src="belajar.jpg"></v-img>
          <v-card-title nuxt to="/">
            Pelantikan Pengurus OSIS 20/21
          </v-card-title>
          <v-card-text>
            READ MORE....
          </v-card-text>
        </v-card>
      </v-col>
      <v-col cols="4">
        <v-card>
          <v-img src="belajar.jpg"></v-img>
          <v-card-title>
            SImulasi Pembelajaran new normal
          </v-card-title>
          <v-card-text>
            READ MORE....
          </v-card-text>
        </v-card>
      </v-col>
      <v-col cols="4">
        <v-card>
          <v-img src="belajar.jpg"></v-img>
          <v-card-title>
            SImulasi Pembelajaran new normal
          </v-card-title>
          <v-card-text>
            READ MORE....
          </v-card-text>
        </v-card>
      </v-col>
      <v-col>
        <v-btn rounded text color="success" nuxt to="/news">
          Lihat Berita Lainnya
        </v-btn>
      </v-col>
    </v-row>
    <v-row>
      <v-col>
        <p class="display-1">Sambutan Kepala Sekolah</p>
      </v-col>
    </v-row>
    <v-row>
      <hr style="width:32%" color="success"> 
    </v-row>
    <v-row>
      <v-card flat color="transparent">
        <v-row>
          <v-col cols="3">
          <v-img src="br-yo.jpg"></v-img>
        </v-col>
        <v-col cols="8">
          <v-card-text>
            Selamat datang di situs resmi SMA Pangudi Luhur St.Yusup Yogyakarta .

            Situs ini merupakan wujud dari kesungguhan kami untuk membangun komunikasi interaktifÂ  antara sekolah, siswa, orang tua, alumni dan masyarakat demi meningkatkan kualitas pendidikan di sekolah ini.

            Melalui situs SMA Pangudi Luhur St.Yusup Yogyakarta, kami hantarkan Anda untuk mengakses berita dan perkembangan apa yang sudah ada sesuai dengan visi SMA Pangudi Luhur St.Yusup Yogyakarta yaitu “Terbuka Menghadapi Tantangan Zaman”.
            <br> <br>
            Salam dan hormat kami,
          </v-card-text>
        </v-col>
        </v-row>
      </v-card>
    </v-row>
  </v-container>
</template>
<script>
export default {
  layout: 'home'
}
</script>
<style lang="scss">
  hr{
    height:         100;
    width:          1px;       
  }
</style>