<template>
<div class="container">
    <global-header :user='currentUser'></global-header>
    <column-list :list="list"></column-list>
</div>
</template>

<script lang="ts">
import {
    defineComponent,
    reactive
} from "vue";
import "bootstrap/dist/css/bootstrap.min.css";
import ColumnList, {
    ColumnProps
} from "./components/ColumnList.vue";
import GlobalHeader, {
    UserProps
} from "./components/GlobalHeader.vue";

const testData: ColumnProps[] = [{
        id: 1,
        title: "test1的专栏",
        description: "这是一个test1的专栏",
        // avatar: "xxx.jpg",
    },
    {
        id: 2,
        title: "test2的专栏",
        description: "这是一个test2的专栏",
        // avatar: "xxx.jpg",
    },
    {
        id: 3,
        title: "test2的专栏",
        description: "这是一个test2的专栏",
        // avatar: "xxx.jpg",
    },
    {
        id: 4,
        title: "test2的专栏",
        description: "这是一个test2的专栏",
        // avatar: "xxx.jpg",
    },
];
const currentUser: UserProps = {
    isLogin: false,
}
export default defineComponent({
    name: "App",
    components: {
        ColumnList,
        GlobalHeader,
    },
    setup() {
        return {
            list: testData,
            currentUser
        };
    },
});
</script>

<style>
</style>
