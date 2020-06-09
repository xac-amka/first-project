<template>
  <section class="words">
      <Word v-for="word in words" :key="word.id"
      :thumbnail="word.thumbnail"
      :word="word.word"
      :id="word.id"
      :description="word.description"/>
  </section>
</template>

<script>
import Word from '@/components/Word'

export default {
    components: {
        Word
    },
    asyncData(){
        return new Promise((resolve, reject) => {
            setTimeout(()=>{
                resolve({
                    words: [
                        {
                            id:'7xa3',
                            word: 'Cruel',
                            thumbnail: 'https://cdn0.iconfinder.com/data/icons/king/431/king-010-512.png',
                            description: 'Description: mean, heartless'
                        },
                        {
                            id:'9bac',
                            word: 'Defy',
                            thumbnail: 'https://previews.123rf.com/images/icetray/icetray1602/icetray160210094/51928522-defy-word-on-keyboard-button.jpg',
                            description: 'Description: resist, challenge'
                        },
                        {
                            id:'51o9',
                            word: 'Cranky',
                            thumbnail: 'https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcTtUDSgPvQ64TYhC6uILgsrj9Wmg0keuvfOQ__kZkjcGMjr4iqm&usqp=CAU',
                            description: 'Description: cross, irritable'
                        }
                    ]
                })
            }, 1500)
        })
    }
}
</script>

<style scoped>
.words {
    display: flex;
    flex-flow: row wrap;
    justify-content: center;
    align-items: center;

}

</style>