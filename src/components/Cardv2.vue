<script>

export default {
    name: 'UserCard',
    props: {
        information: Object,
        photo: ImageData,
    }
}

</script> 

<template>
    <div class="card">
        <div class="picture">
            <img :src="require(`@/assets/${information.photo1}`)" alt="">
        </div>
        <div class="sepator"></div>
        <div class="zone_txt">
            <div>
                <h2 class="titre_card"><b>{{ information.titre }}</b></h2>
                <p class="decription_card">{{ information.description }}</p>
            </div>
            <div>
                <hr>
                <div class="all_link">
                    <a :href="information.lien" target="_blank">Accès Github</a>
                    <a v-if="information.lien2" :href="information.lien2" target="_blank">Accès site</a>
                </div>
            </div>
        </div>
        <div class="sepator"></div>
        <div class="picture">
            <img :src="require(`@/assets/${information.photo2}`)" alt="">
        </div>
    </div>
</template>

<style scoped>
.card {
    display: flex;
    background-color: #d9d4e7;
    border: solid black 2.5px;
}

.zone_txt {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    text-align: justify;
    padding: 3% 1% 1% 1%;
}

a {
    text-decoration: underline;
}

.titre_card {
    color: #0e172c;
    text-align: center;
}

.decription_card{
    font-size: 85%;
}

.sepator{
    border: solid black 2.5px;
}

.all_link{
    display: flex;
    justify-content: space-between;
}

</style>
