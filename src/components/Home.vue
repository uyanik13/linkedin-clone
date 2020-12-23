<template>
<div class="grid lg:grid-cols-12 gap-x-0 pt-20">
    <div class="col-start-3 col-span-1 w-48 ">
        <left-sidebar />
    </div>

    <div class="col-start-4 col-end-7  w-full ml-16  "> 
        <div class="bg-white my-2 p-4 w-full rounded-lg ">
            <button class="p-3 rounded-full border-1 border-gray-300 bg-white w-full text-left flex items-center">
                <font-awesome-icon :icon="['fas', 'pen-square']" class="text-6 text-gray-500 mx-2"  />
                Start a post
            </button>
          <div class="flex items-center mt-3">
            <button class="p-3 flex ">
                <font-awesome-icon :icon="['fas', 'image']" class="text-6 text-blue-500 mx-1"  />
                Photo
            </button>
            <button class="p-3 flex">
                <font-awesome-icon :icon="['fab', 'youtube']" class="text-6 text-red-500 mx-1"  />
                Video
            </button>
            <button class="p-3 flex">
                <font-awesome-icon :icon="['fas', 'calendar-week']" class="text-6 text-gray-500 mx-1"  />
                Event
            </button>
            <button class="p-3 flex">
                <font-awesome-icon :icon="['fas', 'newspaper']" class="text-6 text-red-300 mx-1"  />
                Write Article
            </button>

        </div>

        </div>

        <div v-for="post in posts" :key="post.id" class="bg-white my-2 w-full rounded-lg ">
             <div id="action" class="flex items-center justify-between p-4 border-b-1  border-gray-300  ">
                    <div class="text-xs">
                            <a href="#" class="text-gray-700 font-bold hover:text-blue-600 hover:underline">{{post.user.name}}</a> likes this
                    </div>
                    <div class="text-5 text-gray-800" >
                        <button class="rounded-full w-8 h-8 hover:bg-theme1 hover:rounded-lg">
                            <font-awesome-icon :icon="['fas', 'ellipsis-h']"   />
                        </button>
                    </div>
             </div>   
             <div id="content" class="py-2">
                    <div class="flex items-start p-4 ">
                        <div>
                            <img class="rounded-full w-12"  :src="post.user.avatar" alt="">
                        </div>
                        <button>
                            <p class="mx-2 text-sm font-bold  flex items-center "> {{post.user.name}} <span class="font-light text-gray-600 mx-2"> • 2nd</span></p>
                            <p class="mx-2 text-sm font-light text-gray-600">{{post.user.title}}</p>
                            <p class="mx-2 text-sm font-light text-gray-600 flex items-center "> 4h •  <font-awesome-icon :icon="['fas', 'globe-europe']" class="mx-2"  /> </p>
                        </button>
                        
                    </div>
                    <div class="px-2 py-2 p-4 ">
                        <p class="text-sm text-gray-700">
                          {{post.text}}   <a href="" class="text-sm text-gray-700 hover:text-blue-600 hover:underline">...see more</a>
                        </p>
                        <button class="my-2 text-l px-2 py-1 rounded-lg text-blue-500 font-bold hover:bg-theme1">
                            See translation
                        </button>
                    </div>
                    <div class="px-0">
                        <img :src="post.image" alt="">
                    </div> 
                    <div id="action-2" class="flex items-center justify-start p-2 border-b-1  border-gray-300  ">
                        <button class="rounded-full w-8 h-8 hover:bg-theme1 hover:rounded-lg">
                                    <font-awesome-icon :icon="['fas', 'thumbs-up']" class="text-3 text-blue-500"   />
                        </button>
                        <button class="rounded-full w-8 h-8 hover:bg-theme1 hover:rounded-lg">
                                    <font-awesome-icon :icon="['fas', 'sign-language']" class="text-3 text-blue-500"   />
                        </button>
                           <a href="#" class=" text-gray-500 font-light hover:text-blue-600 hover:underline">{{post.likes}}</a> 
                           <a href="#" class="ml-2 text-gray-500 font-light hover:text-blue-600 hover:underline"> • {{post.comments.length}} comment</a> 
                    </div>
                    <div id="action-3" class="flex items-center justify-start p-2 mx-2 my-4">

                         <button class="rounded-md w-16 h-8 hover:bg-theme1 flex items-center pl-2 pr-4 ">
                                    <font-awesome-icon :icon="['fas', 'thumbs-up']" class="text-5 text-gray-500"/> 
                                    <p class=" text-sm text-gray-500 font-bold ml-1" >Like</p>
                        </button>
                        <button class="rounded-md w-24 h-8 hover:bg-theme1 flex items-center  pl-2 pr-4 ">
                                    <font-awesome-icon :icon="['fas', 'comment-dots']" class="text-5 text-gray-500"/> 
                                    <p class="text-sm text-gray-500 font-bold ml-1" >Comment</p>
                        </button>
                        <button class="rounded-md w-18 h-8 hover:bg-theme1 flex items-center  pl-2 pr-4 ">
                                    <font-awesome-icon :icon="['fas', 'share']" class="text-5 text-gray-500"/> 
                                    <p class=" text-sm text-gray-500 font-bold ml-1" >Share</p>
                        </button>
                         <button class="rounded-md w-18 h-8 hover:bg-theme1 flex items-center  pl-2 pr-4 ">
                                    <font-awesome-icon :icon="['fas', 'location-arrow']" class="text-5 text-gray-500"/> 
                                    <p class="text-sm text-gray-500 font-bold ml-1" >Send</p>
                        </button>
                     
                          
                    </div>

             </div>   
        
        </div>

       
    </div>

    <div class="col-start-7 col-end-10 ml-32 ">
        <right-sidebar />
    </div>
</div>
</template>

<script>
import LeftSidebar from "@/components/sidebar/left"
import RightSidebar from "@/components/sidebar/right"



export default {
  name: 'Home',
  components: {
    LeftSidebar,
    RightSidebar

    
  },
  
data () {
    return {
        posts : [
          {
            id: 1,
            user: {
                id : '4124v12f4',
                name : 'Mehmet Eyüpoğlu',
                title: 'Frontend Developer at YCP Bilgi Teknolojileri',
                avatar: 'https://media-exp1.licdn.com/dms/image/C4D03AQHE0-2RLxmSzA/profile-displayphoto-shrink_100_100/0/1604298775152?e=1614211200&v=beta&t=6J6JofcChpLKITbRB4P9nWNPmjP8tjpMSLfz79M1bZE',
            },
            slug: 'post-1',
            text: 'Adem ilter in CSS videolarını çevremde kime önerdiysem hep olumlu dönüşler aldım. Bu videolarda anlatılanların bir döküman halinde hızlı bir referans kaynağı olması öğrenme açısından oldukça faydalı. Notları githubda açık kaynak olarak paylaştım.',
            image: 'https://media-exp1.licdn.com/dms/image/C4D22AQFzQ4zvjAzg4A/feedshare-shrink_800-alternative/0/1608629805543?e=1611792000&v=beta&t=rscfJ9bpDMSeuYO9ge1nepwqT7Y7KFXFUIl7_apoeqE',
            comments: [],
            likes: 68,
          },
          {
            id: 2,
            user: {
                id : '65f4a5f4',
                name : 'OECD - OCDE',
                title: 'Promoted',
                avatar: 'https://media-exp1.licdn.com/dms/image/C4D0BAQFGdpghr-I1qA/company-logo_100_100/0/1607523590667?e=1616630400&v=beta&t=O57xnnkUbc3Vznoj8YK0xrOSTWx8fKEHkxWKFBdoNnA',
            },
            slug: 'post-2',
            text: 'The OECD Young Associates Programme (YAP) is an exciting opportunity that offers professional experience at the cutting edge of public policy development and analysis. The YAP is a 24-month programme designed to expose recent undergraduates to a variety of research and analytical work on major policy areas.',
            image: 'https://media-exp1.licdn.com/dms/image/sync/C5618AQG_Z-ubHmcetw/companyUpdate-article-image-shrink_627_1200/0/1607625063959?e=1611792000&v=beta&t=c3CbBCtAmhCrh9ERuIcsJK5LKeh5zAFuYzPYjgTc5f0',
            comments: [],
            likes: 39,
          },
         
          
        
        ]
     }
  },
}
</script>
<style>

</style>