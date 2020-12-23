<template>
    <div>
      <Header/>
      <Home />
      <MobileBottomMenu/>
    </div>


</template>

<script>
import Header from "@/components/header/Header"
import MobileBottomMenu from "@/components/header/MobileBottomMenu"
import Home from '@/components/Home'


export default {
  name: 'Main',
  components: {
    Header,
    MobileBottomMenu,
    Home,
    
  }
}
</script>
<style>

</style>