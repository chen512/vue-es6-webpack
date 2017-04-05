<template>
    <div>
        <div>this is template footer</div>
        <div v-on:click="onClick">click</div>
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
            type: Array
          }
        },
        data() {
            return {
                flag: false,
                msg: 'i love u matt1',
                msg1: 'i love u matt'
            };
        },
        methods: {
          showWorld: function (e) {
            this.flag = true;
            this.msg1 = '132231131123232131231132';
          },
          onClick: function() {
            this.$emit('childsay', this.msg);
          }
        },
      create() {
      }
    };
</script>
