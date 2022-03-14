<template>
    <header class="dashboard__header">
        <h2 class="dashboard__header--title">{{ title }}</h2>
        <div class="dashboard__header--user">
            <img src="./../assets/img/profile.jpeg" alt="Perfil" title="Perfil">
            <p>Andrea del Pilar Romero Forero</p>
        </div>
    </header>
</template>

<script>

export default {
    name: 'DashboardHeader',
    props: {
        title: String
    }
}

</script>

<style lang="scss" scoped>
.dashboard {
    &__header {
        padding: 20px 30px;
        display: flex;
        align-items: center;
        justify-content: space-between;
        &--user {
            width: 30%;
            display: flex;
            align-items: center;
            justify-content: space-around;
            img {
                width: 60px;
                height: 60px;
                object-fit: cover;
                object-position: center;
                border-radius: 50%;
                border: none;
            }
        }
    }
}
</style>
