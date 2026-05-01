<template>
    <div class="about-container">
        <h2>欢迎来到关于界面</h2>
        <div class="about-content">
            <div class="about-card">
                <div class="about-icon">🎯</div>
                <h3>我们的使命</h3>
                <p>致力于打造优秀的用户体验，通过技术创新为用户创造价值。</p>
            </div>
            <div class="about-card">
                <div class="about-icon">👥</div>
                <h3>团队介绍</h3>
                <p>由一群热爱技术的开发者组成，我们追求卓越，不断创新。</p>
            </div>
            <div class="about-card">
                <div class="about-icon">📞</div>
                <h3>联系方式</h3>
                <div class="contact-info">
                    <div class="contact-item">📧 email@example.com</div>
                    <div class="contact-item">📱 +86 123-4567-8900</div>
                    <div class="contact-item">📍 北京市朝阳区</div>
                </div>
            </div>
        </div>
        <div class="stats-section">
            <div class="stat-item">
                <div class="stat-number">500+</div>
                <div class="stat-label">项目完成</div>
            </div>
            <div class="stat-item">
                <div class="stat-number">50+</div>
                <div class="stat-label">团队成员</div>
            </div>
            <div class="stat-item">
                <div class="stat-number">99%</div>
                <div class="stat-label">客户满意</div>
            </div>
        </div>
    </div>
</template>

<script lang="ts" setup name="About">
</script>

<style scoped>
    .about-container {
        padding: 2rem;
        max-width: 1200px;
        margin: 0 auto;
    }

    .about-container h2 {
        text-align: center;
        color: #1a202c;
        font-size: 2rem;
        margin-bottom: 2rem;
        font-weight: 700;
        background: linear-gradient(135deg, #4facfe 0%, #00f2fe 100%);
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
        background-clip: text;
    }

    .about-content {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
        gap: 2rem;
        margin-bottom: 3rem;
    }

    .about-card {
        background: white;
        border-radius: 20px;
        padding: 2rem;
        text-align: center;
        box-shadow: 0 4px 20px rgba(0, 0, 0, 0.08);
        transition: all 0.3s ease;
        border: 1px solid #e2e8f0;
    }

    .about-card:hover {
        transform: translateY(-8px);
        box-shadow: 0 12px 40px rgba(79, 172, 254, 0.15);
        border-color: #4facfe;
    }

    .about-icon {
        font-size: 4rem;
        margin-bottom: 1rem;
        background: linear-gradient(135deg, #4facfe 0%, #00f2fe 100%);
        width: 100px;
        height: 100px;
        border-radius: 50%;
        display: flex;
        align-items: center;
        justify-content: center;
        margin: 0 auto 1rem;
    }

    .about-card h3 {
        color: #2d3748;
        font-size: 1.5rem;
        margin-bottom: 1rem;
    }

    .about-card p {
        color: #718096;
        font-size: 1rem;
        line-height: 1.6;
    }

    .contact-info {
        margin-top: 1rem;
        display: flex;
        flex-direction: column;
        gap: 0.75rem;
    }

    .contact-item {
        color: #4a5568;
        font-size: 0.95rem;
        padding: 0.5rem;
        background: #f7fafc;
        border-radius: 8px;
    }

    .stats-section {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
        gap: 1.5rem;
    }

    .stat-item {
        background: linear-gradient(135deg, #4facfe 0%, #00f2fe 100%);
        border-radius: 16px;
        padding: 2rem;
        text-align: center;
        color: white;
        box-shadow: 0 4px 20px rgba(79, 172, 254, 0.2);
        transition: all 0.3s ease;
    }

    .stat-item:hover {
        transform: scale(1.05);
        box-shadow: 0 8px 30px rgba(79, 172, 254, 0.3);
    }

    .stat-number {
        font-size: 2.5rem;
        font-weight: 700;
        margin-bottom: 0.5rem;
    }

    .stat-label {
        font-size: 1rem;
        opacity: 0.9;
    }

    @media (max-width: 768px) {
        .about-container {
            padding: 1rem;
        }

        .about-container h2 {
            font-size: 1.5rem;
        }

        .about-content {
            grid-template-columns: 1fr;
        }

        .stats-section {
            grid-template-columns: repeat(3, 1fr);
        }

        .stat-number {
            font-size: 1.75rem;
        }
    }
</style>
