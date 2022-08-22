 <template>
   <header>
      <h1>{{ title }}</h1>
      <ButtonTag />
   </header>
</template>

 <script>
import ButtonTag from './ButtonTag';

export default {
    name: "TopText",
    props: {
        title: {
            type: String,
        }
    }
    //  ['title'],
    ,
    components: {  ButtonTag }
}
</script>

 <style scoped>
 header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 20px;
 }
 </style>