<template>
    <table :class="css.transactionHistoryTable">
        <thead>
            <tr>
                <th>Type</th>
                <th>Amount</th>
                <th>Currency</th>
            </tr>
        </thead>

        <tbody>
            <tr v-for="transaction in transactions" :key="transaction.id">
                <td>{{capitalizeFirstLetter(transaction.type)}}</td>
                <td>{{transaction.amount}}</td>
                <td>{{transaction.currency}}</td>
            </tr>
        </tbody>
    </table>
</template>
<script setup>
import {defineProps} from "vue"
import css from "./TransactionHistory.module.css"
const props = defineProps({
    transactions: Array,
})
const capitalizeFirstLetter = (string) => {
        return string.charAt(0).toUpperCase() + string.slice(1);
    };
</script>