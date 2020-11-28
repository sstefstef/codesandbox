<template>
  <q-page class="flex flex-center backgroundColor">
    <!-- <img alt="Quasar logo" src="~assets/quasar-logo-full.svg" /> a -->

    <div class="backgroundDash">
      <q-card-section>
        <q-card class="analise">
          <q-card-section>
            <h4 class="analise-text">Análise de Consumo</h4>
          </q-card-section>
          <img class="fror" src="~assets/prantinha.svg" />
        </q-card>
      </q-card-section>
      <q-card class="consumoGeral">
        <q-card-section> </q-card-section>
      </q-card>
      <q-card class="grafico1">
        <q-card-section> </q-card-section>
      </q-card>
      <q-card class="grafico2">
        <q-card-section> </q-card-section>
      </q-card>
      <q-card class="quantitativa">
        <q-card-section> </q-card-section>
      </q-card>
      <q-card class="LeftBar">
        <q-card-section>
          <div class="column justify-evenly">
            <img
              class="logo q-mb-xl"
              src="~assets/home.svg"
              @click="funcaoClick"
            />
            <img
              class="logo q-my-xl"
              src="~assets/pie-chart.svg"
              @click="funcaoClick"
            />
            <img
              class="logo q-my-xl"
              src="~assets/profile.svg"
              @click="funcaoClick"
            />
            <img
              class="logo q-my-xl"
              src="~assets/chat.svg"
              @click="funcaoClick"
            />
            <img
              class="logo q-my-xl"
              src="~assets/settings.svg"
              @click="funcaoClick"
            />
            <img
              class="logo q-my-xl"
              src="~assets/logout.svg"
              @click="funcaoClick"
            />
          </div>
        </q-card-section>
      </q-card>
    </div>

    <q-card class="timeDate">
      <q-card-section>
        <p class="todayDate">
          {{ hourAndDate }}
          <br />
          <br />
          {{ dayOfTheWeek }}
        </p>
      </q-card-section>
    </q-card>

    <q-btn text-color="white" class="maquina1" label="Máquina 1" />

    <q-btn text-color="white" class="maquina2" label="Máquina 2" />

    <q-btn text-color="white" class="maquina3" label="Máquina 3" />

    <q-btn text-color="white" class="maquina4" label="Máquina 4" />

    <q-btn text-color="white" class="maquina5" label="Máquina 5" />

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
      hourAndDate: null,
      dayOfTheWeek: null
    }
  },
  methods: {
    getDate() {
      var days = [
        'Sunday',
        'Monday',
        'Tuesday',
        'Wednesday',
        'Thursday',
        'Friday',
        'Saturday'
      ]

      var data = new Date()
      var hour = data.getHours()
      var minutes = data.getMinutes()
      var dayOfTheWeek = days[data.getDay()]
      // return `${hour} - ${dayOfTheWeek}`

      this.hourAndDate = `${hour}:${minutes}`
      this.dayOfTheWeek = dayOfTheWeek
    },
    funcaoClick() {
      console.log('Me apertaram!!')
    },
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
    this.getDate()
  }
}
</script>


