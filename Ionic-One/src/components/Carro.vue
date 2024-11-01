<template>
    <ion-page>
      <ion-header>
        <ion-toolbar>
          <ion-title>Registro de Parqueadero</ion-title>
        </ion-toolbar>
      </ion-header>
  
      <ion-content :fullscreen="true">
        <ion-card>
          <ion-card-header>
            <ion-card-title>Formulario de Registro</ion-card-title>
          </ion-card-header>
  
          <ion-card-content>
            <!-- Nombre del propietario -->
            <ion-item class="input-item">
              <ion-label position="floating">Nombre del Propietario</ion-label>
              <ion-input v-model="formData.nombrePropietario" clear-input></ion-input>
            </ion-item>
  
            <!-- Número de placa -->
            <ion-item class="input-item">
              <ion-label position="floating">Número de Placa</ion-label>
              <ion-input v-model="formData.numeroPlaca" clear-input></ion-input>
            </ion-item>
  
            <!-- Tipo de vehículo -->
            <ion-item class="input-item">
              <ion-label>Tipo de Vehículo</ion-label>
              <ion-select v-model="formData.tipoVehiculo" ok-text="Aceptar" cancel-text="Cancelar">
                <ion-select-option value="automovil">Automóvil</ion-select-option>
                <ion-select-option value="moto">Moto</ion-select-option>
                <ion-select-option value="camioneta">Camioneta</ion-select-option>
              </ion-select>
            </ion-item>
  
            <!-- Número de parqueadero -->
            <ion-item class="input-item">
              <ion-label position="floating">Número de Parqueadero</ion-label>
              <ion-input v-model="formData.numeroParqueadero" type="number" clear-input></ion-input>
            </ion-item>
  
            <!-- Hora de entrada -->
            <ion-item class="input-item">
              <ion-label position="floating">Hora de Entrada</ion-label>
              <ion-datetime 
                v-model="formData.horaEntrada" 
                display-format="HH:mm" 
                picker-format="HH:mm"
              ></ion-datetime>
            </ion-item>
  
            <!-- Hora de salida -->
            <ion-item class="input-item">
              <ion-label position="floating">Hora de Salida</ion-label>
              <ion-datetime 
                v-model="formData.horaSalida" 
                display-format="HH:mm" 
                picker-format="HH:mm"
              ></ion-datetime>
            </ion-item>
  
            <!-- Pago -->
            <ion-item class="input-item">
              <ion-label position="floating">Valor del Pago</ion-label>
              <ion-input v-model="formData.valorPago" type="number" clear-input></ion-input>
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
  
            <!-- Botón de Envío -->
            <ion-button expand="block" @click="handleSubmit" class="submit-button">
              Enviar
            </ion-button>
          </ion-card-content>
        </ion-card>
      </ion-content>
    </ion-page>
  </template>
  
  <script>
  import { IonPage, IonHeader, IonToolbar, IonTitle, IonContent, IonCard, IonCardHeader, IonCardTitle, IonCardContent, IonItem, IonLabel, IonInput, IonSelect, IonSelectOption, IonDatetime, IonSegment, IonSegmentButton, IonButton } from '@ionic/vue';
  
  export default {
    name: 'RegistroParqueadero',
    components: {
      IonPage,
      IonHeader,
      IonToolbar,
      IonTitle,
      IonContent,
      IonCard,
      IonCardHeader,
      IonCardTitle,
      IonCardContent,
      IonItem,
      IonLabel,
      IonInput,
      IonSelect,
      IonSelectOption,
      IonDatetime,
      IonSegment,
      IonSegmentButton,
      IonButton
    },
    data() {
      return {
        formData: {
          nombrePropietario: '',
          numeroPlaca: '',
          tipoVehiculo: '',
          numeroParqueadero: '',
          horaEntrada: '',
          horaSalida: '',
          valorPago: '',
          pagoRealizado: ''
        }
      }
    },
    methods: {
      handleSubmit() {
        // Lógica para enviar el formulario
        console.log('Formulario enviado:', this.formData);
        alert('Formulario de registro de parqueadero enviado correctamente.');
      }
    }
  }
  </script>
  
  <style scoped>
  ion-card {
    margin: 16px;
  }
  
  .input-item {
    margin-bottom: 20px;
  }
  
  .submit-button {
    margin-top: 20px;
  }
  </style>
  