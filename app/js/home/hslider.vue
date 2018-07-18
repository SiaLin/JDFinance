<template lang="html">
  <article class="">
    <Slider :items="items" :cname="$style.slider"/>
     <section :class="$style.list">
       <div :class="$style.item" v-for="item in enters" :key="item.img">
         <router-link :to="{ name: item.href }">
           <img :src="item.img" :alt="item.title">
           <h4>{{item.title}}</h4>
         </router-link>
       </div>
     </section>
  </article>
</template>

<script>
import Slider from "../core/slider.vue"
export default {
  components: {
    Slider,
  },
  data(){
    return{
      items:[{
        href:'home',
        src:'//img12.360buyimg.com/jrpmobile/jfs/t23989/289/1020372086/42184/c3612678/5b4c8846N19748742.jpg'
      },{
        href:'home',
        src:'//img12.360buyimg.com/jrpmobile/jfs/t24136/236/1034752935/37811/621e24cd/5b4c885eNd45cbb72.jpg'
      },{
        href:'home',
        src:'//img12.360buyimg.com/jrpmobile/jfs/t24406/237/996662219/36372/28d842f6/5b4c8829Ne187ce7b.jpg'
      },{
        href:'home',
        src:'//img12.360buyimg.com/jrpmobile/jfs/t23107/111/1047377883/39342/6449d303/5b4c8804Ne07a7227.jpg'
      }],
      enters:[{
        href:'home',
        img:'//img12.360buyimg.com/jrpmobile/jfs/t3991/64/2521945388/12110/93c0139/58d1e462Ncf294123.png',
        title:'优惠卷'
      },{
        href:'home',
        img:'//img12.360buyimg.com/jrpmobile/jfs/t5590/252/875247023/17343/946aa72c/59224650N0f7ffc92.png',
        title:'领红包'
      },{
        href:'home',
        img:'//img12.360buyimg.com/jrpmobile/jfs/t4393/329/2180608902/13217/c88c0cec/58ec9dcdN1534e2d7.png',
        title:'抢钢蹦'
      },{
        href:'home',
        img:'//img12.360buyimg.com/jrpmobile/jfs/t5488/298/1036263348/12073/b4f4de97/590ac8e8Ne9def22e.png',
        title:'白条提额'
      }],
    }
  },

}
</script>

<style lang="scss" module>
  @import "../../css/element.scss";
  .slider{
    margin-top:120px;
    img{
      width: 100%;
    }
  }
  .list{
    @include list(row);
    background-color: #fff;
    padding-top: 40px;
    padding-bottom: 20px;
    justify-content: space-around;
    a{
      text-decoration: none;
    }
    .item{
      text-align: center;
      img{
        display: inline-block;
        width: 90px;
        height: 90px;
      }
      h4{
        font-size: 26px;
        margin-top: 12px;
        color: #666;
      }
    }
  }

</style>
