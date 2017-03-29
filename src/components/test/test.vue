<template>
  <div>
    <div class="test">
      <div>this is template body</div>
      <ul>
      <li class="test-data" v-for="test in test">{{test.username}}</li>
      </ul>
    </div>
    <foot :test="test"></foot>
  </div>
</template>
<style lang="stylus" rel="stylesheet/stylus">
  @import "../../common/stylus/mixin.styl"

  .test
    text-align center
    background red
    padding 1rem




</style>
<script type="text/ecmascript-6">
  import foot from 'components/foot/footer';
    export default{
       data () {
            return {
                test: [],
                msg: 'hello vue'
            };
        },
       created() {
          this.$http.get('/api/ratings').then((response) => {
            this.test = response.body.data;
            debugger;
            console.log('1112312');
        });
      },
      components: {
        foot
      }
    };

</script>
