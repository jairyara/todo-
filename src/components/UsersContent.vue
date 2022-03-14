<template>

<div class="dashboard__content">

    <div class="dashboard__content--add">
        <button class="btn btn-primary">nuevo usuario</button>
    </div>

    <table class="dashboard__content--users">
        <thead>
            <tr>
                <th>Id</th>
                <th>Nombre</th>
                <th>Usuario</th>
                <th>Email</th>
                <th>Dirección completa</th>
                <th>Compañía</th>
                <th>Listado todos</th>
            </tr>
        </thead>
        <tbody>
            <tr v-for="user in info" :key="user.id">
                <td>{{ user.id }}</td>
                <td>{{ user.name }}</td>
                <td>{{ user.username }}</td>
                <td>{{ user.email }}</td>
                <td>{{ `${user.address.street} - ${user.address.suite} - ${user.address.city}`}}</td>
                <td>{{ user.company.name }}</td>
                <td><router-link v-bind:to="'/todos/'+ user.id" >Ver todos</router-link></td>
            </tr>
        </tbody>
    </table>
</div>

</template>

<script>

import axios from 'axios';

export default {
    name: 'UsersContent',
    data() {
        return {
            info :  null
        }
    },
    mounted() {
        this.getAll();
    },
    methods: {
        getAll() {
            axios
            .get('https://jsonplaceholder.typicode.com/users')
                .then( response => {
                    this.info = response.data
                })
                .catch( e => console.error( e ))
        },
    }
}

</script>

<style lang="scss" scoped>

.dashboard__content {

    &--add {
        display: flex;
        margin-bottom: 40px;
    }

    &--users {
        width: 100%;
        border-collapse: collapse;
        border: 2px solid #0054FE;

        thead {
            background-color: #0054FE;
            color: white;
            font-weight: 700;
        }

        tbody {
            & tr:nth-child(odd) {
                background-color: rgba(#0054FE, 0.25);
            }
        }

        th, td {
            padding: 20px;
        }
    }

}
</style>