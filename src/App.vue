<template>
<main class="h-screencontainer mx-auto p-8 flex">
  <div class="form max-h-315 max-w-full shadow-md rounded-xl bg-gradient-to-r from-gray-50  to-purple-50">
    <form class="list-disc space-y-2 m-8 flex flex-col  ">
              <div class="flex items-center">
                <span class="h-6 flex sm:h-7">
                  <svg class="flex-shrink-0 h-5 w-5 text-red-500" viewBox="0 0 20 20" fill="currentColor">
                    <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd" />
                  </svg>
                </span>
                   <input class="ml-2 rounded-lg border-2 border-gray-500 hover:border-cyan-500 focus:border-cyan-500 w-full" type="text" placeholder="Úkol" name="" id="name">
              </div>
              <div class="flex items-center">
                <span class="h-6 flex items-center sm:h-7">
                  <svg class="flex-shrink-0 h-5 w-5 text-cyan-500" viewBox="0 0 20 20" fill="currentColor">
                    <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd" />
                  </svg>
                </span>
                   <input class="ml-2 rounded-lg border-2 border-gray-500 hover:border-cyan-500 focus:border-cyan-500" type="datetime-local" name="" id="">
              </div>
              <div class="flex items-center">
                <span class="h-6 flex items-center sm:h-7">
                  <svg class="flex-shrink-0 h-5 w-5 text-cyan-500" viewBox="0 0 20 20" fill="currentColor">
                    <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd" />
                  </svg>
                </span>
                   <input class="ml-2 rounded-lg border-2 border-gray-500 hover:border-cyan-500 focus:border-cyan-500" type="datetime-local" name="" id="">
              </div>
               <div class="flex items-center">
                <span class="h-6 flex items-center sm:h-7">
                  <svg class="flex-shrink-0 h-5 w-5 text-cyan-500" viewBox="0 0 20 20" fill="currentColor">
                    <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd" />
                  </svg>
                </span>
                   <select class="ml-2 rounded-lg border-2 border-gray-500 hover:border-cyan-500 focus:border-cyan-500">
                      <option value="coder">Kódování</option>
                      <option value="itak">Programování</option>
                      <option value="meeting">Meetingy</option>
                    </select>
              </div>
             <div class="inline-block mt-2 self-end">
                    <button type="button" class="text-lg py-2.5 px-10 rounded-lg border-2 border-gray-500 hover:border-cyan-500 hover:bg-cyan-500 hover:text-gray-50  ">Dodat</button>
                </div>
            </form>
  </div>
  <div class="shceduel max-w-full ml-5 p-4 shadow-md rounded-xl bg-gradient-to-r from-gray-50  to-purple-50">
  <table class="table-auto">
    <thead>
      <tr>
        <th class="cursor-pointer p-2">Název Úkolu</th>
        <th class="cursor-pointer p-2">Datum a Čas Od</th>
        <th class="cursor-pointer p-2">Datum a Čas Do</th>
        <th class="cursor-pointer p-2">Druh Práce</th>
      </tr>
    </thead>
    <tbody>
      <tr class="hover:bg-gray-200">
        <td class="text-left p-2">HTML&CSS website</td>
        <td class="text-right p-2">27/02/2021 11:30</td>
        <td class="text-right p-2">28/02/2021 17:30</td>
        <td class="text-right p-2">Koder</td>
        <span class="h-6 flex items-center sm:h-7 pt-2.5 cursor-pointer">
          <svg class="flex-shrink-0 h-6 w-5 text-red-200 hover:text-red-500" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 7l-.867 12.142A2 2 0 0116.138 21H7.862a2 2 0 01-1.995-1.858L5 7m5 4v6m4-6v6m1-10V4a1 1 0 00-1-1h-4a1 1 0 00-1 1v3M4 7h16"/>
          </svg>
        </span>
      </tr>
      <tr class="hover:bg-gray-200">
        <td class="text-left p-2">Vue JS 3</td>
        <td class="text-right p-2">27/02/2021 14:30</td>
        <td class="text-right p-2">28/02/2021 20:30</td>
        <td class="text-right p-2">FrontEnd</td>
        <span class="h-6 flex items-center sm:h-7 pt-2.5 cursor-pointer">
          <svg class="flex-shrink-0 h-6 w-5 text-red-200 hover:text-red-500" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 7l-.867 12.142A2 2 0 0116.138 21H7.862a2 2 0 01-1.995-1.858L5 7m5 4v6m4-6v6m1-10V4a1 1 0 00-1-1h-4a1 1 0 00-1 1v3M4 7h16"/>
          </svg>
        </span>
      </tr>
    </tbody>
</table>
  </div>
</main>

</template>

<script>

export default {
  name: 'App'
}
</script>

<style>
  body {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    background-image: linear-gradient(to top, #537895 0%, #09203f 100%);
  }
</style>
