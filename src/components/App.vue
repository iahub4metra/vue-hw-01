<template>
  <div>
    <Profile :userData="userData"/>
    <FriendList :friends="friends"/>
  </div>
</template>
<script setup>
import Profile from "./profile/Profile.vue"
import FriendList from "./friendList/FriendList.vue"
import userData from "../assets/userData.json"
import friends from "../assets/friends.json"
</script>