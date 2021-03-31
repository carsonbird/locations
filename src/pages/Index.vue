<template>
  <div>
    <v-app id="inspire">
      <v-tabs v-model="tab" fixed-tabs>
        <v-tab>Map</v-tab>
        <v-tab>List</v-tab>
        <v-tab>Add</v-tab>
      </v-tabs>

      <v-main>
          <v-tabs-items v-model="tab">
            <v-tab-item>
              <iframe class="clickup-embed" src="https://share.clickup.com/m/h/242b1-1057/0e72d2464fa4e4c" onwheel="" width="100%" height="814px" style="background: transparent; border: 0 solid #ccc;"></iframe>
            </v-tab-item>
            <v-tab-item>
              <iframe class="clickup-embed" src="https://share.clickup.com/l/h/6-56798735-1/4fb361b2f0b4df7" onwheel="" width="100%" height="814px" style="background: transparent; border: 0 solid #ccc;"></iframe>
            </v-tab-item>
            <v-tab-item>
              <iframe class="clickup-embed clickup-dynamic-height" src="https://forms.clickup.com/f/242b1-1120/VFVP5E35KLKYH50XUP" onwheel="" width="100%" height="814px" style="background: transparent; border: 0 solid #ccc;"></iframe>
            </v-tab-item>
          </v-tabs-items>
      </v-main>
    </v-app>
  </div>
</template>

<script>
  export default {
    data: () => ({
        drawer: null,
        selectedItem: null,
        tab: null,
    }),
    methods: {
      includeScript: function (url) {
        let formScript = document.createElement('script')
        formScript.setAttribute('src', url)
        document.head.appendChild(formScript)
      }
    },
    mounted() {
      this.includeScript('https://app-cdn.clickup.com/assets/js/forms-embed/v1.js')
    },
  }
</script>