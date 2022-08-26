<script setup></script>

<template>
    <div class="container mx-auto overflow-auto rounded-xl">
        <table
            class="w-full bg-slate-700 text-md text-left text-gray-500 dark:text-gray-400"
        >
            <thead
                class="text-xs uppercase bg-clip-text text-transparent bg-gradient-to-r from-pink-500 to-violet-500"
            >
                <tr>
                    <th class="py-3 px-6" scope="col">First name</th>
                    <th class="py-3 px-6" scope="col">Last name</th>
                    <th class="py-3 px-6" scope="col">Login ID</th>
                    <th class="py-3 px-6" scope="col">Email address</th>
                    <th class="py-3 px-6" scope="col">Team</th>
                </tr>
            </thead>
            <tbody>
                <tr
                    class="bg-slate-200 border-b dark:bg-slate-800 border-slate-700"
                >
                    <td class="py-4 px-6">Joe</td>
                    <td class="py-4 px-6">Mancini</td>
                    <td class="py-4 px-6">jmancini</td>
                    <td
                        class="py-4 px-6 bg-clip-text text-transparent bg-gradient-to-r from-pink-500 to-violet-500"
                    >
                        jmancini@cvoptical.com
                    </td>
                    <td class="py-4 px-6">IT</td>
                </tr>
            </tbody>
        </table>
    </div>
</template>
