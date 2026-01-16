<script>
import Card from './Card.vue'
import dataFileCard from '../assets/dataFile/dataFileCard'
export default {
    components: {
        Card,
    },
    data() {
        return {
            fileCard: dataFileCard,
        }
    },
}
</script>
<template>
    <div class="container-jumbotron">
        <img src="../assets/images/jumbotron.jpg" alt="jumbotron">
    </div>
    <div class="current-series d-flex align-items-center justify-content-center">
        current series
    </div>
    <section class="bg-black py-5">
        <div class="row">
            <div class="col-12">
                <div class="d-flex flex-wrap justify-content-center">
                    <Card v-for="(items, index) in fileCard" :key="index" :dataCard="items" />
                </div>
            </div>
        </div>
        <div class="row">
            <div class="col-12">
                <div class="d-flex justify-content-center mt-5">
                    <button class="btn-load-more">
                        load more
                    </button>
                </div>
            </div>
        </div>
    </section>
</template>
<style lang="scss">
@use '../styles/partial/variables' as *;

.container-jumbotron {
    height: 17rem;
    width: 100%;
    position: relative;

    img {
        width: 100%;
        height: 100%;
        object-fit: cover;
        object-position: top;
    }
}

.current-series {
    height: 40px;
    width: 250px;
    background-color: $primaryCl;
    text-transform: uppercase;
    font-weight: 600;
    color: $whiteCl;
    font-size: 1.5rem;
    position: absolute;
    top: 320px;
    left: 70px;
}

.btn-load-more {
    color: $whiteCl;
    background-color: $primaryCl;
    text-transform: uppercase;
    padding: 5px 10px;
    border: 2px solid $primaryCl;

    &:hover {
        cursor: pointer;
        background-color: $lightBlack;
    }
}
</style>