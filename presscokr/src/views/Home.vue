<template>
  <v-container
    fill-height
    grid-list-xl
    py-5
  >
    <v-layout
      align-content-center
      justify-center
      wrap
    >
      <v-flex
        v-for="(theme, i) in themes"
        :key="i"
        xs12
        md6
        py-5
      >
        <v-hover>
          <v-card
            slot-scope="{ hover }"
            flat
            color="transparent"
            class="d-block mx-auto"
            :href="theme.href"
            target="_blank"
            max-width="450"
            rel="noopener"
            :title="`WEB Kit - ${theme.name} `"
          >
            <div
              class="headline mb-3 text-uppercase"
              v-text="theme.name"
            />
            <v-img
              :aspect-ratio="16/9"
              :src="require('@/assets/' + theme.img + '.png')"
              height="300"
              :class="`elevation-${hover ? 24 : 4}`"
              class="transition-swing"
            >
              <v-fade-transition>
                <v-sheet
                  v-if="hover"
                  color="primary"
                  style="opacity: .12"
                  height="100%"
                  width="100%"
                />
              </v-fade-transition>
            </v-img>
            <div
              class="mt-3"
              v-text="theme.desc"
            />
          </v-card>
        </v-hover>
      </v-flex>
    </v-layout>
  </v-container>
</template>
<script>
export default {
  metaInfo () {
    return {
      title: "PRESSCO - 소프트웨어를 만들다",  /* this.$i18n.t('Home.title') */
      meta: [
        { name: 'description', content:  'PRESSCO is about connecting in your field of interest. Our vision is to help people share their knowledge, work, projects, papers and ideas and build their network through what they do rather where they live, study or work.'},
        { property: 'og:title', content: "PRESSCO - Build your software in your field of interest"},
        { property: 'og:site_name', content: 'Pressco'},
        { property: 'og:type', content: 'website'},    
        { name: 'robots', content: 'index,follow'} 
      ]
    }
  },
  data: () => ({
    themes: [
      {
        name: 'Coin KIT',
        desc: '암호화폐/거래소/Dapp',
        img: 'bitcoin',
        href: 'http://bitcoin.pressco.kr'
      },
      {
        name: 'Trading KIT',
        desc: '암호화폐 자동트레이딩',
        img: 'trading',
        href: 'http://trading.pressco.kr'
      },
      {
        name: 'Affiliate KIT',
        desc: '제휴사이트 링크',
        img: 'affiliate',
        href: 'http://amazon.pressco.kr'
      },
      {
        name: 'Video KIT',
        desc: '각종 동영상 홈페이지 제작 ',
        img: 'video',
        href: 'http://video.pressco.kr'
      },
      {
        name: 'Naver Keyword Search Tool KIT',
        desc: '네이버 스마트스토어 키워드 툴',
        img: 'navertool',
        href: 'http://naver.pressco.kr'
      },
      {
        name: 'PRESSCO KIT',
        desc: '웹서비스솔루션 KIT제작 및 커스터마이징, 앱/응용프로그램 개발',
        img: 'pressco',
        href: 'http://shop.pressco.kr'
      }
    ]
  })
}
</script>