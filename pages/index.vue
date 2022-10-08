<template>
  <div>
    <div class="icon-gu">
      CHWAN
      <div class="top-right">
        <div class="circle"></div>
        {{ hours }}:{{ minutes }}
      </div>

    </div>
    <div class="left-title">
      =========文章列表=========<br>
      =========项目列表=========<br>
    </div>
    <div class="bottom-cc">
      嗨， 我是 chwan, Web Developer<br>
      你可以在 Github 找到我 id：chwan97<br>
      你可以给我发一封邮件通过 <a href="#">mail#chwan.cc</a>(# -> @)
    </div>
  </div>
</template>

<style>
body {
  padding: 15px;
  background-color: #252525;
  font-weight: 500;
  font-size: 25px;
}

a, a:active, a:visited, a:hover {
  text-underline: none;
  text-decoration: none;
  /*color: #5309CD;*/
}

.bottom-cc {
  text-align: center;
  position: fixed;
  bottom: 30px;
  transform: translateX(-50%);
  left: 50%;
  font-weight: 600;
  color: #FFFF00;
}

.icon-gu {
  font-size: 400px;
  color: #2030a0;
  border: 10px solid #ddd;
  position: fixed;
  top: 30px;
  transform: translateX(-50%);
  left: 50%;
}

.left-title {
  font-size: 25px;
  color: #aaa;
  position: fixed;
  bottom: 150px;
  left: 100px;
  cursor: not-allowed;
}

.circle {
  width: 40px;
  height: 40px;
  border-radius: 100px;
  background-color: #d30000;
  margin-right: 10px;
}

.top-right {
  position: absolute;
  right: 20px;
  top: 20px;
  font-size: 40px;
  display: flex;
  color: #d30000;
  align-items: center;
  font-weight: 600;
}

</style>

<script lang="js">
import pad from 'pad'

export default {
  name: 'IndexPage',
  data() {
    return {
      hours: '--',
      minutes: '--'
    }
  },
  computed: {},
  methods: {},
  mounted() {
    setImmediate(() => {
      this.hours = pad(2, (new Date()).getHours(), '0')
      this.minutes = pad(2, (new Date()).getMinutes(), '0')
    }, 1000)
  }
}
</script>
