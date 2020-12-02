<template>
   <v-app>
       <div>
            <v-app-bar
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
                            v-for="item in items"
                            :key="item.title"
                            link
                            nuxt
                            :to="item.link"
                            >
                            <v-list-item-title>
                                {{item.title}}
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
       </div>
       <nuxt-child/>
       <v-footer
       app
       >
           <v-card>
           </v-card>
           {{ new Date().getFullYear() }} — <strong>SMA Pangudi Luhur Jogja</strong>
       </v-footer>
   </v-app>
</template>
<script>
  export default {
    data: () => ({
      btns: [
        ['Removed', '0'],
        ['Large', 'lg'],
        ['Custom', 'b-xl'],
      ],
      items: [
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
    }),
  }
</script>