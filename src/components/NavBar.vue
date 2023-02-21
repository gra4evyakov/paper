<template>
    <div class="navbar">
        <h1 class="logo">Paper</h1>
        <nav class="nav" :class="{ 'open': isOpen }">
            <ul class="menu">
                <li v-for="item in navList" class="menu__item">{{ item }}</li>
            </ul>
        </nav>
        <div @click="openMenu" class="btn2" :class="{ 'open': isOpen }" data-menu="2">
            <div class="icon"></div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            isOpen: false,
            navList: ['Work', 'About', 'Blog', 'Contact']
        }
    },
    methods: {
        openMenu() {
            this.isOpen = !this.isOpen
        }
    }
}
</script>

<style scoped>
.navbar {
    position: fixed;
    left: 50%;
    transform: translateX(-50%);
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 90%;
    height: 100px;
}
.logo {
    color: #FFFFFF;
}

.menu__item {
    cursor: pointer;
    display: inline-block;
    padding: 0 5px;
    font-size: 22px;
    line-height: 0px;
    color: #FFFFFF;
    transition: .3s;
}

.menu__item:hover {
    transform: scale(1.1);
}

.menu__item+.menu__item {
    margin-left: 25px;
}

.btn2 {
    display: none;
    position: fixed;
    width: 40px;
    height: 40px;
    top: 20px;
    right: 0;
    transition-duration: 0.5s;
}

.btn2 .icon {
    transition-duration: 0.5s;
    position: absolute;
    height: 5px;
    width: 40px;
    top: 30px;
    background-color: #FFFFFF;
}

.btn2 .icon:before {
    transition-duration: 0.5s;
    position: absolute;
    width: 40px;
    height: 5px;
    background-color: #FFFFFF;
    content: "";
    top: -20px;
}

.btn2 .icon:after {
    transition-duration: 0.5s;
    position: absolute;
    width: 40px;
    height: 5px;
    background-color: #FFFFFF;
    content: "";
    top: 20px;
}

.btn2.open .icon {
    transition-duration: 0.5s;
    background: transparent;
}

.btn2.open .icon:before {
    transform: rotateZ(45deg) scaleX(1.25) translate(13px, 13px);
}

.btn2.open .icon:after {
    transform: rotateZ(-45deg) scaleX(1.25) translate(12px, -12px);
}

.btn2:hover {
    cursor: pointer;
}

@media screen and (max-width: 570px) {
    .nav {
        position: fixed;
        top: 0;
        right: -100%;
        height: 100vh;
        width: 50vw;
        display: block;
        background: #ffffffd2;
        transition: .3s;
    }

    .nav.open {
        right: 0;
    }

    .menu {
        position: relative;
        top: 50%;
        transform: translateY(-50%);
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 100px;
    }

    .menu__item+.menu__item {
        margin-left: 0;
    }

    .menu__item {
        display: inline-block;
        padding: 0 5px;
        font-size: 40px;
        line-height: 0px;
        color: #000;
    }

    .btn2 {
        display: block;
    }
}</style>