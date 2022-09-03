<script setup>
import { ref } from "vue";
import axios from "axios";

let first_name = ref("");
let last_name = ref("");
let login_id = ref("");
let email = ref("");
let team = ref("");

let submit = () => {
    axios
        .post("https://cycling-api.cvoapis.com/magento/dc_team", {
            first_name: first_name.value,
            last_name: last_name.value,
            login_id: login_id.value,
            email: email.value,
            team: team.value,
        })
        .then((response) => console.log(response));

    first_name.value = "";
    last_name.value = "";
    login_id.value = "";
    email.value = "";
    team.value = "";
};
</script>

<template>
    <div class="container mx-auto px-20 md:px-44 lg:px-60 xl:px-80 2xl:px-80">
        <form @submit.prevent="submit">
            <!-- First name -->
            <div class="relative z-0 mb-6 w-full group">
                <input
                    type="text"
                    name="first_name"
                    id="first_name"
                    v-model="first_name"
                    class="block py-2.5 px-0 w-full text-lg bg-clip-text text-black/[0.2] dark:text-white/[0.2] bg-gradient-to-r from-pink-500 to-violet-500 border-0 border-b-2 border-slate-400 appearance-none dark:border-slate-400 focus:outline-none focus:ring-0 focus:border-pink-400 peer"
                    placeholder=" "
                    required
                />
                <label
                    for="first_name"
                    class="peer-focus:font-medium absolute text-md text-slate-800 dark:text-slate-400 duration-300 transform -translate-y-6 scale-75 top-3 -z-10 origin-[0] peer-focus:left-0 peer-placeholder-shown:scale-100 peer-placeholder-shown:translate-y-0 peer-focus:scale-75 peer-focus:-translate-y-6"
                    >First name</label
                >
            </div>
            <!-- Last name -->
            <div class="relative z-0 mb-6 w-full group">
                <input
                    type="text"
                    name="last_name"
                    id="last_name"
                    v-model="last_name"
                    class="block py-2.5 px-0 w-full text-lg bg-clip-text text-black/[0.2] dark:text-white/[0.2] bg-gradient-to-r from-pink-500 to-violet-500 border-0 border-b-2 border-slate-400 appearance-none dark:border-slate-400 focus:outline-none focus:ring-0 focus:border-pink-400 peer"
                    placeholder=" "
                    required
                />
                <label
                    for="last_name"
                    class="peer-focus:font-medium absolute text-md text-slate-800 dark:text-slate-400 duration-300 transform -translate-y-6 scale-75 top-3 -z-10 origin-[0] peer-focus:left-0 peer-placeholder-shown:scale-100 peer-placeholder-shown:translate-y-0 peer-focus:scale-75 peer-focus:-translate-y-6"
                    >Last name</label
                >
            </div>
            <!-- Login ID -->
            <div class="relative z-0 mb-6 w-full group">
                <input
                    type="text"
                    name="login_id"
                    id="login_id"
                    v-model="login_id"
                    class="block py-2.5 px-0 w-full text-lg bg-clip-text text-black/[0.2] dark:text-white/[0.2] bg-gradient-to-r from-pink-500 to-violet-500 border-0 border-b-2 border-slate-400 appearance-none dark:border-slate-400 focus:outline-none focus:ring-0 focus:border-pink-400 peer"
                    placeholder=" "
                    required
                />
                <label
                    for="login_id"
                    class="peer-focus:font-medium absolute text-md text-slate-800 dark:text-slate-400 duration-300 transform -translate-y-6 scale-75 top-3 -z-10 origin-[0] peer-focus:left-0 peer-placeholder-shown:scale-100 peer-placeholder-shown:translate-y-0 peer-focus:scale-75 peer-focus:-translate-y-6"
                    >Login ID</label
                >
            </div>
            <!-- Email address -->
            <div class="relative z-0 mb-6 w-full group">
                <input
                    type="email"
                    name="email"
                    id="email"
                    v-model="email"
                    pattern="[A-Za-z0-9._+-]+@[A-Za-z0-9 -]+\.[a-z]{2,}"
                    class="block py-2.5 px-0 w-full text-lg bg-clip-text text-black/[0.2] dark:text-white/[0.2] bg-gradient-to-r from-pink-500 to-violet-500 border-0 border-b-2 border-slate-400 appearance-none dark:border-slate-400 focus:outline-none focus:ring-0 focus:border-pink-400 peer"
                    placeholder=" "
                    required
                />
                <label
                    for="email"
                    class="peer-focus:font-medium absolute text-md text-slate-800 dark:text-slate-400 duration-300 transform -translate-y-6 scale-75 top-3 -z-10 origin-[0] peer-focus:left-0 peer-placeholder-shown:scale-100 peer-placeholder-shown:translate-y-0 peer-focus:scale-75 peer-focus:-translate-y-6"
                    >Email address</label
                >
            </div>
            <!-- Team selector -->
            <label for="team" class="sr-only"></label>
            <select
                id="team"
                v-model="team"
                class="block py-2.5 px-0 w-full text-lg bg-clip-text text-black/[0.2] dark:text-white/[0.2] bg-gradient-to-r from-pink-500 to-violet-500 border-0 border-b-2 border-slate-400 appearance-none dark:border-slate-400 focus:outline-none focus:ring-0 focus:border-pink-400 peer"
                required
            >
                <option selected disabled value="">Choose a team...</option>
                <option class="text-black" value="Order staging">
                    Order staging
                </option>
                <option class="text-black" value="Picking">Picking</option>
                <option class="text-black" value="Receiving">Receiving</option>
                <option class="text-black" value="Refurb">Refurb</option>
                <option class="text-black" value="Shipping">Shipping</option>
            </select>
            <!-- Submit button -->
            <div class="mt-6">
                <button
                    type="submit"
                    class="text-white transition-all duration-500 bg-gradient-to-r to-violet-500 via-pink-500 from-blue-500 bg-size-200 hover:bg-right focus:ring-4 focus:outline-none focus:ring-slate-400 font-bold rounded-lg text-md w-full sm:w-auto px-5 py-2.5 text-center"
                >
                    Submit
                </button>
            </div>
        </form>
    </div>
</template>
