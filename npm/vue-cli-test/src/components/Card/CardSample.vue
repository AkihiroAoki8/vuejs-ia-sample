<template>
  <div>
    <div class="red-b mb-4">
      <CardTitle />
      <CardImage />
      <CardDescription />
    </div>
  </div>
</template>

<script>
import CardTitle from '@/components/Card/CardTitle'
import CardImage from '@/components/Card/CardImage'
import CardDescription from '@/components/Card/CardDescription'

export default {
  components : {
    CardTitle,
    CardImage,
    CardDescription  
  }
}
</script>

<style scoped>
.red-b{
  border: 1px blue solid;
}

.mb-4{
  margin-bottom: 4px;
}

</style>