<script>
export default {
    props: {
        dataCard: Object,
    }
}
</script>
<template>
    <div class="card-comics">
        <img :src="dataCard.thumb" alt="">
        <h4>
            {{ dataCard.series }}
        </h4>
    </div>
</template>
<style lang="scss">
@use '../styles/partial/variables' as *;

.card-comics {
    width: 15%;
    display: flex;
    align-items: center;
    flex-direction: column;
    border: 1px solid $whiteCl;

    img {
        width: 50%;
    }

    h4 {
        text-transform: uppercase;
        color: $whiteCl;
        font-size: 1rem;
        text-align: center;
        margin-top: 1rem;
    }
}
</style>