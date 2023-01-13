<script>
import DynComp1 from './components/DynComp1.vue'
import DynComp2 from './components/DynComp2.vue'
import DynComp3 from './components/DynComp3.vue'


export default {
  components: {
    DynComp1,
    DynComp2,
    DynComp3
  },
  data() {
    return {
      activecomponent: 'DynComp1'
    }
  },
  methods: {
    setcomp(comp) {
      this.activecomponent = comp
    }
  }
}
</script>

<template>
 

      <div>
        <button @click="setcomp('DynComp1')">DynComp1</button>
        <button @click="setcomp('DynComp2')">DynComp2</button>
        <button @click="setcomp('DynComp3')">DynComp3</button>
       

      </div>

      <div>
        <keep-alive>
          <component :is="activecomponent"></component>
        </keep-alive>
        
      </div>


</template>

<style scoped>

</style>
