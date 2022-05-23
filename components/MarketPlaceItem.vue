<template>
  <div>
    <v-col>
<v-container>
      <v-card max-width="250" height="350" elevation="2" class="grey lighten-5 pa-2 rounded">
        <v-col>
          <div>
            <h4 class="heading pa-4 gradient gradient-3 rounded" style="text-align: center">{{ data.title }}</h4>
          </div>
          <div>
            <p class="description">{{ data.description }}</p>
          </div>
        </v-col>
      </v-card>
    </v-container>
    <span v-if="$vuetify.breakpoint.xs || $vuetify.breakpoint.sm">⬅️Swipe➡️</span>
    </v-col>
    
  </div>
</template>

<script>
export default {
  props: {
    data: {
      type: Object,
      default: null,
    },
  },
}
</script>

<style scoped>
.heading {
  font-size: 32px;
  line-height: 36px;
  font-weight: 500;
  color: black;
  text-align: center;
}

.description {
  font-size: 20px;
  line-height: 32px;
  color: black;
  text-align: center;
}

.gradient-3 {
  background: linear-gradient(45deg, #FA8BFF 0%, #2BD2FF 52%, #2BFF88 90%);
}
</style>
