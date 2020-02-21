<template>
  <v-app>
    <v-app-bar color="primary white--text" dense style="max-height: 50px;">
      <v-toolbar-title>Vuetify Datetime Picker</v-toolbar-title>

      <v-spacer />

      <v-btn text color="white" href="https://github.com/goldenm-software/vuetify-datetime-picker" target="_blank">
        <svg style="width: 20px; height: 20px; margin-right: 5px;" viewBox="0 0 24 24">
          <path fill="currentColor" d="M12,2A10,10 0 0,0 2,12C2,16.42 4.87,20.17 8.84,21.5C9.34,21.58 9.5,21.27 9.5,21C9.5,20.77 9.5,20.14 9.5,19.31C6.73,19.91 6.14,17.97 6.14,17.97C5.68,16.81 5.03,16.5 5.03,16.5C4.12,15.88 5.1,15.9 5.1,15.9C6.1,15.97 6.63,16.93 6.63,16.93C7.5,18.45 8.97,18 9.54,17.76C9.63,17.11 9.89,16.67 10.17,16.42C7.95,16.17 5.62,15.31 5.62,11.5C5.62,10.39 6,9.5 6.65,8.79C6.55,8.54 6.2,7.5 6.75,6.15C6.75,6.15 7.59,5.88 9.5,7.17C10.29,6.95 11.15,6.84 12,6.84C12.85,6.84 13.71,6.95 14.5,7.17C16.41,5.88 17.25,6.15 17.25,6.15C17.8,7.5 17.45,8.54 17.35,8.79C18,9.5 18.38,10.39 18.38,11.5C18.38,15.32 16.04,16.16 13.81,16.41C14.17,16.72 14.5,17.33 14.5,18.26C14.5,19.6 14.5,20.68 14.5,21C14.5,21.27 14.66,21.59 15.17,21.5C19.14,20.16 22,16.42 22,12A10,10 0 0,0 12,2Z" />
        </svg>
        <span class="d-none d-sm-flex">View on GitHub</span>
      </v-btn>
    </v-app-bar>

    <v-content>
      <v-container>
        <div class="mb-5">
          Get Source Code:
          <a href="https://github.com/goldenm-software/vuetify-datetime-picker/blob/master/src/app.vue" target="_blank">
            https://github.com/goldenm-software/vuetify-datetime-picker/blob/master/src/app.vue
          </a>
        </div>

        <v-row align="center">
          <v-expansion-panels multiple>
            <v-expansion-panel>
              <v-expansion-panel-header>Null Value</v-expansion-panel-header>
              <v-expansion-panel-content>
                <v-flex xs4>
                  <v-datetime-picker v-model="nullDatetime"></v-datetime-picker>
                </v-flex>
                <div>Datetime value: <span v-text="nullDatetime"></span></div>
              </v-expansion-panel-content>
            </v-expansion-panel>

            <v-expansion-panel>
              <v-expansion-panel-header>Init with Date</v-expansion-panel-header>
              <v-expansion-panel-content>
                <v-flex xs4>
                  <v-datetime-picker v-model="datetime"></v-datetime-picker>
                </v-flex>
                <div>Datetime value: <span v-text="datetime"></span></div>
              </v-expansion-panel-content>
            </v-expansion-panel>

            <v-expansion-panel>
              <v-expansion-panel-header>Init with String</v-expansion-panel-header>
              <v-expansion-panel-content>
                <v-flex xs4>
                  <v-datetime-picker v-model="datetimeString"></v-datetime-picker>
                </v-flex>
                <div>Datetime value: <span v-text="datetimeString"></span></div>
              </v-expansion-panel-content>
            </v-expansion-panel>

            <v-expansion-panel>
              <v-expansion-panel-header>Loading</v-expansion-panel-header>
              <v-expansion-panel-content>
                <v-flex xs4>
                  <v-datetime-picker loading></v-datetime-picker>
                </v-flex>
              </v-expansion-panel-content>
            </v-expansion-panel>

            <v-expansion-panel>
              <v-expansion-panel-header>Custom Loading</v-expansion-panel-header>
              <v-expansion-panel-content>
                <v-flex xs4>
                  <v-datetime-picker loading>
                    <template slot="progress">
                      <v-progress-linear color="red" indeterminate absolute height="7"></v-progress-linear>
                    </template>
                  </v-datetime-picker>
                </v-flex>
              </v-expansion-panel-content>
            </v-expansion-panel>

            <v-expansion-panel>
              <v-expansion-panel-header>Disabled</v-expansion-panel-header>
              <v-expansion-panel-content>
                <v-flex xs4>
                  <v-datetime-picker v-model="datetime" disabled></v-datetime-picker>
                </v-flex>
                <div>Datetime value: <span v-text="datetime"></span></div>
              </v-expansion-panel-content>
            </v-expansion-panel>

            <v-expansion-panel>
              <v-expansion-panel-header>Custom Actions</v-expansion-panel-header>
              <v-expansion-panel-content>
                <v-flex xs4>
                  <v-datetime-picker v-model="datetime">
                    <template slot="actions" slot-scope="{ parent }">
                      <v-btn color="error lighten-1" @click.native="parent.clearHandler">Cancel</v-btn>
                      <v-btn color="success darken-1" @click="parent.okHandler">Done</v-btn>
                    </template>
                  </v-datetime-picker>
                </v-flex>
                <div>Datetime value: <span v-text="datetime"></span></div>
              </v-expansion-panel-content>
            </v-expansion-panel>

            <v-expansion-panel>
              <v-expansion-panel-header>Custom Icons</v-expansion-panel-header>
              <v-expansion-panel-content>
                <v-flex xs4>
                  <v-datetime-picker v-model="datetime">
                    <template slot="dateIcon">
                      <v-icon>fas fa-calendar</v-icon>
                    </template>
                    <template slot="timeIcon">
                      <v-icon>fas fa-clock</v-icon>
                    </template>
                  </v-datetime-picker>
                </v-flex>
                <div>Datetime value: <span v-text="datetime"></span></div>
              </v-expansion-panel-content>
            </v-expansion-panel>

            <v-expansion-panel>
              <v-expansion-panel-header>Custom Format</v-expansion-panel-header>
              <v-expansion-panel-content>
                <v-flex xs4>
                  <v-datetime-picker v-model="formattedDatetime" date-format="MM/dd/yyyy"></v-datetime-picker>
                </v-flex>
                <div>Datetime value: <span v-text="formattedDatetime"></span></div>
              </v-expansion-panel-content>
            </v-expansion-panel>

            <v-expansion-panel>
              <v-expansion-panel-header>Use Seconds</v-expansion-panel-header>
              <v-expansion-panel-content>
                <v-alert type="warning"> You should set <code>time-format</code>. </v-alert>
                <v-flex xs4>
                  <v-datetime-picker
                    v-model="datetime"
                    :time-picker-props="timeProps"
                    time-format="HH:mm:ss"
                  ></v-datetime-picker>
                </v-flex>
                <div>Datetime value: <span v-text="datetime"></span></div>
              </v-expansion-panel-content>
            </v-expansion-panel>

            <v-expansion-panel>
              <v-expansion-panel-header>Custom Properties</v-expansion-panel-header>
              <v-expansion-panel-content>
                <v-alert type="warning"> You should set <code>time-format</code>. </v-alert>
                <v-flex xs4>
                  <v-datetime-picker
                    v-model="datetime"
                    :text-field-props="textFieldProps"
                    :date-picker-props="dateProps"
                    :time-picker-props="timeProps"
                    time-format="HH:mm:ss"
                  ></v-datetime-picker>
                </v-flex>
                <div>Datetime value: <span v-text="datetime"></span></div>
              </v-expansion-panel-content>
            </v-expansion-panel>
          </v-expansion-panels>
        </v-row>
      </v-container>
    </v-content>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      nullDatetime: null,
      datetime: new Date(),
      datetimeString: '2019-01-01 12:00',
      formattedDatetime: '09/01/2019 12:00',
      textFieldProps: {
        appendIcon: 'event'
      },
      dateProps: {
        headerColor: 'red'
      },
      timeProps: {
        useSeconds: true,
        ampmInTitle: true
      }
    }
  }
}
</script>

<style lang="scss">
.v-btn, .v-toolbar__title {
  font-family: 'Cabin', helvetica, sans-serif !important;
}
</style>
