<script>
export default {
    data() {
        return {
            menu: [
                {
                    text: 'Characters',
                    status: false,
                },
                {
                    text: 'Comics',
                    status: true,
                },
                {
                    text: 'Movies',
                    status: false,
                },
                {
                    text: 'Tv',
                    status: false,
                },
                {
                    text: 'Games',
                    status: false,
                },
                {
                    text: 'Collectibles',
                    status: false,
                },
                {
                    text: 'Videos',
                    status: false,
                },
                {
                    text: 'Fans',
                    status: false,
                },
                {
                    text: 'News',
                    status: false,
                },
                {
                    text: 'Shop',
                    status: false,
                },
            ],
        }
    },
};
</script>
<template>
    <header class=" d-flex align-items-center">
        <div class="container">
            <div class="row">
                <div class="col-4">
                    <div class="logo-container">
                        <img src="/src/assets/images/dc-logo.png" alt="logo">
                    </div>
                </div>
                <div class="col-8 d-flex align-items-center">
                    <ul class="menu-list d-flex">
                        <li v-for="(items, index) in menu" :key="index" :class="(items.status) ? 'status-true' : ''">
                            <a href="#">{{ items.text }}</a>
                            <div class="page-true" v-if="(items.status)"></div>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </header>
</template>
<style lang="scss">
@use '../styles/partial/variables' as *;

header {
    height: 75px;
}

.logo-container {
    img {
        width: 15%;
    }
}

.menu-list {
    list-style-type: none;
    margin: 0;

    li {
        margin-right: 1rem;
        text-transform: uppercase;
        font-size: .8rem;
        font-weight: 700;
        display: flex;
        align-items: center;
        flex-direction: column;

        a {
            text-decoration: none;
            color: #000;
            margin-bottom: .5rem;

            &:hover {
                color: $primaryCl;
            }
        }

        &.status-true a {
            color: $primaryCl;
        }

        .page-true {
            height: 5px;
            width: 40px;
            background-color: $primaryCl;
        }
    }
}
</style>
