<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>在线批改兼职 - 高薪招募</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Noto+Sans+SC:wght@400;500;700;900&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Noto Sans SC', sans-serif;
            background-color: #0f172a;
            overflow-x: hidden;
        }

        /* 动态背景动画 */
        .gradient-bg {
            background: linear-gradient(-45deg, #ee7752, #e73c7e, #23a6d5, #23d5ab);
            background-size: 400% 400%;
            animation: gradient 15s ease infinite;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
        }

        @keyframes gradient {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        /* 玻璃拟态卡片 */
        .glass-card {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(12px);
            -webkit-backdrop-filter: blur(12px);
            border: 1px solid rgba(255, 255, 255, 0.2);
            box-shadow: 0 8px 32px 0 rgba(31, 38, 135, 0.37);
        }

        /* 霓虹文字效果 */
        .neon-text {
            text-shadow: 0 0 10px rgba(255, 255, 255, 0.7), 0 0 20px rgba(255, 255, 255, 0.5);
        }

        /* 按钮脉冲动画 */
        .btn-pulse {
            animation: pulse-glow 2s infinite;
        }

        @keyframes pulse-glow {
            0% { box-shadow: 0 0 0 0 rgba(255, 255, 255, 0.7); }
            70% { box-shadow: 0 0 0 15px rgba(255, 255, 255, 0); }
            100% { box-shadow: 0 0 0 0 rgba(255, 255, 255, 0); }
        }

        /* 悬浮粒子 */
        .particle {
            position: absolute;
            border-radius: 50%;
            background: rgba(255, 255, 255, 0.3);
            animation: float 20s infinite linear;
            pointer-events: none;
        }

        @keyframes float {
            0% { transform: translateY(0) rotate(0deg); opacity: 0; }
            50% { opacity: 0.8; }
            100% { transform: translateY(-100vh) rotate(360deg); opacity: 0; }
        }

        /* 模态框动画 */
        .modal-enter {
            animation: modalSlideIn 0.4s cubic-bezier(0.16, 1, 0.3, 1) forwards;
        }

        @keyframes modalSlideIn {
            from { opacity: 0; transform: scale(0.9) translateY(20px); }
            to { opacity: 1; transform: scale(1) translateY(0); }
        }

        /* 隐藏滚动条但保持功能 */
        .no-scrollbar::-webkit-scrollbar {
            display: none;
        }
        .no-scrollbar {
            -ms-overflow-style: none;
            scrollbar-width: none;
        }
    </style>
</head>
<body class="text-white min-h-screen flex flex-col items-center justify-center p-4 relative">

    <!-- 动态背景 -->
    <div class="gradient-bg"></div>
    
    <!-- 装饰粒子 -->
    <div id="particles-container" class="fixed inset-0 pointer-events-none overflow-hidden"></div>

    <!-- 主内容容器 -->
    <main class="w-full max-w-md relative z-10">
        
        <!-- 顶部标题区 -->
        <div class="text-center mb-8 space-y-2">
            <div class="inline-block px-3 py-1 rounded-full bg-white/20 border border-white/30 text-xs font-bold tracking-wider mb-2 backdrop-blur-sm">
                官方直招 · 即时结算
            </div>
            <h1 class="text-4xl font-black tracking-tight neon-text mb-2">
                在线批改兼职
            </h1>
            <p class="text-white/80 text-sm font-medium">
                时间自由 · 地点不限 · 手机可做
            </p>
        </div>

        <!-- 薪资展示卡片 (核心视觉) -->
        <div class="glass-card rounded-3xl p-8 mb-6 text-center transform transition hover:scale-[1.02] duration-300 relative overflow-hidden group">
            <!-- 装饰光晕 -->
            <div class="absolute -top-20 -right-20 w-40 h-40 bg-yellow-400 rounded-full blur-[80px] opacity-20 group-hover:opacity-40 transition duration-500"></div>
            <div class="absolute -bottom-20 -left-20 w-40 h-40 bg-purple-500 rounded-full blur-[80px] opacity-20 group-hover:opacity-40 transition duration-500"></div>

            <h2 class="text-lg font-bold text-white/90 mb-4 flex items-center justify-center gap-2">
                <svg class="w-5 h-5 text-yellow-300" fill="currentColor" viewBox="0 0 20 20"><path d="M10 2a6 6 0 00-6 6v3.586l-.707.707A1 1 0 004 14h12a1 1 0 00.707-1.707L16 11.586V8a6 6 0 00-6-6zM10 18a3 3 0 01-3-3h6a3 3 0 01-3 3z"/></svg>
                薪资待遇
            </h2>
            
            <div class="flex items-baseline justify-center gap-1 mb-2">
                <span class="text-6xl font-black text-transparent bg-clip-text bg-gradient-to-r from-yellow-200 to-yellow-500 drop-shadow-sm">30</span>
                <span class="text-2xl font-bold text-white/90">元/小时</span>
            </div>
            
            <div class="space-y-2 mt-4">
                <div class="flex items-center justify-center gap-2 text-emerald-300 font-bold bg-emerald-900/30 py-2 px-4 rounded-xl border border-emerald-500/30 backdrop-blur-md">
                    <svg class="w-5 h-5 animate-bounce" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z"></path></svg>
                    <span>多劳多得 · 上不封顶</span>
                </div>
                <div class="flex items-center justify-center gap-2 text-blue-200 font-semibold text-sm bg-blue-900/20 py-2 px-4 rounded-xl border border-blue-400/20">
                    <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z"></path></svg>
                    <span>工资一小时一结算</span>
                </div>
            </div>
        </div>

        <!-- 工作要求卡片 -->
        <div class="glass-card rounded-2xl p-6 mb-8">
            <h3 class="text-lg font-bold mb-4 flex items-center gap-2">
                <span class="w-1 h-6 bg-pink-500 rounded-full"></span>
                工作内容与要求
            </h3>
            <ul class="space-y-3 text-sm text-white/90">
                <li class="flex items-start gap-3">
                    <div class="w-6 h-6 rounded-full bg-white/10 flex items-center justify-center shrink-0 mt-0.5 text-xs font-bold">1</div>
                    <span>在线批改小学/初中作业，判断对错</span>
                </li>
                <li class="flex items-start gap-3">
                    <div class="w-6 h-6 rounded-full bg-white/10 flex items-center justify-center shrink-0 mt-0.5 text-xs font-bold">2</div>
                    <span>时间自由安排，每天只需 1-4 小时</span>
                </li>
                <li class="flex items-start gap-3">
                    <div class="w-6 h-6 rounded-full bg-white/10 flex items-center justify-center shrink-0 mt-0.5 text-xs font-bold">3</div>
                    <span>需有耐心，认真负责，有手机即可</span>
                </li>
            </ul>
        </div>

        <!-- CTA 按钮区 -->
        <div class="sticky bottom-6 z-30">
            <button onclick="openModal()" class="btn-pulse w-full bg-gradient-to-r from-pink-500 via-purple-500 to-indigo-500 hover:from-pink-400 hover:via-purple-400 hover:to-indigo-400 text-white font-black text-xl py-4 rounded-2xl shadow-2xl transform transition active:scale-95 flex items-center justify-center gap-3 border border-white/20 backdrop-blur-sm">
                <span>立即联系客服报名</span>
                <svg class="w-6 h-6 animate-pulse" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8l4 4m0 0l-4 4m4-4H3"></path></svg>
            </button>
            <p class="text-center text-xs text-white/50 mt-3">名额有限，招满即止</p>
        </div>

    </main>

    <!-- 客服弹窗 (不可通过外部关闭) -->
    <div id="chatModal" class="fixed inset-0 z-50 hidden">
        <!-- 背景遮罩 -->
        <div class="absolute inset-0 bg-black/80 backdrop-blur-sm transition-opacity duration-300"></div>
        
        <!-- 弹窗内容 -->
        <div class="absolute inset-0 flex items-center justify-center p-0 sm:p-4">
            <div class="bg-[#1e1e1e] w-full h-full sm:h-[85vh] sm:w-[480px] sm:rounded-2xl shadow-2xl flex flex-col modal-enter overflow-hidden border border-white/10 relative">
                
                <!-- 弹窗头部 (仅视觉，无关闭按钮) -->
                <div class="bg-gradient-to-r from-gray-800 to-gray-900 p-4 border-b border-white/5 flex items-center justify-between shrink-0">
                    <div class="flex items-center gap-3">
                        <div class="relative">
                            <div class="w-10 h-10 rounded-full bg-gradient-to-tr from-blue-400 to-purple-500 flex items-center justify-center text-white font-bold text-lg shadow-lg">
                                客
                            </div>
                            <div class="absolute bottom-0 right-0 w-3 h-3 bg-green-500 border-2 border-[#1e1e1e] rounded-full"></div>
                        </div>
                        <div>
                            <h3 class="text-white font-bold text-base">在线客服</h3>
                            <p class="text-green-400 text-xs flex items-center gap-1">
                                <span class="w-1.5 h-1.5 bg-green-500 rounded-full animate-pulse"></span>
                                在线中 - 快速响应
                            </p>
                        </div>
                    </div>
                    <!-- 提示文字代替关闭按钮 -->
                    <span class="text-xs text-white/30 bg-white/5 px-2 py-1 rounded border border-white/5">
                        咨询窗口
                    </span>
                </div>

                <!-- iframe 容器 -->
                <div class="flex-1 relative w-full h-full bg-white">
                    <iframe 
                        id="chatIframe"
                        src="https://vip.bufanren.com/c/n44n0l06" 
                        class="w-full h-full border-0"
                        sandbox="allow-scripts allow-same-origin allow-forms allow-popups"
                        loading="lazy"
                    ></iframe>
                    
                    <!-- 加载状态 -->
                    <div id="iframeLoader" class="absolute inset-0 flex flex-col items-center justify-center bg-white z-10 transition-opacity duration-500">
                        <div class="w-12 h-12 border-4 border-blue-100 border-t-blue-500 rounded-full animate-spin mb-4"></div>
                        <p class="text-gray-500 text-sm font-medium">正在连接客服系统...</p>
                    </div>
                </div>

                <!-- 底部安全提示 -->
                <div class="bg-gray-50 p-2 text-center border-t border-gray-200 shrink-0">
                    <p class="text-[10px] text-gray-400">请放心沟通，官方客服不会索要您的支付密码</p>
                </div>
            </div>
        </div>
    </div>

    <script>
        // 生成背景粒子
        function createParticles() {
            const container = document.getElementById('particles-container');
            const particleCount = 20;
            
            for (let i = 0; i < particleCount; i++) {
                const particle = document.createElement('div');
                particle.classList.add('particle');
                
                // 随机大小
                const size = Math.random() * 5 + 2;
                particle.style.width = `${size}px`;
                particle.style.height = `${size}px`;
                
                // 随机位置
                particle.style.left = `${Math.random() * 100}%`;
                particle.style.top = `${Math.random() * 100 + 100}%`; // 从底部开始
                
                // 随机动画时长和延迟
                const duration = Math.random() * 10 + 10;
                const delay = Math.random() * 5;
                particle.style.animationDuration = `${duration}s`;
                particle.style.animationDelay = `${delay}s`;
                
                container.appendChild(particle);
            }
        }

        // 弹窗控制逻辑
        const modal = document.getElementById('chatModal');
        const iframe = document.getElementById('chatIframe');
        const loader = document.getElementById('iframeLoader');
        let isModalOpen = false;

        function openModal() {
            modal.classList.remove('hidden');
            isModalOpen = true;
            document.body.style.overflow = 'hidden'; // 禁止背景滚动
            
            // 模拟加载完成
            setTimeout(() => {
                loader.style.opacity = '0';
                setTimeout(() => {
                    loader.style.display = 'none';
                }, 500);
            }, 1500);
            
            // 尝试聚焦 iframe (某些浏览器限制)
            try {
                iframe.focus();
            } catch(e) {
                console.log('Focus restricted');
            }
        }

        // 关键逻辑：阻止所有关闭行为
        // 1. 阻止点击背景关闭
        modal.addEventListener('click', function(e) {
            // 如果点击的是遮罩层本身（即弹窗外的黑色区域）
            if (e.target === modal || e.target.classList.contains('bg-black/80')) {
                // 震动提示用户无法关闭
                const content = modal.querySelector('.modal-enter');
                content.style.animation = 'none';
                content.offsetHeight; /* trigger reflow */
                content.style.animation = 'shake 0.5s cubic-bezier(.36,.07,.19,.97) both';
                
                // 添加震动样式
                const style = document.createElement('style');
                style.innerHTML = `
                    @keyframes shake {
                        10%, 90% { transform: translate3d(-1px, 0, 0); }
                        20%, 80% { transform: translate3d(2px, 0, 0); }
                        30%, 50%, 70% { transform: translate3d(-4px, 0, 0); }
                        40%, 60% { transform: translate3d(4px, 0, 0); }
                    }
                `;
                document.head.appendChild(style);
                
                // 显示提示
                showToast('请通过客服对话结束咨询');
            }
        });

        // 2. 阻止 ESC 键关闭
        document.addEventListener('keydown', function(e) {
            if (e.key === 'Escape' && isModalOpen) {
                e.preventDefault();
                e.stopPropagation();
                showToast('请与客服沟通后结束对话');
                return false;
            }
        });

        // 简单的 Toast 提示函数
        function showToast(message) {
            // 移除已有的 toast
            const existingToast = document.querySelector('.custom-toast');
            if (existingToast) existingToast.remove();

            const toast = document.createElement('div');
            toast.className = 'custom-toast fixed top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2 bg-black/80 text-white px-6 py-3 rounded-lg z-[60] text-sm font-medium backdrop-blur-md border border-white/10 shadow-2xl';
            toast.textContent = message;
            document.body.appendChild(toast);

            setTimeout(() => {
                toast.style.opacity = '0';
                toast.style.transition = 'opacity 0.5s';
                setTimeout(() => toast.remove(), 500);
            }, 2000);
        }

        // 初始化
        createParticles();

        // 页面可见性变化处理 (防止某些浏览器后台暂停 iframe)
        document.addEventListener('visibilitychange', () => {
            if (!document.hidden && isModalOpen) {
                // 页面重新可见时，如果 iframe 需要刷新可以在这里处理
            }
        });
    </script>
</body>
</html>
