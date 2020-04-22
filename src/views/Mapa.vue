<template>
    <div>
      <GmapMap
      v-bind:center="center"
      v-bind:zoom="7"
      style="width: 700px; height: 500px"
  >
    <GmapMarker
      v-bind:key="index" v-for="(m, index) in 
      markers"
      v-bind:position="m.position"
      v-bind:clickable="true"
    />
    </GmapMap>
    <button @click="alerta()">Criar Alerta!</button>
    </div>
</template>

<script>
export default {
  name: "Mapa",
  
  components: {
  },

  data() {
    return {
      center: { lat: -22.90278, lng: -43.2075 },
      markers: [
        
      ]
    }
  },

  methods: {
    alerta: function(){
      alert("Chama o desenvoldor!");
    }
  }
  
};
</script>