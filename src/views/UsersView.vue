<template>
    
    <div class="dashboard">
        <DashboardHeader title="Usuarios" />
        <DashboardNavbar />
        <UsersContent />
    </div>
    
</template>

<script>

import DashboardHeader from '@/components/DashboardHeader.vue'
import DashboardNavbar from '@/components/DashboardNavbar.vue'
import UsersContent from '@/components/UsersContent.vue'

export default {
    name: 'UsersView',
    components: {
        DashboardHeader,
        DashboardNavbar,
        UsersContent
    }
}

</script>