<template>
  <div class="footer">
    时间:{{time}}
  </div>
</template>

<script>
export default {
  name: "Footer",
  data () {
    return {
      time: "",
    }
  },
  methods: {
    nowTime() {
      let nowDate = new Date();
      let date = {
        year: nowDate.getFullYear(),
        month: nowDate.getMonth()+1,
        date: nowDate.getDate(),
      };
      this.time = date.year+"-"+date.month+"-"+date.date;
    }
  },
  mounted() {
    this.nowTime()
  },
}
</script>

<style lang="less" scoped>
  .footer {
    border-top: 1px solid rgba(0,0,0,.05);
    height: 100px;
    padding-top: 20px;
  }
</style>