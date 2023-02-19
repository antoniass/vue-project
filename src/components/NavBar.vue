<script setup>
import { RouterLink, RouterView } from "vue-router"
</script>

<!-- Här lägger ni en navbar och istället för href så använder ni RouterLink -->
<template>
    <ul class="nav justify-content-center">
        <li class="nav-item">
            <RouterLink class="nav-link" aria-current="page" to="/">{{ home }}</RouterLink>
        </li>
        <li class="nav-item">
            <RouterLink class="nav-link" to="/about">{{ about }}</RouterLink>
        </li>
    </ul>
<RouterView />
</template>

<script>
export default {
    data() {
        return {
            home: "Hem",
            about: "Dryck"
        }
    }
}
</script>

<style scoped>
.nav {
    height: 50px;
    margin-top: 1rem;
}

.nav-link {
    color: black;
}

.nav-link:hover {
    color: black;
    background-color: gainsboro;
}
</style>
