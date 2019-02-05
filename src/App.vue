<template>
  <div>
    <Header />
    <h1>
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla semper consectetur enim, at venenatis risus porta ac. Vestibulum libero metus, imperdiet sit amet enim in, condimentum laoreet nisi. Nulla vel tincidunt nibh. Quisque eu arcu lacus. Sed malesuada diam vitae elit eleifend, et ornare risus bibendum. Maecenas venenatis nunc et augue vestibulum, id tempus dolor commodo. Donec volutpat neque metus, sit amet fringilla felis sollicitudin vitae.
    </h1>
    <ul>
      <li v-for="comment in comments" class="comment" :key="comment.id">
        <p>{{ comment.name}}</p>
        <p>{{ comment.content}}</p>
      </li>
    </ul>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
export default {
  name: "App",
  components: {
    Header
  },
  data(){
    return{
      comments: [
      {
        id:1234,
        name: 'M',
        content: 'Oj oj oj oj',
      },
      {
        id:12345,
        name: 'M',
        content: 'Oj oj oj oj',
      },
      {
        id:123455,
        name: 'M',
        content: 'Oj oj oj oj',
      },
      ]
    }
  }
};
</script>
<style lang="scss" scoped>
h1 {
  color: #333;
  font-size: 1em;
  font-weight: 300;
  font-family: 'Montserrat';
}
.comment {
  background: #eee;
  padding: 20px;
  margin-bottom: 10px;
  list-style: none;

  p:first-child {
    font-weight: bold;
  }

  p:last-child {
    font-size: 2em;
  }
}
</style>
