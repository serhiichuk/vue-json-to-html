<template>
    <div id="app">
        <JsonToHtml :json="json" :bem="true" rootClassName="wrapper" rootTagName="section">
            <button @click="doSms">OK</button>
        </JsonToHtml>
    </div>
</template>

<script>
  import JsonToHtml from "./components/json-to-html";

  export default {
    components: {
      JsonToHtml,
    },
    data() {
      return {
        json: {
          title: 'True Title',
          'oredered-list': [
            'list item - 1',
            'list item - 2',
            'list item - 3',
            'list item - 4',
            {
              'extended': {
                name: 'foo',
                desc: 'bar',
              },
            },
          ],
        },
      }
    },
    methods: {
      doSms() {
        console.log('OK');
      },
    },
  }
</script>

<style lang="scss">
    #app {
        font-family: "Avenir", Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        text-align: center;
        color: #2c3e50;
        margin-top: 60px;
    }
</style>
