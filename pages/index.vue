<template>
  <div>
    <header class="flex items-center justify-between py-4 px-6 bg-gray-900">
      <div>
        <span class="text-3xl text-white">Work</span><span class="text-3xl text-indigo-200">cation</span>
      </div>
      <div>
        <svg class="h-6 fill-current text-gray-600" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 0 124 124">
          <path d="M112,6H12C5.4,6,0,11.4,0,18s5.4,12,12,12h100c6.6,0,12-5.4,12-12S118.6,6,112,6z" />
          <path d="M112,50H12C5.4,50,0,55.4,0,62c0,6.6,5.4,12,12,12h100c6.6,0,12-5.4,12-12C124,55.4,118.6,50,112,50z" />
          <path d="M112,94H12c-6.6,0-12,5.4-12,12s5.4,12,12,12h100c6.6,0,12-5.4,12-12S118.6,94,112,94z" />
        </svg>
      </div>
    </header>
    <div class="flex justify-between bg-gray-800 py-4 px-6">
      <input class="bg-gray-900 py-3 px-3 rounded-lg" type="text" placeholder="Search by keywords">
      <button class="bg-gray-600 px-4 rounded-lg text-white">
        Filters
      </button>
    </div>
    <main class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 bg-gray-200 py-6 px-6">
      <div v-for="imovel in imoveis" :key="imovel.id" class="mt-12 mx-4">
        <h4 class="text-2xl text-gray-800">
          {{ imovel.titulo }}
        </h4>
        <p class="mt-2">
          {{ imovel.descricao }}
        </p>

        <div class="mt-4">
          <img class="rounded-lg" src="https://images.unsplash.com/photo-1512917774080-9991f1c4c750?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1950&q=80">
        </div>

        <div class="px-3 -mt-12 z-10 relative">
          <div class="py-5 px-5 bg-white rounded-lg">
            <span class="rounded-lg bg-teal-200 py-1 px-2 text-sm font-bold">PLUS</span> <span class="text-gray-600 font-medium text-sm">3 BEDS - 2 BATHS</span>
            <h5 class="py-2 font-bold text-lg">
              Modern home in city center
            </h5>
            <span class="font-semibold">$1,400</span> <span class="font-light text-sm text-gray-700">/wk</span>
            <p class="mt-2 font-sm font-semibold text-gray-700">
              34 Reviews
            </p>
          </div>
        </div>
      </div>
    </main>
  </div>
</template>

<script>

export default {
  name: 'Principal',
  data () {
    return {
      imoveis: [
        {
          id: 1, titulo: 'Los Angeles', descricao: 'Live like the stars in these luxurious Southern California estates.'
        },
        {
          id: 2, titulo: 'Paris', descricao: 'Live like the stars in these luxurious North French estates.'
        },
        {
          id: 3, titulo: 'Grécia', descricao: 'Live like the stars in these luxurious Greek estates.'
        },
        {
          id: 4, titulo: 'Itália', descricao: 'Live like the stars in these luxurious Italian estates.'
        }
      ]
    }
  }
}
</script>
