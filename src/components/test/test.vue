<template>
  <div>
    <div class="test">
      <div>this is template body</div>
      <ul>
      </ul>
    </div>
    <p style="backgroud:black"></p>
    <foot v-on:childsay="listenToBoy"></foot>
    <p>{{child}}</p>
    <div>end</div>
  </div>
</template>
<style lang="stylus" rel="stylesheet/stylus">
  @import "../../common/stylus/mixin.styl"

  .test
    text-align center
    background red
    padding 1rem
  p
    background-color aqua




</style>
<script type="text/ecmascript-6">
  import foot from 'components/foot/footer';
    export default{
       data () {
            return {
                test: [],
                test1: '',
                msg: 'hello vue',
                childWords: '',
                child: ''
            };
        },
      methods: {
        listenToBoy: function (msg) {
          this.child = msg;
        }},
       created() {
          this.$http.get('/api/ratings').then((response) => {
            this.test = response.body.data;
            console.log('1112312');
        });
      },
      components: {
        foot
      }
    };

</script>
