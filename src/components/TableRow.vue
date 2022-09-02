<script setup>
defineProps({
    first_name: String,
    last_name: String,
    login_id: String,
    email: String,
    team: String,
});
</script>

<template>
    <tr class="bg-slate-200 border-b dark:bg-slate-800 border-slate-700">
        <td class="py-4 px-6">{{ first_name }}</td>
        <td class="py-4 px-6">{{ last_name }}</td>
        <td class="py-4 px-6">{{ login_id }}</td>
        <td
            class="py-4 px-6 bg-clip-text text-transparent bg-gradient-to-r from-pink-500 to-violet-500"
        >
            {{ email }}
        </td>
        <td class="py-4 px-6">{{ team }}</td>
    </tr>
</template>
