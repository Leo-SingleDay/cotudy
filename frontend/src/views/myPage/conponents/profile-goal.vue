<template>
  <div class="my-goal-container">
    <div class="my-studytime-area">
      <div>오늘 나의 공부한 시간</div>
      <div class="studytime-wrapper">
        <div>{{state.user.todayStudyTime}}</div>
        <div>{{state.user.goalTimeToString}}</div>
      </div>
      <el-progress
        :text-inside="true"
        :stroke-width="26"
        :percentage="
          state.user.todayStudyTimeBefore > 0 ?
          (Math.floor(state.user.todayStudyTimeBefore / state.user.goalTime* 100)) > 100 ? 100 : Math.floor(state.user.todayStudyTimeBefore / state.user.goalTime* 100)
          : 0
        "
        status="success"
      />

    </div>
    <div class="my-resolution-area">
      <div>나의 다짐</div>
      <div>{{state.user.goal}}</div>
    </div>
  </div>
</template>
<style scoped>
  .my-goal-container {
    background: rgb(255, 255, 255);
    height:250px;
    width:45vw;
    padding: 40px 20px;
    border-radius: 20px;
    text-align: left;
  }
  .my-studytime-area {
    width:45vw;
  }
  @media (max-width: 1150px) {
    .my-studytime-area{
      width:75vw;
    }
  }
  .my-resolution-area {
    margin-top: 40px;
  }

  .my-resolution-area div:first-child{
    font-size: 20px;
    font-weight: 900;
    margin-bottom: 10px;
  }
  .my-studytime-area div:first-child {
    font-size: 17px;
    font-weight: 900;
    margin-bottom: 10px;
  }
  .my-studytime-area .studytime-wrapper {
    display: flex;
    justify-content : space-between;
    flex-direction: row;

  }
  .my-studytime-area .studytime-wrapper div {
    font-size: 23px;
    font-weight: 900;
  }
  .my-studytime-area .studytime-wrapper div:last-child {
    color: var(--el-border-color-lighter);
    font-weight: 200;
  }
</style>
<style>
  :root {
    --el-color-success: #3AC258;
    --el-border-color-lighter: #cccccc;
  }
</style>

<script>
import { reactive, onUpdated } from 'vue';
export default {
  name: 'profile-goal',

  props: {
		user: Object,
	},
  setup (props) {
    const state = reactive({
      user: props.user,
      percentage: 0,
    })

    onUpdated(()=> {
      let tempTime = state.user.goalTime
      let hour = (tempTime / 60) >= 1 ? tempTime/60 : 0;
      let minute = (tempTime % 60) >= 1? tempTime%60 : 0;
      state.user['goalTimeToString'] = Math.floor(hour)+'시간 '+minute+'분'
    })

    return {
      state
    }
  }

}
</script>


