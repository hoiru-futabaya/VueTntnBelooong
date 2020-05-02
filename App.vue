<template>
   <view class="container">
      <text>お</text>
      <text>ち</text>
      <text>ん</text>
      <text>ち</text>
      <text>ん</text>
      <text>び</text>
      <text>ろ</text>
      <text v-for="(message, index) in messages" :key="index">{{message}}</text>
      <text>ん</text>
      <touchable-opacity class="button" :on-press="addTodo">
          <text class="button-text">のびる</text>
      </touchable-opacity>
      <touchable-opacity class="button" :on-press="rmTodo">
          <text class="button-text">ちちむ</text>
      </touchable-opacity>
    </view>
</template>
<script>
    export default {
       data: function() {
         return {
           messageText: '｜',
           messages: ['｜']
       }
    },
        methods: {
          addTodo: function() {
          this.messages.push(this.messageText)
            },
          rmTodo: function() {
          this.messages.splice(1, 1)
            }
          },
        }
</script>

<style>
.container {
  background-color: white;
  flex: 1;
  justify-content: center;
  align-items: center;
}

.button {
  background-color: pink;
  padding: 10px;
  border-radius: 5;
  justify-content: center;
  align-items: center;
  }

.main {
  flex: 1;
  max-width: 400px;
  align-items: center;
}
</style>
