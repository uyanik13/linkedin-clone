<template>
  <header class="bg-white flex flex-row justify-center h-15 w-full z-40 lg:fixed  border-b border-gray-200">
      <div class="container mx-auto px-6 h-16 flex justify-between items-center  ">
           <div id="logo" class="flex w-3/12">
              <div>
                <svg xmlns="http://www.w3.org/2000/svg" width="34" height="34" viewBox="0 0 34 34" class="text-blue">
                  <title>LinkedIn</title>
                  <g><path d="M34,2.5v29A2.5,2.5,0,0,1,31.5,34H2.5A2.5,2.5,0,0,1,0,31.5V2.5A2.5,2.5,0,0,1,2.5,0h29A2.5,2.5,0,0,1,34,2.5ZM10,13H5V29h5Zm.45-5.5A2.88,2.88,0,0,0,7.59,4.6H7.5a2.9,2.9,0,0,0,0,5.8h0a2.88,2.88,0,0,0,2.95-2.81ZM29,19.28c0-4.81-3.06-6.68-6.1-6.68a5.7,5.7,0,0,0-5.06,2.58H17.7V13H13V29h5V20.49a3.32,3.32,0,0,1,3-3.58h.19c1.59,0,2.77,1,2.77,3.52V29h5Z" fill="currentColor"></path> </g>
                </svg>
            </div>
            <div>
              <input  class="p-2 ml-2 py-1 rounded-md border-none bg-gray-200 w-full" placeholder="Search"  aria-label="Search" type="text">
            </div>
           </div>

          <nav class="w-5/12">
              <ul class="flex list-none pb-1 border-r-default border-gray-300  " >
                <li v-for="item in Menu" :key="item.id">
                    <div class="grid text-secondary hover:text-black text-center" >
                        <font-awesome-icon :icon="['fas', item.icon]" class="mt-3 pb-2 text-6 mx-7"  />
                        <span class="text-xs ">{{item.title}}</span>
                    </div>
                </li>
                <li class="mx-2" >
                    <div id="me" class="grid mt-2 text-secondary hover:text-gray-900 text-center">
                      <img class="rounded-full w-6" src="https://media-exp1.licdn.com/dms/image/C4E35AQHYiObqT_uAOA/profile-framedphoto-shrink_100_100/0/1608036315334?e=1608818400&v=beta&t=ONPAGPISoh4aCtfvv8RIklxQaw-ZHYouZUJ75oGA6ns" alt="Profile picture" />
                      <span class="text-xs ">Me <font-awesome-icon  :icon="['fas', 'caret-down']" class="text-6"/></span>
                  </div>
                </li>
              </ul>
          </nav>

          <div id="top-right-side" class="w-3/12">
            <ul class="flex list-none pb-1 ">
                <li class="mx-2" >
                    <div id="me" class="grid  text-secondary hover:text-gray-900 text-center">
                      <font-awesome-icon :icon="['fas', 'th']" class="mt-3 pb-1 text-5"  />
                      <span class="text-xs">Work <font-awesome-icon  :icon="['fas', 'caret-down']" class="text-6"/></span>
                  </div>
                </li>
              </ul>
          </div>
      </div>
  </header>

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
            id: 3,
            title: 'Jobs',
            slug: 'jobs',
            icon: 'suitcase',
          },
          {
            id: 4,
            title: 'Messaging',
            slug: 'messaging',
            icon: 'comment-dots',
          },
          {
            id: 5,
            title: 'Notifications',
            slug: 'notifications',
            icon: 'bell',
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