<script setup>
import TableRow from "./TableRow.vue";
import { onMounted, ref } from "vue";
import axios from "axios";

const employees = ref([]);

onMounted(async () => {
    await axios
        .get("https://cycling-api.cvoapis.com/magento/dc_team")
        .then((response) => {
            employees.value = response.data;
        });
});
</script>

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
                <TableRow
                    v-for="employee in employees"
                    :first_name="employee.first_name"
                    :last_name="employee.last_name"
                    :login_id="employee.login_id"
                    :email="employee.email"
                    :team="employee.team"
                />
            </tbody>
        </table>
    </div>
</template>
