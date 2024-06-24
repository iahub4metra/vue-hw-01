<template>
    <ul :class="css.friendList">
        <li v-for="friend in friends" :key="friend.id">
            <FriendListItem :name="friend.name" :status="friend.isOnline" :img="friend.avatar"/>
        </li>
    </ul>

</template>
<script setup>
import FriendListItem from "../friendListItem/FriendListItem.vue"
import css from "./FriendList.module.css"
import {defineProps} from "vue"
const props = defineProps({
    friends: Array,
})
</script>