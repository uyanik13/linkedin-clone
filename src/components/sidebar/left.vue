<template>
<!-- /* eslint-disable */ -->
  <div class="flex flex-row justify-center ">
    <div class="bg-white my-2 pb-6 w-full justify-center items-center overflow-hidden md:max-w-sm rounded-lg shadow-sm mx-auto ">
      <div class="relative h-16 ">
        <img class="absolute h-full w-full object-cover" src="/assets/img/ogur-bg.jpg">
      </div>
      <div class="relative shadow mx-auto h-16 w-16 -my-12 rounded-full  overflow-hidden border-4 border-white ">
        <img class="object-cover w-full h-full" src="/assets/img/ogur.jpg">
      </div>
      <div class="mt-16 border-b-default border-gray-300">
        <h1 class="text-lg text-center text-primary ">
         Oğur UYANIK
        </h1>
        <p class="text-sm text-secondary text-center pb-4">
          Full Stack Developer
        </p>
      </div>
      <div class=" text-3 pt-1 hover:bg-theme1 flex mt-2 px-2 py-2  items-center justify-between">
        <div class="text-gray-600  px-0">
            Who viewed your profile
          </div>
          <div  class="font-bold text-indigo-600">
            798
          </div>
      </div>

       <div class="text-3 pt-1  hover:bg-theme1 flex mb-3  px-2  items-center justify-between">
          <div class="text-gray-600  px-0">
            Views of your post
          </div>

          <div class="font-bold text-indigo-600">
            4988
          </div>
      </div>

       
      <div class="text-4 pt-1  hover:bg-theme1 flex mt-0 px-2  items-center justify-between border-t-default border-gray-300">
          <div class="text-gray-600 px-0">
             <font-awesome-icon :icon="['fas', 'bookmark']" class="text-3"  />
            My items
          </div>
      </div>
    </div>
    
  </div>

</template>

<script>
export default {
  name: "left-sidebar",
  components: {
   
  },
data () {
    return {
        
     }
  },
  computed: {
  

  },
  watch : {

     
  },
  methods : {
     

  },
 
  mounted () {
  

  },
  created () {
    

  }

}
</script>