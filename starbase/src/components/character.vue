<template>
    <div>
        {{character}}
    </div>
</template>

<script>
export default {
  props: ['id'],
  data(){
      return {
          character: {}
      }
  },
  methods: {
      getData(id){
          var url = `https://swapi.co/api/people/${id}`;
          console.log(url);
          fetch(url,{
              method: 'GET'
          }).then(response => response.json()).then(json => this.character = json)
      }
  },
  created() {
      this.getData(this.id);
  }
}
</script>

