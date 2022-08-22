<template> 
   <header>
      <h1>{{ title }}</h1>
      <ButtonTag text="Add Task" color="green" />
      <ButtonTag text="Update Task" color="blue" />
      <ButtonTag text="Delete Task" color="red" />
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