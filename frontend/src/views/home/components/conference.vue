<template>
  <div style="margin:10px">
    <el-card :body-style="{ padding: '0px' }">
      <el-image
        style="width: auto; height: 120px"
        :src="state.imgList[thumbnail].imgUrl"
        class="image"
      ></el-image>
      <div style="display:flex; justify-content:space-between;">
        <span style="margin-start:5px;">{{ title }}</span>
        <span style="margin-end:5px; font-size:0.8rem; color:grey;">({{ headCount }} / {{ maxPeople }})</span>
      </div>
      <div style="text-align:start;">
        <span style="margin-start:5px; font-size:0.8rem; color:grey;"># {{ state.roomCategory[category-1] }}</span>
      </div>
    </el-card>
  </div>
</template>

<style scoped>
.image {
  width: 100%;
  display: block;
}

</style>
<script>
import { reactive } from 'vue'

export default {
  name: 'Home',

  props: {
    title: {
      type: String,
      default: ''
    },
    category: {
      type: Number,
      default: 1
    },
    thumbnail: {
      type: Number,
      default: 0
    },
    headCount: {
      type: Number,
      default: 0
    },
    maxPeople: {
      type: Number,
      default: 0
    },
  },

  setup () {
    const state = reactive({
      imgList: [
        {
          imgNum: '0',
          imgUrl: require('../../../assets/images/thumbnail/0.png')
        },
        {
          imgNum: '1',
          imgUrl: require('../../../assets/images/thumbnail/1.png')
        },
        {
          imgNum: '2',
          imgUrl: require('../../../assets/images/thumbnail/2.png')
        },
        {
          imgNum: '3',
          imgUrl: require('../../../assets/images/thumbnail/3.png')
        },
        {
          imgNum: '4',
          imgUrl: require('../../../assets/images/thumbnail/4.png')
        },
        {
          imgNum: '5',
          imgUrl: require('../../../assets/images/thumbnail/5.png')
        },
        {
          imgNum: '6',
          imgUrl: require('../../../assets/images/thumbnail/6.png')
        },
        {
          imgNum: '7',
          imgUrl: require('../../../assets/images/thumbnail/7.png')
        },
        {
          imgNum: '8',
          imgUrl: require('../../../assets/images/thumbnail/8.png')
        }
      ],
      roomCategory: ['어학', '공무원', '취업', '자격증', '대입', '자율']
    })

    return { state }
  }
}
</script>
