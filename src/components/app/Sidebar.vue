<template>
    <ul class="sidenav app-sidenav open">
        <li class="waves-effect waves-orange pointer" >
        <router-link
                v-for="link in links"
                :key="link.url"
                active-class="active"
                :to="link.url"
                :exact="link.exact"
        >
            <a href="#"   > {{ link.title }}</a>
        </router-link>
        </li>

        <!--<li>
            <a href="#" class="waves-effect waves-orange pointer">Счет</a>
        </li>
        <li>
            <a href="#" class="waves-effect waves-orange pointer">История</a>
        </li>
        <li>
            <a href="#" class="waves-effect waves-orange pointer">Планирование</a>
        </li>
        <li>
            <a href="#" class="waves-effect waves-orange pointer">Новая запись</a>
        </li>
        <li>
            <a href="#" class="waves-effect waves-orange pointer">Категории</a>
        </li>-->
    </ul>
</template>

<script>
    export default {
        name: "Sidebar",
        props: ['value'],
        data: () => ({
            links: [
                {title: 'Счет', url: '/', exact: true},
                {title: 'История', url: '/history'},
                {title: 'Планирование', url: '/planning'},
                {title: 'Новая запись', url: '/record'},
                {title: 'Категории', url: '/categories'}
            ]
        })
    }
</script>

<style scoped>

</style>
