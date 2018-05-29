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
    </section>
</template>
<script>
    export default{
        asyncData({params}){
            return {
                dogName: params.dog
            };
        }
    }
</script> <!-- _dog의 사용으로 parmas.dog !-->