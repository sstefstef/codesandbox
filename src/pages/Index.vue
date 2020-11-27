<template>
  <q-page class="flex flex-center">
    <!-- <img alt="Quasar logo" src="~assets/quasar-logo-full.svg" /> a -->

    <q-card class="backgroundColor">
      <q-card-section> </q-card-section>
    </q-card>

    <q-card class="timeDate">
      <q-card-section> </q-card-section>
    </q-card>

    <q-card class="backgroundDash">
      <q-card-section>
        <q-card class="analise">
          <q-card-section> </q-card-section>
        </q-card>
      </q-card-section>
      <q-card class="consumoGeral">
        <q-card-section> </q-card-section>
      </q-card>
      <q-card class="maquina1">
        <q-card-section> </q-card-section>
      </q-card>
      <q-card class="maquina2">
        <q-card-section> </q-card-section>
      </q-card>
      <q-card class="maquina3">
        <q-card-section> </q-card-section>
      </q-card>
      <q-card class="LeftBar">
        <q-card-section> </q-card-section>
      </q-card>
    </q-card>

    <!-- <q-card
      v-if="showCard"
      class="my-card text-white"
      style="background: radial-gradient(circle, #35a2ff 0%, #014a88 100%)"
    >
      <q-card-section>
        <div class="text-h6">Rubinho Lindo</div>
        <div class="text-subtitle2">by Matheus do pop</div>
      </q-card-section>

      <q-card-section class="q-pt-none">
        <q-btn @click="submit"> Enviar </q-btn>
      </q-card-section>
    </q-card> -->
    <!-- 
    <q-card v-else> novo card </q-card> -->
  </q-page>
</template>

<script>
export default {
  data() {
    return {
      showCard: true,
      lorem:
        'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.',
      variavelnova: 0,
      variavelnova2: 0,
      variavelnova3: 0
    }
  },
  methods: {
    submit() {
      this.showCard = false
      console.log('Enviado')
    },
    createText() {
      this.lorem = 'teste 1'
      // this.variavelnova
      return 'texto para teste'
    }
  },
  mounted() {
    this.createText()
  }
}
</script>


