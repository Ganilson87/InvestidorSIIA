<style>
.BarraModalInvestir {
  background: #0b5ed7;
  color: #fff;
}

/* Responsive table styles */
.responsiveTable {
  border-collapse: collapse;
  margin: 0;
  padding: 0;
  width: 100%;
  table-layout: fixed;
}

.responsiveTable caption {
  font-size: 1rem;
  /* margin: 0.5rem 0 0.75rem; */
}

.responsiveTable tr {
  border-bottom: 1px solid #d1d1d161;
  /* padding: 0.5rem; */
}

.responsiveTable th,
.responsiveTable td {
  /* padding: 0.625rem; */
  text-align: left;
}

.responsiveTable th {
  font-size: 1rem;
  font-weight: 700;
  border-bottom: 2px solid #8f8f8f6e;
}

@media screen and (max-width: 999px) {

  .responsiveTable {
    border: 0;
  }


  .responsiveTable caption {
    font-size: 1rem;
  }

  .responsiveTable thead {
    clip: rect(0 0 0 0);
    height: 1px;
    margin: -1px;
    overflow: hidden;
    padding: 0;
    position: absolute;
    width: 1px;
  }

  .responsiveTable tr {
    border-bottom: 3px solid #ddd;
    display: block;
    margin-bottom: 0.625rem;
    padding: 0;
  }

  .responsiveTable td {
    border-bottom: 1px solid #ddd;
    display: block;
    font-size: 1rem;
    text-align: right;
  }

  .responsiveTable td::before {
    /*************************************************************************
      ** aria-label has no advantage, it won't be read inside a .responsiveTable
      content: attr(aria-label);================================================
      **************************************************************************/
    content: attr(data-label);
    float: left;
    font-weight: 700;
    text-transform: uppercase;
    font-size: 0.9rem;
  }

  .responsiveTable td:last-child {
    border-bottom: 0;
  }
}
</style>

<template>
  <v-row justify="center">
    <v-dialog v-model="dialog" persistent width="1024">
      <template v-slot:activator="{ props }">
        <v-btn v-bind="props">
          Abrir
        </v-btn>
      </template>
      <v-card>
        <v-card-title class="BarraModalInvestir">
          <span class="text-h5 text-white">Investir na Fazenda</span>
        </v-card-title>
        <v-card-text>
          <v-container>
            <v-row>
              <v-col cols="12" sm="6" md="4">
                <v-text-field label="Legal first name*" required></v-text-field>
              </v-col>
              <v-col cols="12" sm="6" md="4">
                <v-text-field label="Legal middle name" hint="example of helper text only on focus"></v-text-field>
              </v-col>
              <v-col cols="12" sm="6" md="4">
                <v-text-field label="Legal last name*" hint="example of persistent helper text" persistent-hint
                  required></v-text-field>
              </v-col>
              <v-col cols="12">
                <v-text-field label="Email*" required></v-text-field>
              </v-col>
              <v-col cols="12">
                <v-text-field label="Password*" type="password" required></v-text-field>
              </v-col>
              <v-col cols="12" sm="6">
                <v-select :items="['0-17', '18-29', '30-54', '54+']" label="Age*" required></v-select>
              </v-col>
              <v-col cols="12" sm="6">
                <v-autocomplete
                  :items="['Skiing', 'Ice hockey', 'Soccer', 'Basketball', 'Hockey', 'Reading', 'Writing', 'Coding', 'Basejump']"
                  label="Interests" multiple></v-autocomplete>
              </v-col>
            </v-row>
          </v-container>
        </v-card-text>
        <v-card-actions>
          <v-spacer></v-spacer>
          <v-btn color="blue-darken-1" variant="text" @click="dialog = false">
            Fechar
          </v-btn>
          <v-btn color="blue-darken-1" variant="text" @click="dialog = false">
            Finalizar
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