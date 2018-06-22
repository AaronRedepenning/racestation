<template>
  <v-layout column>
    <v-layout row>
      <v-flex xs12 sm6 offset-sm3>
        <v-card>
          <v-subheader>Overview</v-subheader>
          <v-divider></v-divider>
          72.2 °F
        </v-card>
      </v-flex>
    </v-layout>
    <v-layout row>
      <v-flex xs12 sm6 offset-sm3>
        <v-card>
          <v-list>
            <v-subheader>Details</v-subheader>
            <v-divider></v-divider>
            <v-list-tile v-for="item in items" :key="item.name">
              <v-list-tile-content>
                <v-list-tile-title>{{ item.name }}</v-list-tile-title>
              </v-list-tile-content>
              <v-list-tile-action>
                {{ item.value }}
              </v-list-tile-action>
            </v-list-tile>
          </v-list>
        </v-card>
      </v-flex>
    </v-layout>
  </v-layout>
</template>

<script>
  export default {
    data () {
      return {
        items: [
          { name: 'Absolute Temperature', value: "1009.2 hPa" },
          { name: 'Air Temperature', value: "72.2 °F" },
          { name: 'Relative Humidity', value: "22 %" },
          { name: 'Adjusted Altitude', value: "60 Ft" },
          { name: 'Absolute Humidity', value: "40 %" },
          { name: 'Grains', value: "99" },
          { name: 'Vapor Pressure', value: "300.9 bars" },
          { name: 'Dew Point', value: "55 °F" },
          { name: 'Air Density Ratio', value: "33" },
          { name: 'Density Altitude', value: "70 Ft" },
          { name: 'Pressure Altitude', value: "44 Ft" },
          { name: 'Wind Speed', value: "12 mph" },
          { name: 'Wind Direction', value: "NW" },
          { name: 'Wind Gust', value: "30 mph" },
          { name: 'Ambient Light', value: "30 lumens" }
        ]
      }
    }
  }
</script>
