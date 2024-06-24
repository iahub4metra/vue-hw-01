<template>
    <div :class="css.profileContainer">
        <div :class="css.profileContainerImage">
            <img
                :src="userData.avatar"
                :alt="`${userData.username}'s avatar`"
                :class="css.profileImage"
            />
            <p :class="css.profileTitle">{{userData.username}}</p>
            <p :class="css.profileText">@{{userData.tag}}</p>
            <p :class="css.profileText">{{userData.location}}</p>
        </div>
        <ul :class="css.profileList">
            <li :class="css.profileListItem">
                <span>Followers</span>
                <span>{{userData.stats.followers}}</span>
            </li>
            <li :class="css.profileListItem">
                <span>Views</span>
                <span>{{userData.stats.views}}</span>
            </li>
            <li :class="css.profileListItem">
                <span>Likes</span>
                <span>{{userData.stats.likes}}</span>
            </li>
        </ul>
    </div>
</template>
<script setup>
import { defineProps } from 'vue'
import css from "./Profile.module.css"
const props = defineProps({
    userData: Object,
})
</script>