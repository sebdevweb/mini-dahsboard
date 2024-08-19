<script setup>
import { ref } from 'vue'
import AccountBadge from 'vue-material-design-icons/AccountBadge.vue';
import Cog from 'vue-material-design-icons/Cog.vue';
components: {
    AccountBadge,
    Cog
}
</script>

<template>
    <header>
        <div class="logo"><span>my</span>Dashboard<span>!</span></div>
        <nav class="account">
            <ul>
                <li><cog /></li>
                <li><account-badge /></li>
            </ul>
        </nav>
    </header>
</template>

<style lang="scss">
header {
    max-width: 100%;
    background: #252b38;
    padding: 12px;
    border-bottom: 1px solid #66686c;
    display: flex;
    justify-content: space-between;
    align-items: center;
    .logo {
        font-size: 24px;
        color: white;
        span {
            color: #b370ff;
            font-size: 32px;
            font-weight: bold;
            &:nth-child(2) {
                color: yellowgreen;
                font-weight: normal;
            }
        }
    }
    .account {
        li {
            svg {
                transition: 0.3s ease-in;
                &:hover {
                    cursor: pointer;
                    color: #b370ff;
                    transition: 0.3s ease-out;
                }
            }
        }
    }
}
</style>
