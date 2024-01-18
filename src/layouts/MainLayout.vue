<template>
  <q-layout view="hHh lpR fff" class="bg-primary">
    <q-header>
      <q-toolbar class="row justify-between">
        <q-toolbar-title class="q-ml-sm col-3 q-pa-sm">
          <q-img src="../assets/mrlogo3.png" width="20%" class="q-ma-md"></q-img>
        </q-toolbar-title>

        <q-tabs class="col-5" v-model="selected_tab" active-color="accent" indicator-color="transparent" shrink>
          <q-tab name="home" @click='onScroll("id_home")' label="Home" />
          <q-tab name="catalog" @click='onScroll("id_catalog")' label="Catálogo" />
          <q-tab name="aboutUs" @click='onScroll("id_aboutUs")' label="Sobre nós" />
          <q-tab name="deal" @click='onScroll("id_deal")' class="bg-accent" label="Faça um orçamento" style="border-radius: 20px;"/>
        </q-tabs>
      </q-toolbar>
    </q-header>
    <q-page-container>
      <div id="id_home" class="q-mb-xl">
        <q-img img-class="my-custom-image" height="700px" src="../assets/background.jpg">
          <div class="absolute-full text-subtitle column justify-start">
            <div class="text-h2 q-mt-xl q-ml-xl col col-sm-2">
              MENDES & ROSA
            </div>
            <div class="text-subtitle1 q-ml-xl col col-xs-3">
              Somos uma empresa familiar com sede em Lisboa,<br/>
              dedicada a cativar nossos clientes. Comprometemo-nos<br/>
              com um atendimento confiável, priorizando<br/>
              pontualidade, qualidade e máxima comodidade.<br/>
            </div>
            <div class="col-auto q-ml-xl">
              <q-btn color="accent" size="lg" label="FAÇA UM ORÇAMENTO" style="border-radius: 10px;" unelevated></q-btn>
            </div>
          </div>
        </q-img>
        <div class="q-mt-xl bg-primary">
          <div class="text-center text-h6 text-secondary">Por que escolher a Mendes & Rosa?</div>
          <div class="row justify-around q-mt-xl">
            <q-card flat bordered class="col-3 bg-secondary">
              <q-card-section class="row justify-center q-mt-xl">
                <q-img class="col-6" src="https://cdn.quasar.dev/img/material.png" style="border-radius: 30px;"/>
              </q-card-section>
              <q-card-section class="text-center">
                Lorem ipsum dolor sit amet, consectetur.
              </q-card-section>
            </q-card>
            <q-card flat bordered class="col-3 bg-secondary">
              <q-card-section class="row justify-center q-mt-xl">
                <q-img class="col-6" src="https://cdn.quasar.dev/img/material.png" style="border-radius: 30px;"/>
              </q-card-section>
              <q-card-section class="text-center">
                Lorem ipsum dolor sit amet, consectetur.
              </q-card-section>
            </q-card>
            <q-card flat bordered class="col-3 bg-secondary">
              <q-card-section class="row justify-center q-mt-xl">
                <q-img class="col-6" src="https://cdn.quasar.dev/img/material.png" style="border-radius: 30px;"/>
              </q-card-section>
              <q-card-section class="text-center">
                Lorem ipsum dolor sit amet, consectetur.
              </q-card-section>
            </q-card>
          </div>
        </div>
      </div>
      <div id="id_catalog" class="q-mt-xl q-pt-xl">
        <div class="q-mt-xl">
          <div class="row justify-between q-mx-md">
            <div class="text-left q-ml-xl text-h6 text-secondary">CONFIRA NOSSOS PRODUTOS</div>
            <div class="text-right q-mr-xl text-subtitle1 text-secondary">
              <q-btn
                class="bg-transparent text-secondary"
                label="ver tudo"
                :ripple="false"
                no-caps
                flat
              ></q-btn>
            </div>
          </div>
          <div class="row justify-center q-mt-md">
            <q-card flat bordered class="col-2 bg-secondary q-mx-sm">
              <q-card-section class="row justify-center q-mt-xl">
                <q-img class="col-6" src="https://cdn.quasar.dev/img/material.png" style="border-radius: 30px;"/>
              </q-card-section>
              <q-card-section class="text-center">
                <div class="text-subtitle1">Nome: </div>
                <div class="text-caption">Descrição </div>
              </q-card-section>
            </q-card>
            <q-card flat bordered class="col-2 bg-secondary q-mx-sm">
              <q-card-section class="row justify-center q-mt-xl">
                <q-img class="col-6" src="https://cdn.quasar.dev/img/material.png" style="border-radius: 30px;"/>
              </q-card-section>
              <q-card-section class="text-center">
                <div class="text-subtitle1">Nome: </div>
                <div class="text-caption">Descrição </div>
              </q-card-section>
            </q-card>
            <q-card flat bordered class="col-2 bg-secondary q-mx-sm">
              <q-card-section class="row justify-center q-mt-xl">
                <q-img class="col-6" src="https://cdn.quasar.dev/img/material.png" style="border-radius: 30px;"/>
              </q-card-section>
              <q-card-section class="text-center">
                <div class="text-subtitle1">Nome: </div>
                <div class="text-caption">Descrição </div>
              </q-card-section>
            </q-card>
            <q-card flat bordered class="col-2 bg-secondary q-mx-sm">
              <q-card-section class="row justify-center q-mt-xl">
                <q-img class="col-6" src="https://cdn.quasar.dev/img/material.png" style="border-radius: 30px;"/>
              </q-card-section>
              <q-card-section class="text-center">
                <div class="text-subtitle1">Nome: </div>
                <div class="text-caption">Descrição </div>
              </q-card-section>
            </q-card>
          </div>
          <div class="row justify-center q-mt-md">
            <q-card flat bordered class="col-2 bg-secondary q-mx-sm">
              <q-card-section class="row justify-center q-mt-xl">
                <q-img class="col-6" src="https://cdn.quasar.dev/img/material.png" style="border-radius: 30px;"/>
              </q-card-section>
              <q-card-section class="text-center">
                <div class="text-subtitle1">Nome: </div>
                <div class="text-caption">Descrição </div>
              </q-card-section>
            </q-card>
            <q-card flat bordered class="col-2 bg-secondary q-mx-sm">
              <q-card-section class="row justify-center q-mt-xl">
                <q-img class="col-6" src="https://cdn.quasar.dev/img/material.png" style="border-radius: 30px;"/>
              </q-card-section>
              <q-card-section class="text-center">
                <div class="text-subtitle1">Nome: </div>
                <div class="text-caption">Descrição </div>
              </q-card-section>
            </q-card>
            <q-card flat bordered class="col-2 bg-secondary q-mx-sm">
              <q-card-section class="row justify-center q-mt-xl">
                <q-img class="col-6" src="https://cdn.quasar.dev/img/material.png" style="border-radius: 30px;"/>
              </q-card-section>
              <q-card-section class="text-center">
                <div class="text-subtitle1">Nome: </div>
                <div class="text-caption">Descrição </div>
              </q-card-section>
            </q-card>
            <q-card flat bordered class="col-2 bg-secondary q-mx-sm">
              <q-card-section class="row justify-center q-mt-xl">
                <q-img class="col-6" src="https://cdn.quasar.dev/img/material.png" style="border-radius: 30px;"/>
              </q-card-section>
              <q-card-section class="text-center">
                <div class="text-subtitle1">Nome: </div>
                <div class="text-caption">Descrição </div>
              </q-card-section>
            </q-card>
          </div>
        </div>
      </div>
      <div id="id_aboutUs"></div>
      <div id="id_deal"></div>
    </q-page-container>
  </q-layout>
</template>

<script>
import { defineComponent } from 'vue'
import { scroll } from 'quasar'
import EssentialLink from 'components/EssentialLink.vue'
// const { getScrollTarget, setVerticalScrollPosition } = scroll

export default defineComponent({
  name: 'MainLayout',

  components: {
    EssentialLink,
    scroll
  },

  setup () {
    return {
      selected_tab: 'home',
      theme_color: 'rgb(184, 152, 33)',
    }
  },
  methods: {
    onScroll (id) {
      const target = scroll.getScrollTarget(id)
      const offset = 0
      const duration = 1000
      setVerticalScrollPosition(target, offset, duration)
    },
  }
})
</script>

<style lang="sass">
.my-custom-image
  filter: blur(5px)
</style>
