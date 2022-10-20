<template>
    <div>
        <div
            class="min-h-screen flex flex-col flex-auto flex-shrink-0 antialiased bg-white dark:bg-gray-700 text-black dark:text-white">
            <div class="h-full ml-14 mt-14 mb-10 md:ml-64">
                <div class="grid grid-cols-1 p-2 gap-10">
                    <div
                        class="relative flex flex-col min-w-0 break-words bg-gray-50 dark:bg-gray-800 w-full shadow-lg rounded">
                        <div class="rounded-t mb-0 px-0 border-0">
                            <div class="flex flex-wrap items-center px-4 py-2">
                                <div class="relative w-full max-w-full flex-grow flex-1">
                                    <h3 class="font-semibold text-base text-gray-900 dark:text-gray-50">PRODUTOS</h3>
                                </div>

                                <div class="flex-1 flex justify-center px-2 lg:ml-6 lg:justify-end">
                                    <div class="max-w-lg w-full lg:max-w-xs">
                                        <label for="search" class="sr-only"> </label>
                                        <form methode="get" action="#" class="relative z-50">
                                            <button type="submit" id="searchsubmit"
                                                class="absolute inset-y-0 left-0 pl-3 flex items-center pointer-events-none">
                                                <svg class="h-5 w-5 text-gray-400" fill="currentColor"
                                                    viewBox="0 0 20 20">
                                                    <path fill-rule="evenodd"
                                                        d="M8 4a4 4 0 100 8 4 4 0 000-8zM2 8a6 6 0 1110.89 3.476l4.817 4.817a1 1 0 01-1.414 1.414l-4.816-4.816A6 6 0 012 8z"
                                                        clip-rule="evenodd"></path>
                                                </svg>
                                            </button>
                                            <input type="text" name="s" id="s"
                                                class="block w-full pl-10 pr-3 py-2 border border- rounded-md leading-5 bg-white-200 text-gray-300 placeholder-gray-400 focus:outline-none focus:bg-white focus:text-gray-900 sm:text-sm transition duration-150 ease-in-out"
                                                placeholder="Pesquisar produto">
                                        </form>
                                    </div>
                                </div>
                                <div class="relative w-full max-w-full flex-grow flex-1 text-right">
                                    <router-link to="/products/create"
                                        class="bg-blue-500 dark:bg-gray-100 text-white active:bg-blue-600 dark:text-gray-800 dark:active:text-gray-700 text-xs font-bold uppercase px-3 py-1 rounded outline-none focus:outline-none mr-1 mb-1 ease-linear transition-all duration-150">
                                        CRIAR NOVO PRODUTO</router-link>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Clientes  -->
                <div class="mt-2 mx-2">
                    <div class="w-full overflow-hidden rounded-lg shadow-xs">
                        <div class="w-full overflow-x-auto">
                            <table class="w-full">
                                <thead>
                                    <tr
                                        class="text-xs font-semibold tracking-wide text-left text-gray-500 uppercase border-b dark:border-gray-700 bg-gray-50 dark:text-gray-400 dark:bg-gray-800">
                                        <th class="px-4 py-3">ID</th>
                                        <th class="px-4 py-3">Nome do produto</th>
                                        <th class="px-4 py-3">Preço custo</th>
                                        <th class="px-4 py-3">Preço Venda</th>
                                        <th class="px-4 py-3">Estoque</th>
                                        <th class="px-4 py-3">ação</th>
                                    </tr>
                                </thead>

                                <tbody class="bg-white divide-y dark:divide-gray-700 dark:bg-gray-800">

                                    <tr v-for="(product, index) in products" :key="index"
                                        class="bg-gray-50 dark:bg-gray-800 hover:bg-gray-100 dark:hover:bg-gray-900 text-gray-700 dark:text-gray-400">
                                        <td class="px-4 py-3">
                                            <div class="flex items-center text-sm">
                                                <div>

                                                    <p class="text-xs text-gray-600 dark:text-gray-400">10
                                                    </p>
                                                </div>
                                            </div>
                                        </td>
                                        <p class="font-semibold px-4 py-3 text-sm"> {{ product.name }} </p>
                                        <td class="px-4 py-3 text-sm"> {{ product.price_c }}</td>
                                        <td class="px-4 py-3 text-sm"> {{ product.price }}</td>
                                        <td class="px-4 py-3 text-sm"> {{ product.stock }}</td>
                                        <td class="py-4 px-3 text-sm">
                                            <div class="flex item-center ">
                                                <Nuxt-link :to="`/products/update/${product._id}`"
                                                    class="w-4 mr-2 transform hover:text-purple-500 hover:scale-110">
                                                    <svg xmlns="http://www.w3.org/2000/svg" fill="none"
                                                        viewBox="0 0 24 24" stroke="currentColor">
                                                        <path stroke-linecap="round" stroke-linejoin="round"
                                                            stroke-width="2"
                                                            d="M15.232 5.232l3.536 3.536m-2.036-5.036a2.5 2.5 0 113.536 3.536L6.5 21.036H3v-3.572L16.732 3.732z" />
                                                    </svg>
                                                </Nuxt-link>

                                                <div @click="deleteProduct(product._id, index)"
                                                    class="w-4 mr-2 transform hover:text-purple-500 hover:scale-110">
                                                    <svg xmlns="http://www.w3.org/2000/svg" fill="none"
                                                        viewBox="0 0 24 24" stroke="currentColor">
                                                        <path stroke-linecap="round" stroke-linejoin="round"
                                                            stroke-width="2"
                                                            d="M19 7l-.867 12.142A2 2 0 0116.138 21H7.862a2 2 0 01-1.995-1.858L5 7m5 4v6m4-6v6m1-10V4a1 1 0 00-1-1h-4a1 1 0 00-1 1v3M4 7h16" />
                                                    </svg>
                                                </div>
                                            </div>
                                        </td>
                                    </tr>
                                </tbody>
                            </table>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>

</template>



<script>


export default {
    data() {
        return {
            products: [],
            error: ""
        }
    },
    mounted() {
        this.getProducts()
    },

    methods: {
        async getProducts() {

            await this.$axios.$get("/products").then(success => {
                this.products = success

            }).catch(error => {
                this.error = "Produtos não encontrados"
            });
        },
        async deleteProduct(id, index) {
            let confirmation = confirm("Deseja realmente deletar?")

            if (confirmation == true) {
                await this.$axios.$delete(`/products/${id}`).then(success => {
                    alert("Removido com sucesso!")
                    this.products.splice(index, 1)
                })

            }


        }

    }
}
</script>