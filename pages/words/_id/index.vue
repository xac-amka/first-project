<template>
    <div class="single-word">
        <p>Breadcrumb Home/Words/{{ $route.params.id }}</p>
        <h1>{{ word.word }}</h1>
        <div>
            <img class="image" :src="word.thumbnail" :alt="word.word">
        </div>
        <p>{{ word.description }}</p>
    </div>
</template>
<script>
export default {
    // context => API description
    asyncData(context){
        return new Promise((resolve, reject) => {
            setTimeout(()=>{
                resolve({
                    word: [
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
                    ].find(el => el.id === context.params.id)
                })
            }, 1500)
        })
    }
}
</script>
<style scoped>
.single-word {
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
    padding: 30px;
    flex-flow: column;
}
.image {
    width: 100%;
    height: 300px;
}
</style>