//index.vue
<template>
    <div>
        <ul>
            <li v-for="todo in todos" v-if="seen">
                {{ todo.text }}
            </li>
        </ul>
        <button v-on:click="eClick">事件</button>
    </div>
</template>

<script>
export default {
  name: 'indexP',
  data () {
    return {
       todos: [
          { text: 'Learn JavaScript' },
          { text: 'Learn Vue' },
          { text: 'Build something awesome' }
        ],
       seen : true
    }
  },
  methods:{
    eClick:function(){
        this.seen = !this.seen;
    }
  }
}
</script>
