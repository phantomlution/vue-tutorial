# v-on

<vuep template="#example"></vuep>

<script v-pre type="text/x-template" id="example">
<template>
  <div>
  	<p>{{ date | dateFilter }}</p>
    <p>消息数：{{ count | countFilter }}
    <p>金额：{{ money | moneyFilter }}
  </div>
</template>

<script>
module.exports = {
  data(){
    return {
      date: new Date().getTime(),
      count: 120,
      money: 100
    }
  },
  filters: {
    dateFilter(val){
      return val ? moment(val).fromNow() : '-'
    },
    countFilter(val){
      if(!val){
        return '';
      }else if(val > 99){
        return '99+'
      }else{
        return val;
      }
    },
    moneyFilter(val){
      if(!val){
        return ''
      }else{
        return (Number(val) / 100.00).toFixed(2) + '元'
      }
    }
  },
  methods: {
    reverseMessage: function () {
      this.message = this.message.split('').reverse().join('')
    }
  }
}
</script>
</script>