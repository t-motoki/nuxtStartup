<template>
  <section class="container">
    <h1>todo app</h1>
    <p><input type="text" name="content"/></p>
    <div>
      <button>save</button>
      <button>find</button>
    </div>
    <ul>
      <li v-for="(todo, index) in todos" :key="index">
        <span>{{todo.content}}</span><span>{{todo.created}}</span>
      </li>
    </ul>
  </section>
</template>

<script>
import {mapState} from 'vuex';
export default {
  data: function() {
    return {
      content:''
    }
  },
  computed: {
    ...mapState(['todos'])
  }
}

</script>
