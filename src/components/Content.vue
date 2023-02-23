<script lang="ts" >
export default {
    props: ['id','title','note','remark']
}
</script>
<template>
   <h2>{{ id }}{{ title }}</h2> 
   <h4>{{ note }}</h4>
   <h6>{{ remark }}</h6>
</template>