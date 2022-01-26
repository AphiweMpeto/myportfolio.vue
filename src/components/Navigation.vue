<template>
    <header :class="{'scrolled-nav':scrollPosition}">
        <nav>
            <div class="brand">
                <img src="@assets/logo.png" alt="">
            </div>
            <ul v-show="!mobile" class="navigation">
                <li>
                    <router-link class="link" :to="{name:'Home'}"></router-link>
                    <router-link class="link" :to="{name:'About'}">About</router-link>
                    <router-link class="link" :to="{name:'Portfolio'}">Portfolio</router-link>
                    <router-link class="link" :to="{name:'Contact'}">Contact</router-link>
                </li>
            </ul>
            <div class="icon">
            <i @click="toggleMobileNav" v-show="mobile" class="far fa bars" :class="{'icon-active' : mobileNav}"></i>
            </div>
            <transition name="mobile-nav">
            <ul v-show="mobileNav" class="dropdown-nav">
                <li>
                    <router-link class="link" :to="{name:'Home'}"></router-link>
                    <router-link class="link" :to="{name:'About'}">About</router-link>
                    <router-link class="link" :to="{name:'Portfolio'}">Portfolio</router-link>
                    <router-link class="link" :to="{name:'Contact'}">Contact</router-link>
                </li>
            </ul>    
            </transition>
        </nav>
    </header>
</template>

<script>
import Header from '../views/Header.vue'
export default {
    name:'navigation',
    data() {
        return {
            scrollPosition: null,
            mobile: true,
            mobileNav: null,
            windowWidth: null,            
        };
    },
    components: { Header },

}
</script>

<style lang="scss" scoped>
header {
    background-color: rgba(0, 0, 0, 0.8);
    z-index: 99;
    width: 100%;
    position: fixed;
    transition: 0.5s ease all;
    color: #ffff

    nav {
        display: flex;
        flex-direction: row;
        padding: 12px 0;
        transition: 0.5 ease all; 
        width:90%;
        margin: 0 auto;
    }
        @media (min-width: 1140px) {
            max-width: 1140px;
        }

        ul,
        .link {
            font-weight: 500;
            color: #ffff;
            list-style: none;
            text-decoration: none;
        }

        li {
            text-transform: uppercase;
            padding:16px;
            margin-left: 16px;
        }
        
        .link {
            font-size: 14px;
            transition: 0.5 ease all;
            padding-bottom: 4px;
            border-bottom: 1px solid transparent;

            &:hover {
                color: #00afea;
                border-color: #00afea;
                
            }
        }
        .brand{
            display:flex;
            align-items: center;

            img {
                width: 50px;
                transition: 0.5s ease all;
            }

        }
    

}

</style>