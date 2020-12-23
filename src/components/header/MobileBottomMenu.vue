<template>
  <div class="bg-white flex-row justify-center h-15 w-full bottom-0 z-40 fixed block sm:block md:block lg:hidden" >
      <div class="container mx-auto px-10 flex justify-between items-center ">
            <nav class="w-full">
                <ul class="flex list-none pb-1" >
                  <li v-for="item in Menu" :key="item.id">
                      <div class="grid text-secondary hover:text-black text-center" >
                          <font-awesome-icon :icon="['fas', item.icon]" class="mt-3 pb-2 text-8 mx-7"  />
                          <span class="text-xs ">{{item.title}}</span>
                      </div>
                  </li>
                </ul>
            </nav>
      </div>
  </div>
</template>

<script>
export default {
  name: "Header",
  components: {
   
  },
data () {
    return {
        Menu : [
          {
            id: 1,
            title: 'Home',
            slug: 'home',
            icon: 'home',
          },
          {
            id: 2,
            title: 'My Network',
            slug: 'my-network',
            icon: 'user-friends',
          },
          
          {
            id: 4,
            title: 'Post',
            slug: 'post',
            icon: 'plus',
          },
          {
            id: 5,
            title: 'Notifications',
            slug: 'notifications',
            icon: 'bell',
          },
          {
            id: 3,
            title: 'Jobs',
            slug: 'jobs',
            icon: 'suitcase',
          },
          
          
        ]
     }
  },
  computed: {
  

  },
  watch : {

     
  },
  methods : {
      tryFreeNow(){
        console.log('clicked')
      }

  },
 
  mounted () {
  

  },
  created () {
    

  }

}
</script>