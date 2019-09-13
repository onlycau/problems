<template>
  <v-app>
    <v-content>
      <div v-show='is_hide_text' ref='text'>
        <p>some text</p>
      </div>
      <button @click='hide_content'>hide_content</button>
    </v-content>
  </v-app>
</template>

<script>
import HelloWorld from './components/HelloWorld';

export default {
  name: 'App',
  data: () => ({
    //
  }),
  computed:{
    is_hide_text(){
      return this.$vuetify.breakpoint.mdAndUp
    }
  },
  methods:{
    hide_text(){
      this.$refs['text'].style.display = 'none'
    }
  }
};
</script>
