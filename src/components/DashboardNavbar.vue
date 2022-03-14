<template>
    <aside class="dashboard__nav">
        <h1 class="dashboard__nav--title">To do list</h1>
        <nav class="dashboard__nav--menu">
            <li>
                <router-link to="/usuarios">usuarios</router-link>
            </li>
            <li>
                <router-link to="/">salir</router-link>
            </li>
        </nav>
    </aside>
</template>

<script>

export default {
    name: 'NavbarDashboard'
}
</script>


<style lang="scss" scoped>
.dashboard {

    &__nav {
        width: 100%;
        height: calc(100% - 40px);
        grid-area: aside;
        background-color: white;

        &--title {
            height: 90px;
            margin: 0;
            display: grid;
            place-content: center;
        }

        &--menu {
            padding: 20px;
            display: flex;
            flex-direction: column;
            align-items: flex-start;
            justify-content: space-around;

            li {
                margin-bottom: 20px;
                list-style: none;

                a {
                    text-transform: capitalize;
                    text-decoration: none;
                }
            }
        }
    }
}

</style>