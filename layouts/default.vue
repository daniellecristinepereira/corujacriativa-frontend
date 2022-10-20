<template>
    <div>
        <!-- Menu -->
        <div class="bg-green-300 fixed w-full flex items-center justify-between text-green-900 z-12">
            <!-- Profile -->
            <div
                class="flex items-center justify-start md:justify-center pl-3 w-14 md:w-64 h-14 bg-green-300 border-none">
                <img class="w-10 h-8 md:w-10 md:h-10 mr-4 rounded-md overflow-hidden" src="foto.png" />
                <span class="hidden md:block">Danielle</span>
            </div>
            <!--search  -->
            <div class="flex justify-between items-center bg-green-300 header-right">
                <div class="pt-2 relative mx-auto text-gray-600">
                    <input
                        class="border-2 border-gray-300 bg-white h-10 px-5 pr-16 rounded-lg text-sm focus:outline-none"
                        type="search" name="search" placeholder="Pesqueise aqui Dona Coruja">
                    <button type="submit" class="absolute right-0 top-0 mt-5 mr-4">
                        <svg class="text-gray-600 h-4 w-4 fill-current" xmlns="http://www.w3.org/2000/svg"
                            xmlns:xlink="http://www.w3.org/1999/xlink" version="1.1" id="Capa_1" x="0px" y="0px"
                            viewBox="0 0 56.966 56.966" style="enable-background:new 0 0 56.966 56.966;"
                            xml:space="preserve" width="512px" height="512px">
                            <path
                                d="M55.146,51.887L41.588,37.786c3.486-4.144,5.396-9.358,5.396-14.786c0-12.682-10.318-23-23-23s-23,10.318-23,23  s10.318,23,23,23c4.761,0,9.298-1.436,13.177-4.162l13.661,14.208c0.571,0.593,1.339,0.92,2.162,0.92  c0.779,0,1.518-0.297,2.079-0.837C56.255,54.982,56.293,53.08,55.146,51.887z M23.984,6c9.374,0,17,7.626,17,17s-7.626,17-17,17  s-17-7.626-17-17S14.61,6,23.984,6z" />
                        </svg>
                    </button>
                </div>
                <!-- log out-->
                <ul class="flex items-center">
                    <li>
                        <div class="block w-px h-6 mx-3 bg-gray-400 dark:bg-gray-800"></div>
                    </li>
                    <li>
                        <a href="#" class="flex items-center mr-4 hover:text-gray-600">
                            <span class="inline-flex mr-1">
                                <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"
                                    xmlns="http://www.w3.org/2000/svg">
                                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                        d="M17 16l4-4m0 0l-4-4m4 4H7m6 4v1a3 3 0 01-3 3H6a3 3 0 01-3-3V7a3 3 0 013-3h4a3 3 0 013 3v1">
                                    </path>
                                </svg>
                            </span>
                            Sair
                        </a>
                    </li>
                </ul>
            </div>
        </div>
    <div>
</div>
<!-- Menu Lateral -->
        <div
            class="fixed flex flex-col top-14 left-0 w-12 hover:w-64 md:w-64 bg-pink-300 h-full text-black transition-all duration-300 border-none z-10 sidebar">
            <div class="overflow-y-auto overflow-x-hidden flex flex-col justify-between flex-grow">
                <ul class="flex flex-col py-4 space-y-1">
                    <li class="px-16 hidden md:block">
                        <div class="flex flex-row items-center h-8">
                            <div class="text-lg font-medium tracking-wide text-black uppercase">Menu</div>
                        </div>
                    </li>

                    <Nuxt-link to="dashboard"
                        class="relative flex flex-row items-center h-11 focus:outline-none hover:bg-green-300 border-l-4 border-transparent hover:border-pink-500 dark:hover:bg-green-300 pr-6">
                        <span class="inline-flex justify-center items-center ml-4">
                        <span class="ml-2 text-sm tracking-wide truncate">Dashboard</span>
                        </span>
                    </Nuxt-link>

                    <Nuxt-link to="customers"
                        class="relative flex flex-row items-center h-11 focus:outline-none hover:bg-green-300 border-l-4 border-transparent hover:border-pink-500 dark:hover:border-gray-800 pr-6">
                        <span class="inline-flex justify-center items-center ml-4">
                        <span class="ml-2 text-sm tracking-wide truncate">Clientes</span>
                        </span>
                    </Nuxt-link>

                    <Nuxt-link to="products"
                        class="relative flex flex-row items-center h-11 focus:outline-none hover:bg-green-300 border-l-4 border-transparent hover:border-pink-500 dark:hover:border-gray-800 pr-6">
                        <span class="inline-flex justify-center items-center ml-4">
                            <span class="ml-2 text-sm tracking-wide truncate">Produtos</span>
                        </span>
                    </Nuxt-link>

                    <Nuxt-link to="provider"
                        class="relative flex flex-row items-center h-11 focus:outline-none hover:bg-green-300 border-l-4 border-transparent hover:border-pink-500 dark:hover:border-gray-800 pr-6">
                        <span class="inline-flex justify-center items-center ml-4">
                            <span class="ml-2 text-sm tracking-wide truncate">Fornecedores</span>
                        </span>
                    </Nuxt-link>

                    <li class="px-8 hidden md:block">
                        <div class="flex flex-row items-center mt-5 h-8">
                            <div class="text-lg font-medium tracking-wide text-black uppercase">Configurações</div>
                        </div>
                    </li>
                    <Nuxt-link to="profile"
                        class="relative flex flex-row items-center h-11 focus:outline-none hover:bg-green-300 border-l-4 border-transparent hover:border-pink-500 dark:hover:border-gray-800 pr-6">
                        <span class="inline-flex justify-center items-center ml-4">
                        </span>
                        <span class="ml-2 text-sm tracking-wide truncate">Perfil</span>
                    </Nuxt-link>

                    <Nuxt-link to="settings"
                        class="relative flex flex-row items-center h-11 focus:outline-none hover:bg-green-300 border-l-4 border-transparent hover:border-pink-500 dark:hover:border-gray-800 pr-6">
                        <span class="inline-flex justify-center items-center ml-4">
                        </span>
                        <span class="ml-2 text-sm tracking-wide truncate">Configurações</span>
                    </Nuxt-link>
                    <Nuxt-link to="settings"
                        class="relative flex flex-row items-center h-11 focus:outline-none hover:bg-green-300 border-l-4 border-transparent hover:border-pink-500 dark:hover:border-gray-800 pr-6">
                        <span class="inline-flex justify-center items-center ml-4">
                        </span>
                        <span class="ml-2 text-sm tracking-wide truncate">Configurações</span>
                    </Nuxt-link>
                </ul>
            </div>
        </div>
        <Nuxt />
    </div>
</template>

<style>
.header-right {
    width: calc(100% - 3.5rem);
}

.sidebar:hover {
    width: 16rem;
}
</style>