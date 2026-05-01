<template>
    <div class="app">
        <h2 class="title">路由测试</h2>
        <div class="navigate">
            <RouterLink to="/home" active-class="active">首页</RouterLink>
            <RouterLink to="/news" active-class="active">新闻</RouterLink>
            <RouterLink to="/about" active-class="active">关于</RouterLink>
        </div>
        <div class="main-content">
            <router-view></router-view>
        </div>
    </div>
</template>

<script lang="ts" setup name="App">
import { ref } from 'vue';
import { RouterView, RouterLink } from 'vue-router';

const activeBtn = ref('home');
</script>

<style>
    * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
    }

    html,
    body {
        width: 100%;
        min-height: 100vh;
        font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        overflow-x: hidden;
    }

    .app {
        min-height: 100vh;
        width: 100%;
        min-width: 320px;
        background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
        background-size: cover;
        background-position: center;
        padding: 2vw;
    }

    .title {
        text-align: center;
        color: black;
        margin-bottom: 4vh;
        font-size: clamp(1.5rem, 5vw, 2rem);
        font-weight: 600;
        padding: 20px 40px;
        border: 1px solid #999999;
        border-radius: 12px;
        background: linear-gradient(135deg, #666666 0%, #ffffff 100%);
        max-width: 400px;
        margin-left: auto;
        margin-right: auto;
        box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
    }

    .navigate {
        background: transparent;
        padding: 15px 2%;
        margin: 0 auto 4vh;
        max-width: 800px;
        min-width: 300px;
        width: 95%;
        display: flex;
        justify-content: space-around;
        align-items: center;
        gap: 2%;
    }

    .navigate a {
        text-decoration: none;
        color: white;
        padding: 12px 15px;
        border-radius: 8px;
        font-weight: 500;
        transition: transform 0.3s ease, box-shadow 0.3s ease, background 0.3s ease, color 0.3s ease;
        background: #666666;
        border: 2px solid #555555;
        text-align: center;
        flex: 0 0 calc(28% - 10px);
        min-width: 60px;
        font-size: clamp(0.875rem, 2.5vw, 1rem);
        cursor: pointer;
    }

    .navigate a:hover {
        background: #888888;
        color: white;
        transform: translateY(-2px);
        box-shadow: 0 4px 12px rgba(0, 0, 0, 0.2);
    }

    .navigate a.active {
        background: #2d5a2d;
        border-color: #1a3d1a;
        box-shadow: 0 4px 12px rgba(45, 90, 45, 0.4);
        color: #ffd700;
    }

    .navigate a.active:hover {
        background: #3d7a3d;
        color: #ffd700;
    }

    .navigate a:active {
        transform: translateY(0);
    }

    .main-content {
        background: white;
        padding: 4vh 4%;
        max-width: 800px;
        min-width: 300px;
        width: 95%;
        margin: 0 auto;
        box-shadow: 0 8px 32px rgba(0, 0, 0, 0.1);
        min-height: 200px;
        text-align: center;
        color: #666;
        font-size: clamp(0.875rem, 2.5vw, 1rem);
    }

    @media (max-width: 480px) {
        .navigate {
            padding: 10px 2%;
        }

        .navigate a {
            padding: 10px 8px;
            flex: 0 0 calc(30% - 8px);
        }

        .main-content {
            padding: 20px 5%;
        }

        .title {
            padding: 15px 20px;
        }
    }
</style>