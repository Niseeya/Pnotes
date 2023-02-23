<script>
import Content from '../components/Content.vue' 
export default {
  components: {
    Content
  },
  data() {
    return {
      posts: [
        { id: 1, title:'空',note: '空想社会主义的产生、发展和局限性', },
        { id: 2,  title:'课',note: '科学社会主义的创立、第一国际和巴黎公社' },
        { id: 3,  title:'是',note: '十月革命胜利与第一个社会主义国家的建立' }
      ]
    }
  }
}
</script>

<template>
	<Content
  	v-for="post in posts"
	  :id="post.id"
  	:title="post.title"
    :note="post.note"
	></Content>
</template>