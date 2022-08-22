 <template>
    <header>
        <h1>{{ title }}</h1>
    </header>
 </template>

 <script>
 export default {
    name: 'Header',
    props: ['title'],
 }
 </script>

 <style scoped>
  Header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 20px;
  }
 </style>