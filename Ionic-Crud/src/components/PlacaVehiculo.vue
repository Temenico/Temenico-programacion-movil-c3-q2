<template>
    <div>
      <!-- Número de placa -->
      <ion-item class="input-item">
        <ion-label position="stacked">Número de Placa</ion-label>
        <ion-input v-model="formData.numeroPlaca" clear-input></ion-input>
      </ion-item>
  
      <!-- Tipo de vehículo -->
      <ion-item class="input-item">
        <ion-label>Tipo de Vehículo</ion-label>
        <ion-select v-model="formData.tipoVehiculo" ok-text="Aceptar" cancel-text="Cancelar">
          <ion-select-option value="automóvil">Automóvil</ion-select-option>
          <ion-select-option value="moto">Moto</ion-select-option>
          <ion-select-option value="camioneta">Camioneta</ion-select-option>
          <ion-select-option value="otro">Otro</ion-select-option>
        </ion-select>
      </ion-item>
  
      <!-- Número de parqueadero -->
      <ion-item class="input-item">
        <ion-label position="stacked">Número de Parqueadero</ion-label>
        <ion-input v-model="formData.numeroParqueadero" type="number" clear-input></ion-input>
      </ion-item>
    </div>
  </template>
  
  <script>
  export default {
    props: ['formData']
  };
  </script>
  