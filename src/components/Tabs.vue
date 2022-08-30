<script setup>
import { TabGroup, TabList, Tab, TabPanels, TabPanel } from "@headlessui/vue";
import Form from "./Form.vue";
import Table from "./Table.vue";

const tabs = ["Form", "Table"];
</script>

<template>
    <TabGroup>
        <div
            class="container mx-auto py-10 px-32 sm:px-44 md:px-60 lg:px-80 xl:px-96 2xl:px-96"
        >
            <TabList
                class="flex space-x-1 rounded-xl bg-slate-500 dark:bg-slate-400 p-1"
            >
                <Tab
                    v-for="tab in tabs"
                    as="template"
                    :key="tab"
                    v-slot="{ selected }"
                >
                    <button
                        :class="[
                            'w-full rounded-lg py-2.5 text-lg font-medium leading-5 text-slate-800 dark:text-slate-400',
                            'ring-white ring-opacity-60 ring-offset-2 ring-offset-slate-500 dark:ring-offset-slate-400 focus:outline-none focus:ring-2',
                            selected
                                ? 'bg-slate-200 dark:bg-slate-800 shadow'
                                : 'text-slate-200 dark:text-slate-800 hover:bg-white/[0.12] dark:hover:bg-slate-800/[0.12]',
                        ]"
                    >
                        {{ tab }}
                    </button>
                </Tab>
            </TabList>
        </div>

        <TabPanels class="my-10">
            <TabPanel>
                <Form />
            </TabPanel>
            <TabPanel>
                <Table />
            </TabPanel>
        </TabPanels>
    </TabGroup>
</template>
