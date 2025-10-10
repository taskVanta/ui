<template>
    <div class="font-bold text-3xl text-center mt-10">
        <h1>Welcome to Nuxt 4 Starter Kit</h1>
        <p>This is the home page.</p>
    </div>
</template>

<script setup >
import { useCommonStore } from '~/store';


const commonStore = useCommonStore()


onMounted(() => {
  commonStore.increment()
  console.log('Count from store:', commonStore.count)
  console.log('Double Count from getter:', commonStore.doubleCount)
})


useMeta({
  title: 'Home – Resume Builder',
  description: 'Create your professional resume in minutes with our platform.',

})


</script>