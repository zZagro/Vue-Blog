<template>
    <h1>The sidebar is {{ collapsed ? 'closed' : 'open' }}</h1>
    <button @click="toggleSidebar">Toggle Sidebar</button>
</template>

<script>
import { collapsed, toggleSidebar } from '../components/nav/state'

export default {
    name: 'DashBoard',
    setup() {
        return { collapsed, toggleSidebar }
    }
}
</script>