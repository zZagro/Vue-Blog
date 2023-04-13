<template>
    <div class="sidebar" :style="{ width: sidebarWidth }" @mouseenter="toggleSidebar" @mouseleave="toggleSidebar">
        <h1>
            <img class="sidebar-img" :style="{ width: logoWidth }" alt="Vue logo" src="../../assets/logo.png">
            <span v-if="!collapsed">
                <div>Blog</div>
            </span>
        </h1>

        <SidebarLink to="/" icon="fas fa-home">Home</SidebarLink>
        <SidebarLink to="/recent" icon="fas fa-clock">Recent</SidebarLink>
        <SidebarLink to="/blog" icon="fas fa-newspaper">Blog</SidebarLink>
        <SidebarLink to="/dashboard" icon="fas fa-columns">Dashboard</SidebarLink>
        <SidebarLink to="/image" icon="fas fa-image">Images</SidebarLink>

        <span class="collapse-icon" :class="{ 'rotate-180': collapsed }">
            <i class="fas fa-angle-double-left" />
        </span>
    </div>
</template>

<script>
import SidebarLink from './SidebarLink'
import { collapsed, toggleSidebar, sidebarWidth, logoWidth } from './state';

export default {
    name: 'Sidebar-nav',
    props: {

    },
    components: {
        SidebarLink,
    },
    setup() {
        return { collapsed, toggleSidebar, sidebarWidth, logoWidth }
    }
}
</script>

<style scoped>
.sidebar {
    color: white;
    background-color: var(--clr-indigo950);

    float: left;
    position: fixed;
    z-index: 1;
    top: 0;
    left: 0;
    bottom: 0;
    padding: 0.5em;

    transition: 0.3s ease;

    display: flex;
    flex-direction: column;
}

.sidebar-img {
    transition: .3s ease;
}

.collapse-icon {
    position: absolute;
    bottom: 0;
    padding: 0.75em;

    color: rgba(255, 255, 255, 0.7);

    transition: 0.2s linear;
}

.rotate-180 {
    transform: rotate(180deg);
    transition: 0.2s linear;
}
</style>