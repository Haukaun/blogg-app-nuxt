<template>
    <div class="px-5 shadow-lg md:flex items-center justify-between w-full">
        <div class="">
            <img src="../../static/Capture-removebg-preview.png" alt="" class="h-28 cursor-pointer">
        </div>

        <button data-collapse-toggle="navbar-default" type="button" @click="navbarOpen()"
            class="absolute text-sm rounded-lg right-11 top-11 md:hidden" aria-controls="navbar-default"
            aria-expanded="false">
            <svg v-if="!open" class="w-6 h-6" aria-hidden="true" fill="currentColor" viewBox="0 0 20 20"
                xmlns="http://www.w3.org/2000/svg">
                <path fill-rule="evenodd"
                    d="M3 5a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 10a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 15a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1z"
                    clip-rule="evenodd"></path>
            </svg>
            <div v-else>
                <svg xmlns="http://www.w3.org/2000/svg" class="w-6 h-5" aria-hidden="true" fill="currentColor"
                    viewBox="0 0 24 24">
                    <path fill-rule="evenodd"
                        d="M24 20.188l-8.315-8.209 8.2-8.282-3.697-3.697-8.212 8.318-8.31-8.203-3.666 3.666 8.321 8.24-8.206 8.313 3.666 3.666 8.237-8.318 8.285 8.203z"
                        clip-rule="evenodd" />
                </svg>
            </div>
        </button>

        <ul class="md:flex md:items-center md:px-0 px-14 md:pb-0 pb-10 md:static absolute 
        md:w-auto w-full top-28 duration-700 ease-in" :class="[open ? 'left-0' : 'left-[-100%]']">
            <li class="md:mx-4 md:my-0 my-6" v-for="link in links" :key="link.name">
                <a :href="link.url" class="text-xl hover:text-gray-800">{{ link.name }}</a>
            </li>
        </ul>
    </div>
</template>


<script>

export default {
    data() {
        return {
            open: false,
            links: [
                {
                    name: 'Home',
                    url: '/'
                },
                {
                    name: 'Other blogs',
                    url: '/other-blogs'
                },
                {
                    name: 'Services',
                    url: '/services'
                },
                {
                    name: 'Contact us',
                    url: '/contact'
                }
            ],
        }
    },

    methods: {
        navbarOpen() {
            this.open = !this.open
        }
    },
}
</script>