<template>
<main class="h-screencontainer mx-auto p-8 flex">
  <div class="form max-h-315 max-w-full shadow-md rounded-xl bg-gradient-to-r from-gray-50  to-purple-50">
    <form
      @submit.prevent="submitHandler"
      class="list-disc space-y-2 m-8 flex flex-col">
              <div class="flex items-end">
                <span class="h-6 flex sm:h-7">
                  <svg
                    :class="{'text-cyan-500':name }"
                    class="flex-shrink-0 h-5 w-5 text-red-500"
                    viewBox="0 0 20 20"
                    fill="currentColor">
                    <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd" />
                  </svg>
                </span>
                <div class="flex flex-col">
                  <label class="ml-2" for="name">Název Úkolu:</label>
                   <input
                    v-model.trim="name"
                    class="ml-2 rounded-lg border-2 border-gray-500 hover:border-cyan-500 focus:border-cyan-500 w-full" type="text" placeholder="Úkol" id="name">
                </div>
              </div>
              <div class="flex items-end">
                <span class="h-6 flex items-center sm:h-7">
                  <svg
                    :class="{'text-cyan-500':timestart }"
                    class="flex-shrink-0 h-5 w-5 text-red-500"
                    viewBox="0 0 20 20"
                    fill="currentColor">
                    <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd" />
                  </svg>
                </span>
                <div class="flex flex-col">
                  <label class="ml-2" for="timefrom">Datum a Čas Od:</label>
                   <input
                    v-model="timestart"
                    class="ml-2 rounded-lg border-2 border-gray-500 hover:border-cyan-500 focus:border-cyan-500"
                    type="datetime-local"
                    id="timefrom">
                </div>
              </div>
              <div class="flex items-end">
                <span class="h-6 flex items-center sm:h-7">
                  <svg
                    :class="{'text-cyan-500':timeend }"
                    class="flex-shrink-0 h-5 w-5 text-red-500"
                    viewBox="0 0 20 20"
                    fill="currentColor">
                    <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd" />
                  </svg>
                </span>
                <div class="flex flex-col">
                  <label class="ml-2" for="timeend">Datum a Čas Do:</label>
                   <input
                    v-model="timeend"
                    class="ml-2 rounded-lg border-2 border-gray-500 hover:border-cyan-500 focus:border-cyan-500"
                    type="datetime-local"
                    id="timeend">
                </div>
              </div>
               <div class="flex items-end">
                <span class="h-6 flex items-center sm:h-7">
                  <svg
                    :class="{'text-cyan-500':work }"
                    class="flex-shrink-0 h-5 w-5 text-red-500"
                    viewBox="0 0 20 20"
                    fill="currentColor">
                    <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd" />
                  </svg>
                </span>
                <div class="flex flex-col">
                  <label class="ml-2" for="typeofwork">Druh Práce:</label>
                   <select
                    v-model="work"
                    id="typeofwork"
                    class="ml-2 rounded-lg border-2 border-gray-500 hover:border-cyan-500 focus:border-cyan-500">
                      <option value="coder">Kódování</option>
                      <option value="dev">Programování</option>
                      <option value="meeting">Meetingy</option>
                    </select>
                </div>
              </div>
              <div class="inline-block mt-2 self-end">
                <button
                  type="submit"
                  class="text-lg py-2.5 px-10 rounded-lg border-2 border-gray-500  hover:border-cyan-500 hover:bg-cyan-500 hover:text-gray-50">Dodat</button>
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
      <tr
        v-for="(item, index) in arr" :key="index"
        class="hover:bg-gray-200">
        <td
          v-for="(elem, index) in item" :key="index"
          class="text-center p-2">{{ elem }}</td>
        <span class="h-6 flex items-center sm:h-7 pt-2.5 cursor-pointer">
          <svg class="flex-shrink-0 h-6 w-5 text-red-200 hover:text-red-500" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 7l-.867 12.142A2 2 0 0116.138 21H7.862a2 2 0 01-1.995-1.858L5 7m5 4v6m4-6v6m1-10V4a1 1 0 00-1-1h-4a1 1 0 00-1 1v3M4 7h16"/>
          </svg>
        </span>
      </tr>
      <!-- <tr class="hover:bg-gray-200">
        <td class="text-center p-2">Vue JS 3</td>
        <td class="text-right p-2">27/02/2021 14:30</td>
        <td class="text-right p-2">28/02/2021 20:30</td>
        <td class="text-right p-2">FrontEnd</td>
        <span class="h-6 flex items-center sm:h-7 pt-2.5 cursor-pointer">
          <svg class="flex-shrink-0 h-6 w-5 text-red-200 hover:text-red-500" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 7l-.867 12.142A2 2 0 0116.138 21H7.862a2 2 0 01-1.995-1.858L5 7m5 4v6m4-6v6m1-10V4a1 1 0 00-1-1h-4a1 1 0 00-1 1v3M4 7h16"/>
          </svg>
        </span>
      </tr> -->
    </tbody>
</table>
  </div>
</main>

</template>

<script>

export default {
  data () {
    return {
      name: '',
      timestart: '',
      timeend: '',
      work: '',
      arr: []
    }
  },
  methods: {
    submitHandler (event) {
      this.arr.push({ name: this.name, timestart: this.timestart, timeend: this.timeend, work: this.work })
      this.name = ''
      this.timestart = ''
      this.timeend = ''
      this.work = ''
      event.target.reset()
    }
  }
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
