<template>
    <section class="section">
        <article class = "hero is-danger">
            <div class = "hero-body">
                <div class = "container">
                    <h1 class="title">{{dogName.toUpperCase()}}</h1>
                    <h2 class="subtitle">많이 사랑해주세요 :)</h2>
                </div>
            </div>
        </article>

        <article class="notification is-success">
        <div class="columns">
            <div v-for="image in images" :key="image" class= "column">
            <figure class = "image is-square">
                <img :src="image" alt="">
            </figure>
            </div>
        </div>
        </article>

        <article class="message is-danger">
            <div class="message-header">
                <p>{{dogName.toUpperCase()}}의 아품종</p>
            </div>
            <div class="message-body">
                <ol>
                    <li v-for="subdog in dogList" :key="subdog">
                        {{subdog.toUpperCase()}}
                    </li>
                </ol>
            </div>
        </article>
    </section>
</template>
<script>
    import axios from 'axios';

    export default{
        async asyncData({ params }) 
        {
            let maxImg = 4;
            let images =[];
            for(let i=0; i<maxImg; i++){
                const image = await axios.get(`https://dog.ceo/api/breed/${params.dog}/images/random`);
                images.push(image.data.message);
            }
            const list = await axios.get(`https://dog.ceo/api/breed/${params.dog}/list`);
            return {
                dogName: params.dog,
                images: images,
                dogList: list.data.message
            };
        }
    }
</script> <!-- _dog의 사용으로 parmas.dog !-->