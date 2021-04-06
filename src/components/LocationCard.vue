<template>
<div v-if="adress.county" class="location-card">
    <div class="adress-data col">
        {{adress.road}} <br/>
        {{adress.state}} {{adress.country}} <br/>
        {{adress.county}} <br/>
        {{adress.neighbourhood}} <br/>
        {{adress.postcode}} <br/>
    </div>
    <div class="adress-image col">
        <img :src='countyPic'/>
    </div>
</div>
</template>

<script>

export default {
    name: 'LocationCard',
    props: {
        adress: Object
    },
    computed: {
        countyPic(){
            return `https://source.unsplash.com/1600x900/?${this.adress.country},${this.adress.county}`;
        } 
    }
}
</script>

<style scoped>
.location-card{
    position: relative;
    display: flex;
    align-items: center;
    justify-content: center;
    background-color: rgb(34, 34, 34);
    color: white;
    padding: 15px 40px;
    border-radius: 4px;
}
.col{
    width: 50%;
    padding: 10px;
}
img{
    max-width: 60%;
}
.adress-image {
    text-align: left;
}
.adress-data{
    text-align: right;
}
</style>