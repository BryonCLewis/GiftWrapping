<template>
  <div>
    <v-container fluid>
      <!--Heading tool to add in new buttons -->
      <v-row >
          <v-col cols='10'></v-col>
        <v-col >
          <v-btn outlined large>+ Add</v-btn>
        </v-col>
      </v-row>
      <!--List of rows of the different point generation types -->
      <v-row>
        <v-col>
        <table width='100%'>
          <thead>
            <tr >
              <th v-for="item in tableHeader" :key="item" class="text-left">{{item}}</th>
            </tr>
          </thead>
          <tbody>
            <tr v-for="(item,key) in pointList" :key="'pointlistitem_'+key">
                <!--We take each item in the list and then subdivide it out based on the headers to add it to the table -->
              <td v-for="(itemheader, subkey) in tableHeader" :key="'subpoint_'+key+'_header'+subkey">{{ item[itemheader] }}</td>
            </tr>
          </tbody>
                </table>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script lang="ts">
import Vue from "vue";

export default Vue.extend({
  data() {
    return {
      tableHeader: ["Type", "Points", "Config", "Modify", "Edit"],
      pointList: [{"Type":"Random","Points":"view"}]
    };
  }
});
</script>

<style scoped></style>
