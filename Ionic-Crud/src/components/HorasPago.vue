<template>
    <div>
      <!-- Hora de entrada -->
      <ion-item class="input-item">
        <ion-label position="stacked">Hora de Entrada</ion-label>
        <ion-datetime
          v-model="formData.horaEntrada"
          display-format="HH:mm"
          picker-format="HH:mm"
          class="datetime-center"
        ></ion-datetime>
      </ion-item>
  
      <!-- Hora de salida -->
      <ion-item class="input-item">
        <ion-label position="stacked">Hora de Salida</ion-label>
        <ion-datetime
          v-model="formData.horaSalida"
          display-format="HH:mm"
          picker-format="HH:mm"
          class="datetime-center"
        ></ion-datetime>
      </ion-item>
  
      <!-- Valor del Pago -->
      <ion-item class="input-item">
        <ion-label position="stacked">Valor del Pago</ion-label>
        <ion-input v-model="formData.valorPago" type="number" clear-input></ion-input>
      </ion-item>
    </div>
  </template>
  
  <script>
  export default {
    props: ['formData']
  };
  </script>

<style scoped>
  .datetime-center {
    display: block;
    margin: 0 auto;
  }
  ion-input {
      font-size: 22px;
      color: #f70404;
      font-weight: bold;
    }
  </style>