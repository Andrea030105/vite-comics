<script>
export default {
    data() {
        return {

        }
    },
}
</script>
<template>
    <div class="container-fluid p-0">
        <div class="row">
            <div class="col-12">
                <div class="container-jumbotron">
                    <img src="../assets/images/jumbotron.jpg" alt="jumbotron">
                </div>
                <div class="current-series d-flex align-items-center justify-content-center">
                    current series
                </div>
            </div>
        </div>
        <section class="bg-black">
            <div class="row">
                <div class="col-12">
                    <div></div>
                </div>
            </div>
        </section>
    </div>
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

.bg-black {
    height: 10rem;
}
</style>