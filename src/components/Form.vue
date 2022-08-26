<script setup></script>

<template>
    <div class="container mx-auto px-20 md:px-44 lg:px-60 xl:px-80 2xl:px-80">
        <form>
            <!--text-slate-800 dark:text-slate-400-->
            <!-- bg-clip-text text-transparent bg-gradient-to-r from-pink-500 to-violet-500 -->
            <div class="relative z-0 mb-6 w-full group">
                <input
                    type="text"
                    name="floating_first_name"
                    id="floating_first_name"
                    class="block py-2.5 px-0 w-full text-lg bg-clip-text text-black/[0.2] dark:text-white/[0.2] bg-gradient-to-r from-pink-500 to-violet-500 border-0 border-b-2 border-slate-400 appearance-none dark:border-slate-400 focus:outline-none focus:ring-0 focus:border-pink-400 peer"
                    placeholder=" "
                    required
                />
                <label
                    for="floating_first_name"
                    class="peer-focus:font-medium absolute text-md text-slate-800 dark:text-slate-400 duration-300 transform -translate-y-6 scale-75 top-3 -z-10 origin-[0] peer-focus:left-0 peer-placeholder-shown:scale-100 peer-placeholder-shown:translate-y-0 peer-focus:scale-75 peer-focus:-translate-y-6"
                    >First name</label
                >
            </div>
            <div class="relative z-0 mb-6 w-full group">
                <input
                    type="text"
                    name="floating_last_name"
                    id="floating_last_name"
                    class="block py-2.5 px-0 w-full text-lg bg-clip-text text-black/[0.2] dark:text-white/[0.2] bg-gradient-to-r from-pink-500 to-violet-500 border-0 border-b-2 border-slate-400 appearance-none dark:border-slate-400 focus:outline-none focus:ring-0 focus:border-pink-400 peer"
                    placeholder=" "
                    required
                />
                <label
                    for="floating_last_name"
                    class="peer-focus:font-medium absolute text-md text-slate-800 dark:text-slate-400 duration-300 transform -translate-y-6 scale-75 top-3 -z-10 origin-[0] peer-focus:left-0 peer-placeholder-shown:scale-100 peer-placeholder-shown:translate-y-0 peer-focus:scale-75 peer-focus:-translate-y-6"
                    >Last name</label
                >
            </div>
            <div class="relative z-0 mb-6 w-full group">
                <input
                    type="text"
                    name="floating_login_id"
                    id="floating_login_id"
                    class="block py-2.5 px-0 w-full text-lg bg-clip-text text-black/[0.2] dark:text-white/[0.2] bg-gradient-to-r from-pink-500 to-violet-500 border-0 border-b-2 border-slate-400 appearance-none dark:border-slate-400 focus:outline-none focus:ring-0 focus:border-pink-400 peer"
                    placeholder=" "
                    required
                />
                <label
                    for="floating_login_id"
                    class="peer-focus:font-medium absolute text-md text-slate-800 dark:text-slate-400 duration-300 transform -translate-y-6 scale-75 top-3 -z-10 origin-[0] peer-focus:left-0 peer-placeholder-shown:scale-100 peer-placeholder-shown:translate-y-0 peer-focus:scale-75 peer-focus:-translate-y-6"
                    >Login ID</label
                >
            </div>
            <div class="relative z-0 mb-6 w-full group">
                <input
                    type="email"
                    name="floating_email"
                    id="floating_email"
                    class="block py-2.5 px-0 w-full text-lg bg-clip-text text-black/[0.2] dark:text-white/[0.2] bg-gradient-to-r from-pink-500 to-violet-500 border-0 border-b-2 border-slate-400 appearance-none dark:border-slate-400 focus:outline-none focus:ring-0 focus:border-pink-400 peer"
                    placeholder=" "
                    required
                />
                <label
                    for="floating_email"
                    class="peer-focus:font-medium absolute text-md text-slate-800 dark:text-slate-400 duration-300 transform -translate-y-6 scale-75 top-3 -z-10 origin-[0] peer-focus:left-0 peer-placeholder-shown:scale-100 peer-placeholder-shown:translate-y-0 peer-focus:scale-75 peer-focus:-translate-y-6"
                    >Email address</label
                >
            </div>
            <label for="underline_select" class="sr-only"
                >Underline select</label
            >
            <select
                id="underline_select"
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
            <div class="mt-6">
                <button
                    type="submit"
                    class="text-white bg-gradient-to-r from-blue-500 to-violet-500 hover:from-pink-500 hover:to-violet-500 focus:ring-4 focus:outline-none focus:ring-slate-400 font-bold rounded-lg text-md w-full sm:w-auto px-5 py-2.5 text-center"
                >
                    Submit
                </button>
            </div>
        </form>
    </div>
</template>
