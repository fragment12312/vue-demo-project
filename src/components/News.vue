<template>
    <div class="news-container">
        <h2>欢迎来到新闻界面</h2>
        <div class="news-list">
            <div class="news-item">
                <div class="news-image">📰</div>
                <div class="news-content">
                    <span class="news-tag">热点</span>
                    <h3>最新技术动态发布</h3>
                    <p>了解最新的前端技术发展和行业趋势，保持技术前沿。</p>
                    <div class="news-meta">
                        <span>2024-05-01</span>
                        <span>阅读 1.2k</span>
                    </div>
                </div>
            </div>
            <div class="news-item">
                <div class="news-image">💡</div>
                <div class="news-content">
                    <span class="news-tag">教程</span>
                    <h3>Vue3 最佳实践指南</h3>
                    <p>深入学习Vue3的Composition API，提升开发效率和代码质量。</p>
                    <div class="news-meta">
                        <span>2024-04-30</span>
                        <span>阅读 890</span>
                    </div>
                </div>
            </div>
            <div class="news-item">
                <div class="news-image">🚀</div>
                <div class="news-content">
                    <span class="news-tag">活动</span>
                    <h3>开发者大会即将召开</h3>
                    <p>全球顶级开发者齐聚一堂，分享技术经验和创新成果。</p>
                    <div class="news-meta">
                        <span>2024-04-29</span>
                        <span>阅读 2.1k</span>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script lang="ts" setup name="News">
</script>

<style scoped>
    .news-container {
        padding: 2rem;
        max-width: 1000px;
        margin: 0 auto;
    }

    .news-container h2 {
        text-align: center;
        color: #1a202c;
        font-size: 2rem;
        margin-bottom: 2rem;
        font-weight: 700;
        background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
        background-clip: text;
    }

    .news-list {
        display: flex;
        flex-direction: column;
        gap: 1.5rem;
    }

    .news-item {
        display: flex;
        background: white;
        border-radius: 16px;
        overflow: hidden;
        box-shadow: 0 4px 20px rgba(0, 0, 0, 0.08);
        transition: all 0.3s ease;
        border: 1px solid #e2e8f0;
    }

    .news-item:hover {
        transform: translateX(8px);
        box-shadow: 0 8px 30px rgba(240, 147, 251, 0.15);
        border-color: #f093fb;
    }

    .news-image {
        flex: 0 0 120px;
        display: flex;
        align-items: center;
        justify-content: center;
        font-size: 3rem;
        background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
    }

    .news-content {
        flex: 1;
        padding: 1.5rem;
    }

    .news-tag {
        display: inline-block;
        background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
        color: white;
        padding: 0.25rem 0.75rem;
        border-radius: 20px;
        font-size: 0.75rem;
        font-weight: 600;
        margin-bottom: 0.5rem;
    }

    .news-content h3 {
        color: #2d3748;
        font-size: 1.25rem;
        margin-bottom: 0.5rem;
    }

    .news-content p {
        color: #718096;
        font-size: 0.95rem;
        line-height: 1.6;
        margin-bottom: 0.75rem;
    }

    .news-meta {
        display: flex;
        gap: 1.5rem;
        color: #a0aec0;
        font-size: 0.85rem;
    }

    @media (max-width: 768px) {
        .news-container {
            padding: 1rem;
        }

        .news-container h2 {
            font-size: 1.5rem;
        }

        .news-item {
            flex-direction: column;
        }

        .news-image {
            flex: none;
            height: 100px;
        }
    }
</style>
