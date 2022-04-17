<template>
  <div class="App">
    <div class="Tabs">
      <div class="nav">
        <button @click="activeTab = 'Tab01'">Tab01</button>
        <button @click="activeTab = 'Tab02'">Tab02</button>
        <button @click="activeTab = 'Tab03'">Tab03</button>
        <button @click="activeTab = 'Tab04'">Tab04</button>
      </div>
      <div class="outlet">
        <Tab01 v-if="activeTab === 'Tab01'"/>
        <Tab02 v-if="activeTab === 'Tab02'"/>
        <Tab03 v-if="activeTab === 'Tab03'"/>
        <Tab04 v-if="activeTab === 'Tab04'"/>
      </div>
    </div>
  </div>
</template>

<script>
  import Tab01 from './components/Tab01.vue'
  import Tab02 from './components/Tab02.vue'
  import Tab03 from './components/Tab03.vue'
  import Tab04 from './components/Tab04.vue'

  export default {
    components: {
      Tab01,
      Tab02,
      Tab03,
      Tab04
    },
    data() {
      return {
        activeTab: 'Tab01'
      }
    },
  }
</script>

<style>

  * {
  box-sizing: border-box;
  padding: 0;
  margin: 0;
}

.App {
  width: 100vw;
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  overflow: hidden;
}



/* Tab Navigation */
div.nav {
  width: 100%;
  margin: 0 auto 1rem;
  display: flex;
  justify-content: space-between;

  @media (max-width: 768px) {
    width: 90%;
  }
}

div.nav button {
  width: 150px;
  height: 50px;
  padding: 1rem;
  margin: 0.5px 10px;
  list-style: none;
  text-align: center;
  cursor: pointer;
  transition: all 0.7s;
  border-radius: 0.5rem;
  font-size: 15px;
  background-color: rgba(219, 209, 209, 0.993);
}


div.nav button:hover {
  background-color: rgba(219, 209, 209, 0.299);
}

div.nav button.active {
  background-color: rgba(219, 209, 209, 0.299);
}

div.outlet {
  width: 100%;
  height: 180px;
  padding: 1rem 1rem;
  list-style: none;
  cursor: pointer;
  transition: all 0.7s;
  border-radius: 0.5rem;
  border: 1px solid black;
  background: #e1e8ec;
  font-size: 25px;
}

</style>