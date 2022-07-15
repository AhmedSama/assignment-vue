<template>
    <h1 class="title mb">{{data.title}}</h1>
    <Tags :tags="data.tags" />
    <Image :image="data.image" />
     <div class="flex justify-between align-center mb-2">
        <div class="flex align-center gap">
            <span class="material-icons">schedule</span>
            <div class="time">{{data.datetime}}</div>
        </div>
        <div class="flex align-center gap">
            <RoundedGroup>
                <Btn :clickevent="share" className="flex align-center gap">
                    <span class="material-icons">share</span> share
                </Btn>
            </RoundedGroup>
            <RoundedGroup>
              <Btn className="flex align-center gap">
                <span class="material-icons-outlined">article</span> Enable reading mode
              </Btn>
              <Btn>A-</Btn>
              <Btn>A</Btn>
              <Btn>A+</Btn>
            </RoundedGroup>
        </div>
     </div>
     <div class="articles">
        <Content v-for="text in data.content" :key="text" :text="text" />
    </div>
</template>

<script>
import Tags from './Tags.vue'
import Image from './Image.vue'
import RoundedGroup from './RoundedGroup.vue'
import Btn from './Btn.vue'
import Content from './Content.vue'

    export default{
        props : {
            data : Object
        },
        components : {
            Tags,
            Image,
            RoundedGroup,
            Btn,
            Content
        },
        methods : {
             share : async()=>{
                try {
                    await navigator.share({
                        title: 'Test Assignment',
                        text: 'just a test',
                        url: window.location.href
                    })
                }
                catch(err) {
                    console.log(err)
                }
            }
        }
    }
</script>

<style scoped>
    
.title{
  font-size: 19px;
  font-weight: 500;
}
</style>