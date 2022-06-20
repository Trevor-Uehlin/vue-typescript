
  <template>
    <br />
    This is the home page


    <button class="btn btn-dark" @click.native="getApiResponse()">Response Button</button>
  </template>

<script lang="ts">

export default {
  components:{},
  methods:{
    getApiResponse(){
      fetch("http://fbf.com/api/test")
      .then(res => {
        return res.json()
      })
      .then(data => {
        console.log(data)
      });
    }
  }
}

</script>
