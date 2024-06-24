<template>
    <div :class="css.friendListItemContainer">
        <img :src="props.img" alt="Avatar" width="48" />
        <p>{{props.name}}</p>
        <p :class="computedClasses">{{props.status ? 'Online' : 'Offline'}}</p>
    </div>
</template>
<script setup>
import {defineProps, computed} from "vue"
import css from "./FriendListItem.module.css"
import clsx from "clsx"
const props = defineProps({
    name: String,
    status: Boolean,
    img: String,
})
const computedClasses = computed(()=>{
    return clsx(css.friendListItemStatus,{
        [css.online]: props.status,
        [css.offline]: !props.status,
    })
})
</script>