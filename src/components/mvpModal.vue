<template>
  <v-row justify="center" class="btn-open">
    <v-dialog
      v-model="dialog"
      persistent
      max-width="600px"
    >
      <template v-slot:activator="{ on, attrs }">
        <v-btn
          color="black"
          dark
          v-bind="attrs"
          v-on="on"
          
        >
          Abrir Modal
        </v-btn>
      </template>
      <v-card class="modal-opened">
        <v-card-title>
          <span class="text-h5">Informe o perfil proprietário da marca</span>
          <small>Você precisa adicionar no mínimo um perfil proprietário</small>
        </v-card-title>
        <v-card-text>
          <v-container>
            <v-row>
              <v-col cols="12">
                <v-text-field
                  label="Digite ou cole o perfil ou nome da marca"
                  required
                  id="text-field"
                ></v-text-field>
              </v-col>
            </v-row>
          </v-container>
        </v-card-text>
        <v-card-actions>
          <v-spacer></v-spacer>
          <v-btn
            color="white"
            text
            @click="dialog = false"
          >
            Cancelar
          </v-btn>
          <v-btn
            color="white"
            text
            @click="dialog = false"
          >
            Confirmar
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
  </v-row>
</template>

<script>
  export default {
    data: () => ({
      dialog: false,
    }),
  }
</script>

<style>
.btn-open {
    padding-top: 5%;
  }
.modal-opened{
  background-color: #333333 !important;
}
#text-field, .modal-opened{
  color: #fff !important;
}
</style>