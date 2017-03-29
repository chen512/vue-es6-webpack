<template>
    <div>
        <div>this is template footer</div>
        <div @click="showWorld">{{msg}}</div>
        <div>{{test}}</div>
      <div v-show="flag">layear</div>
    </div>
</template>
<style>

</style>
<script type="text/ecmascript-6">
    export default{
        props: {
          test: {
            type: Number
          }
        },
        data() {
            return {
                flag: false,
                msg: 'hello vue'
            };
        },
        methods: {
          showWorld: function (e) {
            this.flag = true;
            console.log(this.test);
          }
        },
      create() {
        debugger;
        console.log(this.flag);
      }
    };
</script>
