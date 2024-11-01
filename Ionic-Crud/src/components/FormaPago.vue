<template>
    <div>
      <!-- Forma de pago -->
      <ion-item class="input-item">
        <ion-label>Forma de Pago</ion-label>
        <ion-select v-model="formData.formaPago" ok-text="Aceptar" cancel-text="Cancelar">
          <ion-select-option value="efectivo">Efectivo</ion-select-option>
          <ion-select-option value="tarjeta_credito">Tarjeta de Crédito</ion-select-option>
          <ion-select-option value="tarjeta_debito">Tarjeta de Débito</ion-select-option>
          <ion-select-option value="consignacion">Consignación</ion-select-option>
        </ion-select>
      </ion-item>
  
      <!-- Pago realizado -->
      <ion-item class="input-item">
        <ion-label>Pago Realizado</ion-label>
        <ion-segment v-model="formData.pagoRealizado">
          <ion-segment-button value="si">
            <ion-label>Sí</ion-label>
          </ion-segment-button>
          <ion-segment-button value="no">
            <ion-label>No</ion-label>
          </ion-segment-button>
        </ion-segment>
      </ion-item>
    </div>
  </template>
  
  <script>
  export default {
    props: ['formData']
  };
  </script>

  <style scoped>
  
    ion-label {
      font-size: 22px;
      color: #000;
      font-weight: bold;
    }
    </style>