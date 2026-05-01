<template>
    <div class="home-container">
        <h2>欢迎来到首页界面</h2>
        <div class="content-card">
            <div class="card-icon">🏠</div>
            <p>这是我们的首页，您可以在这里浏览最新内容</p>
        </div>
        <div class="feature-grid">
            <div class="feature-item">
                <span class="feature-icon">📋</span>
                <h3>最新资讯</h3>
                <p>获取最新的新闻和公告</p>
            </div>
            <div class="feature-item">
                <span class="feature-icon">📊</span>
                <h3>数据概览</h3>
                <p>查看关键数据和统计信息</p>
            </div>
            <div class="feature-item">
                <span class="feature-icon">🎯</span>
                <h3>快速导航</h3>
                <p>一键跳转到您需要的页面</p>
            </div>
        </div>
    </div>
</template>

<script lang="ts" setup name="Home">
</script>

<style scoped>
.home-container {
    padding: 2rem;
    max-width: 1200px;
    margin: 0 auto;
}

.home-container h2 {
    text-align: center;
    color: #1a202c;
    font-size: 2rem;
    margin-bottom: 2rem;
    font-weight: 700;
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
}

.content-card {
    background: linear-gradient(135deg, #f6f8fb 0%, #e9ecef 100%);
    border-radius: 16px;
    padding: 2rem;
    text-align: center;
    margin-bottom: 2rem;
    box-shadow: 0 4px 20px rgba(0, 0, 0, 0.08);
    transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.content-card:hover {
    transform: translateY(-4px);
    box-shadow: 0 8px 30px rgba(0, 0, 0, 0.12);
}

.card-icon {
    font-size: 4rem;
    margin-bottom: 1rem;
}

.content-card p {
    color: #4a5568;
    font-size: 1.1rem;
    line-height: 1.6;
}

.feature-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 1.5rem;
}

.feature-item {
    background: white;
    border-radius: 12px;
    padding: 1.5rem;
    text-align: center;
    box-shadow: 0 2px 12px rgba(0, 0, 0, 0.06);
    transition: all 0.3s ease;
    border: 1px solid #e2e8f0;
}

.feature-item:hover {
    transform: translateY(-4px);
    box-shadow: 0 8px 24px rgba(102, 126, 234, 0.15);
    border-color: #667eea;
}

.feature-icon {
    font-size: 2.5rem;
    display: block;
    margin-bottom: 1rem;
}

.feature-item h3 {
    color: #2d3748;
    font-size: 1.25rem;
    margin-bottom: 0.5rem;
}

.feature-item p {
    color: #718096;
    font-size: 0.95rem;
    line-height: 1.5;
}

@media (max-width: 768px) {
    .home-container {
        padding: 1rem;
    }
    
    .home-container h2 {
        font-size: 1.5rem;
    }
    
    .feature-grid {
        grid-template-columns: 1fr;
    }
}
</style>
