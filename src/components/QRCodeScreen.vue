<template>
  <div>
    <div class="d-flex h-screen bg-black">
      <div class="w-4/5 h-full m-auto">
        <qrcode-stream @decode="onDecode"/>
      </div>
    </div>

  </div>
</template>

<script>
import { QrcodeStream } from 'vue3-qrcode-reader'
import axios from "axios"
axios.defaults.headers.common['Access-Control-Allow-Origin'] = '*';

export default {
  components: {
      QrcodeStream
  },
  methods: {
    async onDecode(decodeString){
      console.log(decodeString)
      // try {
      //   const a = await axios.post("https://example.com", decodeString);
      //   console.log(a);
      // } catch (error) {
      //   throw Error(error);
      // }
    }
  }
}
</script>

<style>

</style>