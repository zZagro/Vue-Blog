<template>
    <router-link :to="to" class="link" :class="{ active: isActive }">
        <i class="icon" :class="icon" />
        <Transition
        enter-active-class="fade-transition fade-no-opacity"
        enter-to-class="fade-transition fade-full-opacity"
        leave-active-class="fade-transition fade-no-opacity"
        leave-to-class="fade-transition fade-no-opacity"
        fade>
            <span v-if="!collapsed">
                <slot />
            </span>
        </Transition>
    </router-link>
</template>

<script>
import { computed } from 'vue'
import { useRoute } from 'vue-router'
import { collapsed } from './state'

export default {
    props: {
        to: { type: String, required: true },
        icon: { type: String, required: true }
    },
    setup(props) {
        const route = useRoute()
        const isActive = computed(() => route.path === props.to)
        return { isActive, collapsed }
    }
}
</script>

<style scoped>
.fade-transition {
    transition: opacity .1s linear;
}

.fade-no-opacity {
    opacity: 0;
}

.fade-full-opacity {
    opacity: 1;
}

.link {
    display: flex;
    align-items: center;

    cursor: pointer;
    position: relative;
    font-weight: 400;
    user-select: none;

    margin: 0.1em 0;
    padding: 0.4em;
    border-radius: 0.25em;
    height: 1.5em;

    color: white;
    text-decoration: none;
}

.link:hover {
    background-color: var(--clr-indigo500);
}

.link.active {
    background-color: var(--clr-indigo700);
}

.link .icon {
    flex-shrink: 0;
    width: 25px;
    margin-right: 10px;
    color: white;
}
</style>