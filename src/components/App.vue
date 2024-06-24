<template>
  <div>
    <Profile :userData="userData"/>
    <FriendList :friends="friends"/>
    <TransactionHistory :transactions="transactions"/>
  </div>
</template>
<script setup>
import Profile from "./profile/Profile.vue"
import FriendList from "./friendList/FriendList.vue"
import userData from "../assets/userData.json"
import friends from "../assets/friends.json"
import TransactionHistory from "./transactionHistory/TransactionHistory.vue"
import transactions from "../assets/transactions.json"
</script>