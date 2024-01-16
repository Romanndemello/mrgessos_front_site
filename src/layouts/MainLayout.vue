<template>
  <q-layout view="lHh Lpr lFf">
    <q-header>
      <q-toolbar class="row justify-between">
        <q-toolbar-title class="q-ml-sm col-3 q-pa-sm">
          <q-img src="../assets/mr_gessos_3d.jpeg" width="25%"></q-img>
        </q-toolbar-title>

        <q-tabs class="col-5" v-model="selected_tab" active-color="accent" indicator-color="transparent" shrink>
          <q-tab name="home" @click='onScroll("id_home")' label="Home" />
          <q-tab name="catalog" @click='onScroll("id_catalog")' label="Catálogo" />
          <q-tab name="aboutUs" @click='onScroll("id_aboutUs")' label="Sobre nós" />
          <q-tab name="deal" @click='onScroll("id_deal")' class="bg-accent" label="Faça um orçamento" style="border-radius: 20px;"/>
        </q-tabs>
        <!-- <q-icon class="col-2" name="fafacebook" size="lg"></q-icon> -->
      </q-toolbar>
    </q-header>
    <q-page-container>
      <div id="id_home">
        <q-img img-class="my-custom-image" src="../assets/background.jpg">
          <div class="absolute-full text-subtitle flex flex-start column justify-start">
            <div class="text-h1 q-mt-xl q-ml-xl col-2">
              MENDES & ROSA
            </div>
            <div class="text-subtitle1 q-ml-xl col-1">
              Somos uma empresa familiar com sede em Lisboa, dedicada a cativar nossos clientes.<br/>
              Comprometemo-nos com um atendimento confiável, priorizando pontualidade, qualidade e máxima comodidade.<br/>
              Destacamo-nos na concepção de painéis de gesso 3D, utilizando gesso cerâmico de alta durabilidade. <br/>
              Buscamos constantemente inovar, visando a plena satisfação dos nossos clientes em cada opção disponibilizada.<br/>
            </div>
            <div class="col-1 q-mt-lg q-ml-xl">
              <q-btn color="accent" label="FAÇA UM ORÇAMENTO"></q-btn>
            </div>
          </div>
        </q-img>
      </div>
      <div id="id_catalog"></div>
      <div id="id_aboutUs"></div>
      <div id="id_deal"></div>
    </q-page-container>
  </q-layout>
</template>

<script>
import { defineComponent } from 'vue'
import EssentialLink from 'components/EssentialLink.vue'

export default defineComponent({
  name: 'MainLayout',

  components: {
    EssentialLink,
  },

  setup () {
    return {
      selected_tab: 'home',
      theme_color: 'rgb(184, 152, 33)',
    }
  },
  methods: {
    onScroll (id) {
      console.log(id)
      const tabValue = id.split('_')
      this.selected_tab = tabValue[1]
      window.scrollTo({
        top: document.getElementById(`#${id}`),
        behavior: "smooth",
      })
    },
  }
})
</script>

<style lang="sass">
.my-custom-image
  filter: blur(5px)
</style>