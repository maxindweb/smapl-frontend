<template>
   <v-app>
       <div>
        <v-carousel
          height="100vh"
          hide-delimiters
          cycle
          
        >
            <v-app-bar
                fixed
                flat
                color=""
                dark
            >
                <v-toolbar-title
                class="font-weight-bold headline"
                >SMA Pangudi Luhur Jogja</v-toolbar-title>
                <v-spacer/>
                    <div>
                        <v-btn text nuxt to="/">Home</v-btn>
                        <v-btn text href="http://ppdb.smaplyk.sch.id">PPDB</v-btn>
                        <v-btn text href="http://elearning2.smaplyk.sch.id">E-Learning</v-btn>
                        <v-menu
                        offset-y
                        >
                        <template v-slot:activator="{ on, attrs }">
                            <v-btn
                            v-bind="attrs"
                            v-on="on"
                            >
                            PUBLIKASI
                            </v-btn>
                        </template>

                        <v-list>
                            <v-list-item
                            v-for="publik in publication"
                            :key="publik.title"
                            link
                            nuxt
                            :to="publik.link"
                            >
                            <v-list-item-title>
                                {{publik.title}}
                            </v-list-item-title>
                            </v-list-item>
                        </v-list>
                        </v-menu>
                        <v-menu
                        offset-y
                        >
                        <template v-slot:activator="{ on, attrs }">
                            <v-btn
                            v-bind="attrs"
                            v-on="on"
                            >
                            TENTANG KAMI
                            </v-btn>
                        </template>

                        <v-list>
                            <v-list-item
                            v-for="about in abouts"
                            :key="about.title"
                            link
                            nuxt
                            :to="about.link"
                            >
                            <v-list-item-title>
                                {{about.title}}
                            </v-list-item-title>
                            </v-list-item>
                        </v-list>
                        </v-menu>
                    </div>
            </v-app-bar>
            <v-carousel-item
                v-for="(item, i) in items"
                interval="5"
                :key="i"
                :src="item.src"            
            ></v-carousel-item>
        </v-carousel>
       </div>
       <nuxt-child/>
       <v-footer>
           <v-card>
           </v-card>
           {{ new Date().getFullYear() }} — <strong>SMA Pangudi Luhur Jogja</strong>
       </v-footer>
   </v-app>
</template>
<script>
export default {
    data() {
        return{
            items: [
                {
                    src: "gelar-budaya1.jpg"
                },
                {
                    src:  "gelar-budaya2.jpg"
                },
                {
                    src: "gelar-budaya3.jpg"
                },
            ],
            news: [
                {
                    title: "Kegiatan Sekolah"
                }
            ],
            publication: [
         {
             title: "BERITA DAN KEGIATAN",
             link : "news"
         },
         {
             title: "GALERI",
             link:  "galery"
         },
         {
             title: " MAJALAH PELITA",
             link : "pelita"
         }
      ],
      abouts: [
          {
              title : "VISI & MISI",
              link  : "visi-misi"
          },
          {
              title : "SEJARAH SEKOLAH",
              link  : "history"
          },
          {
              title : "NILAI-NILAI",
              link  : "/value"
          },
      ]
        }
    }
}
</script>