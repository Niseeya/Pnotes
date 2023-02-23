<script lang="ts" >
export default {
    props: ['id','title','note']
}
</script>
<template>
   <h2>{{ id }}{{ title }}</h2> 
   <h4>{{ note }}</h4>
</template>