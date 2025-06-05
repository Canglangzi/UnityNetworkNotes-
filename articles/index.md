<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>我的第一个HTML页面</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://cdn.jsdelivr.net/npm/font-awesome@4.7.0/css/font-awesome.min.css" rel="stylesheet">
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        primary: '#3B82F6',
                        secondary: '#10B981',
                        accent: '#8B5CF6',
                        dark: '#1E293B',
                        light: '#F8FAFC'
                    },
                    fontFamily: {
                        sans: ['Inter', 'system-ui', 'sans-serif'],
                    },
                }
            }
        }
    </script>
    <style type="text/tailwindcss">
        @layer utilities {
            .content-auto {
                content-visibility: auto;
            }
            .text-shadow {
                text-shadow: 0 2px 4px rgba(0,0,0,0.1);
            }
            .transition-custom {
                transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
            }
        }
    </style>
</head>
<body class="bg-gray-50 font-sans text-dark">
    <!-- 导航栏 -->
    <header class="sticky top-0 z-50 bg-white/90 backdrop-blur-sm shadow-sm transition-custom">
        <div class="container mx-auto px-4 py-3 flex justify-between items-center">
            <div class="flex items-center space-x-2">
                <i class="fa fa-code text-primary text-2xl"></i>
                <h1 class="text-xl font-bold text-dark">WebPage</h1>
            </div>
            <nav class="hidden md:flex items-center space-x-8">
                <a href="#home" class="text-dark hover:text-primary transition-custom font-medium">首页</a>
                <a href="#features" class="text-dark hover:text-primary transition-custom font-medium">特性</a>
                <a href="#gallery" class="text-dark hover:text-primary transition-custom font-medium">图库</a>
                <a href="#contact" class="text-dark hover:text-primary transition-custom font-medium">联系我们</a>
            </nav>
            <button class="md:hidden text-dark text-xl">
                <i class="fa fa-bars"></i>
            </button>
        </div>
    </header>

    <!DOCTYPE html>
    <html lang="zh-CN">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Markdown Viewer</title>
        <script src="https://cdn.tailwindcss.com"></script>
        <link href="https://cdn.jsdelivr.net/npm/font-awesome@4.7.0/css/font-awesome.min.css" rel="stylesheet">
        <script src="https://cdn.jsdelivr.net/npm/marked@4.2.12/marked.min.js"></script>
        <script src="https://cdn.jsdelivr.net/npm/highlight.js@11.7.0/lib/highlight.min.js"></script>
        <link href="https://cdn.jsdelivr.net/npm/highlight.js@11.7.0/styles/github-dark.min.css" rel="stylesheet">
        <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
        
        <script>
            tailwind.config = {
                theme: {
                    extend: {
                        colors: {
                            primary: '#3B82F6',
                            secondary: '#10B981',
                            accent: '#8B5CF6',
                            dark: '#1E293B',
                            light: '#F8FAFC',
                            neutral: {
                                100: '#F3F4F6',
                                200: '#E5E7EB',
                                300: '#D1D5DB',
                                400: '#9CA3AF',
                                500: '#6B7280',
                                600: '#4B5563',
                                700: '#374151',
                                800: '#1F2937',
                                900: '#111827'
                            }
                        },
                        fontFamily: {
                            inter: ['Inter', 'sans-serif'],
                            mono: ['Consolas', 'Monaco', 'monospace']
                        },
                        boxShadow: {
                            'custom': '0 4px 20px rgba(0, 0, 0, 0.08)',
                            'hover': '0 8px 30px rgba(0, 0, 0, 0.12)'
                        }
                    }
                }
            }
        </script>
        
        <style type="text/tailwindcss">
            @layer utilities {
                .content-auto {
                    content-visibility: auto;
                }
                .scrollbar-hide::-webkit-scrollbar {
                    display: none;
                }
                .scrollbar-hide {
                    -ms-overflow-style: none;
                    scrollbar-width: none;
                }
                .markdown-content h1 {
                    @apply text-2xl font-bold mb-4 mt-6 text-neutral-800;
                }
                .markdown-content h2 {
                    @apply text-xl font-bold mb-3 mt-5 text-neutral-800;
                }
                .markdown-content h3 {
                    @apply text-lg font-bold mb-2 mt-4 text-neutral-800;
                }
                .markdown-content p {
                    @apply mb-4 text-neutral-700 leading-relaxed;
                }
                .markdown-content a {
                    @apply text-primary hover:underline;
                }
                .markdown-content ul {
                    @apply list-disc pl-5 mb-4 space-y-1;
                }
                .markdown-content ol {
                    @apply list-decimal pl-5 mb-4 space-y-1;
                }
                .markdown-content blockquote {
                    @apply border-l-4 border-primary/30 pl-4 italic text-neutral-600 my-4;
                }
                .markdown-content code:not(pre code) {
                    @apply bg-neutral-100 text-neutral-800 px-1 py-0.5 rounded text-sm font-mono;
                }
                .markdown-content pre {
                    @apply bg-neutral-800 text-white p-4 rounded-lg my-4 overflow-x-auto;
                }
                .markdown-content img {
                    @apply max-w-full rounded-lg my-4;
                }
                .markdown-content table {
                    @apply w-full border-collapse my-4;
                }
                .markdown-content th {
                    @apply border border-neutral-300 bg-neutral-100 px-4 py-2 text-left;
                }
                .markdown-content td {
                    @apply border border-neutral-300 px-4 py-2;
                }
            }
        </style>
    </head>
    <body class="font-inter bg-neutral-50 text-neutral-800 min-h-screen flex flex-col">
        <!-- 顶部导航栏 -->
        <header class="bg-white shadow-sm sticky top-0 z-50 transition-all duration-300">
            <div class="container mx-auto px-4">
                <div class="flex items-center justify-between h-16">
                    <!-- 左侧Logo和标题 -->
                    <div class="flex items-center space-x-2">
                        <i class="fa fa-markdown text-primary text-2xl"></i>
                        <h1 class="text-xl font-bold text-neutral-800">Markdown Viewer</h1>
                    </div>
                    
                    <!-- 中央搜索栏 -->
                    <div class="hidden md:flex flex-1 max-w-md mx-8">
                        <div class="relative w-full">
                            <input type="text" id="search-input" placeholder="搜索文档..." class="w-full pl-10 pr-4 py-2 rounded-lg border border-neutral-300 focus:outline-none focus:ring-2 focus:ring-primary/30 focus:border-primary transition-all">
                            <i class="fa fa-search absolute left-3 top-1/2 transform -translate-y-1/2 text-neutral-400"></i>
                        </div>
                    </div>
                    
                    <!-- 右侧工具栏 -->
                    <div class="flex items-center space-x-4">
                        <button id="theme-toggle" class="p-2 rounded-full hover:bg-neutral-100 transition-colors">
                            <i class="fa fa-moon-o text-neutral-600"></i>
                        </button>
                        <button id="upload-btn" class="p-2 rounded-full hover:bg-neutral-100 transition-colors">
                            <i class="fa fa-upload text-neutral-600"></i>
                        </button>
                        <input type="file" id="file-input" accept=".md" class="hidden">
                        <button id="settings-btn" class="p-2 rounded-full hover:bg-neutral-100 transition-colors">
                            <i class="fa fa-cog text-neutral-600"></i>
                        </button>
                    </div>
                </div>
            </div>
        </header>
    
        <!-- 主内容区 -->
        <main class="flex-1 flex overflow-hidden">
            <!-- 左侧文件列表 -->
            <aside class="w-64 bg-white shadow-sm border-r border-neutral-200 hidden md:block overflow-y-auto scrollbar-hide transition-all duration-300" id="sidebar">
                <div class="p-4 border-b border-neutral-200">
                    <div class="flex items-center justify-between">
                        <h2 class="font-semibold text-neutral-800">我的文档</h2>
                        <button id="new-file-btn" class="text-primary hover:text-primary/80">
                            <i class="fa fa-plus-circle"></i>
                        </button>
                    </div>
                    <div class="mt-3 relative">
                        <input type="text" placeholder="筛选文档..." class="w-full pl-8 pr-3 py-2 rounded-lg border border-neutral-200 text-sm focus:outline-none focus:ring-2 focus:ring-primary/30 focus:border-primary">
                        <i class="fa fa-filter absolute left-3 top-1/2 transform -translate-y-1/2 text-neutral-400 text-sm"></i>
                    </div>
                </div>
                
                <div class="p-2">
                    <div class="mb-3 px-3 py-2 text-xs font-semibold text-neutral-500 uppercase tracking-wider">最近使用</div>
                    <div class="space-y-1">
                        <div class="file-item px-3 py-2 rounded-lg bg-primary/5 border-l-4 border-primary cursor-pointer hover:bg-primary/10 transition-colors">
                            <div class="flex items-center justify-between">
                                <span class="font-medium text-neutral-800 truncate">README.md</span>
                                <i class="fa fa-star text-primary text-xs"></i>
                            </div>
                            <div class="text-xs text-neutral-500 mt-1">今天 14:30</div>
                        </div>
                        <div class="file-item px-3 py-2 rounded-lg cursor-pointer hover:bg-neutral-100 transition-colors">
                            <div class="flex items-center justify-between">
                                <span class="text-neutral-700 truncate">documentation.md</span>
                                <i class="fa fa-clock-o text-neutral-400 text-xs"></i>
                            </div>
                            <div class="text-xs text-neutral-500 mt-1">昨天 09:15</div>
                        </div>
                        <div class="file-item px-3 py-2 rounded-lg cursor-pointer hover:bg-neutral-100 transition-colors">
                            <div class="flex items-center justify-between">
                                <span class="text-neutral-700 truncate">tutorial.md</span>
                                <i class="fa fa-clock-o text-neutral-400 text-xs"></i>
                            </div>
                            <div class="text-xs text-neutral-500 mt-1">2023-06-01</div>
                        </div>
                    </div>
                    
                    <div class="mt-4 mb-3 px-3 py-2 text-xs font-semibold text-neutral-500 uppercase tracking-wider">项目文档</div>
                    <div class="space-y-1">
                        <div class="file-item px-3 py-2 rounded-lg cursor-pointer hover:bg-neutral-100 transition-colors">
                            <div class="flex items-center justify-between">
                                <span class="text-neutral-700 truncate">architecture.md</span>
                                <i class="fa fa-folder-o text-neutral-400 text-xs"></i>
                            </div>
                            <div class="text-xs text-neutral-500 mt-1">2023-05-28</div>
                        </div>
                        <div class="file-item px-3 py-2 rounded-lg cursor-pointer hover:bg-neutral-100 transition-colors">
                            <div class="flex items-center justify-between">
                                <span class="text-neutral-700 truncate">guidelines.md</span>
                                <i class="fa fa-folder-o text-neutral-400 text-xs"></i>
                            </div>
                            <div class="text-xs text-neutral-500 mt-1">2023-05-25</div>
                        </div>
                    </div>
                    
                    <div class="mt-4 mb-3 px-3 py-2 text-xs font-semibold text-neutral-500 uppercase tracking-wider">其他</div>
                    <div class="space-y-1">
                        <div class="file-item px-3 py-2 rounded-lg cursor-pointer hover:bg-neutral-100 transition-colors">
                            <div class="flex items-center justify-between">
                                <span class="text-neutral-700 truncate">notes.md</span>
                                <i class="fa fa-file-text-o text-neutral-400 text-xs"></i>
                            </div>
                            <div class="text-xs text-neutral-500 mt-1">2023-05-20</div>
                        </div>
                    </div>
                </div>
            </aside>
            
            <!-- 移动端菜单按钮 -->
            <button id="mobile-menu-btn" class="md:hidden fixed bottom-6 left-6 bg-white rounded-full shadow-lg p-3 z-40">
                <i class="fa fa-bars text-neutral-700"></i>
            </button>
            
            <!-- 中央内容区 -->
            <div class="flex-1 overflow-y-auto p-4 md:p-6 lg:p-8 bg-neutral-50">
                <div class="max-w-5xl mx-auto">
                    <!-- 文件信息栏 -->
                    <div class="mb-6 flex flex-col sm:flex-row sm:items-center justify-between gap-4">
                        <div>
                            <h2 class="text-[clamp(1.5rem,3vw,2rem)] font-bold text-neutral-800">README.md</h2>
                            <div class="flex items-center mt-1 text-sm text-neutral-500">
                                <span>上次编辑: 今天 14:30</span>
                                <span class="mx-2">•</span>
                                <span>3.2 KB</span>
                            </div>
                        </div>
                        <div class="flex items-center space-x-2">
                            <button class="p-2 rounded-lg hover:bg-neutral-100 transition-colors text-neutral-600" title="编辑">
                                <i class="fa fa-pencil"></i>
                            </button>
                            <button class="p-2 rounded-lg hover:bg-neutral-100 transition-colors text-neutral-600" title="历史版本">
                                <i class="fa fa-history"></i>
                            </button>
                            <button class="p-2 rounded-lg hover:bg-neutral-100 transition-colors text-neutral-600" title="分享">
                                <i class="fa fa-share-alt"></i>
                            </button>
                            <button class="p-2 rounded-lg hover:bg-neutral-100 transition-colors text-neutral-600" title="下载">
                                <i class="fa fa-download"></i>
                            </button>
                        </div>
                    </div>
                    
                    <!-- 文档内容预览 -->
                    <div class="bg-white rounded-xl shadow-custom p-6 md:p-8 mb-6 transition-all duration-300 hover:shadow-hover">
                        <div id="markdown-content" class="markdown-content">
                            <h1>欢迎使用 Markdown 文档查看器</h1>
                            <p>这是一个现代化的 Markdown 文档查看网站，支持多种 Markdown 语法和代码高亮。</p>
                            
                            <h2>功能特点</h2>
                            <ul>
                                <li>实时预览 Markdown 文档</li>
                                <li>支持代码高亮显示</li>
                                <li>可上传本地 Markdown 文件</li>
                                <li>响应式设计，适配各种设备</li>
                                <li>支持深色/浅色模式切换</li>
                            </ul>
                            
                            <h2>Markdown 语法示例</h2>
                            
                            <h3>标题</h3>
                            <pre><code># 一级标题
    ## 二级标题
    ### 三级标题</code></pre>
                            
                            <h3>列表</h3>
                            <pre><code>1. 有序列表项1
    2. 有序列表项2
       - 无序列表项A
       - 无序列表项B</code></pre>
                            
                            <h3>代码块</h3>
                            <pre><code class="language-python">def fibonacci(n):
        a, b = 0, 1
        for _ in range(n):
            yield a
            a, b = b, a + b</code></pre>
                            
                            <h3>引用</h3>
                            <blockquote>
                                <p>这是一段引用文本，通常用于引用他人的话语或重要的段落。</p>
                            </blockquote>
                            
                            <h3>表格</h3>
                            <pre><code>| 姓名 | 年龄 | 职业 |
    |------|------|------|
    | 张三 | 28   | 工程师 |
    | 李四 | 32   | 设计师 |
    | 王五 | 45   | 产品经理 |</code></pre>
                            
                            <h2>使用方法</h2>
                            <ol>
                                <li>点击右上角的上传按钮选择本地 Markdown 文件</li>
                                <li>从左侧文件列表中选择已有的文档</li>
                                <li>使用顶部的搜索框快速查找文档</li>
                                <li>点击右上角的月亮/太阳图标切换主题</li>
                            </ol>
                            
                            <p>希望这个 Markdown 查看器能帮助你更高效地阅读和管理文档！</p>
                        </div>
                    </div>
                    
                    <!-- 文档信息和操作 -->
                    <div class="flex flex-col sm:flex-row justify-between items-center text-sm text-neutral-500">
                        <div>
                            <span>文档 ID: MD-20230601-001</span>
                            <span class="mx-2">•</span>
                            <span>字数统计: 约 350 字</span>
                        </div>
                        <div class="mt-3 sm:mt-0">
                            <button class="text-primary hover:text-primary/80 flex items-center">
                                <i class="fa fa-bookmark-o mr-1"></i> 收藏文档
                            </button>
                        </div>
                    </div>
                </div>
            </div>
        </main>
    
        <!-- 移动端侧边栏遮罩 -->
        <div id="sidebar-overlay" class="fixed inset-0 bg-black/50 z-40 hidden md:hidden"></div>
    
        <!-- 底部状态栏 -->
        <footer class="bg-white border-t border-neutral-200 py-3 px-4">
            <div class="container mx-auto flex items-center justify-between text-sm text-neutral-500">
                <div>
                    <span>Markdown Viewer v1.0.0</span>
                    <span class="mx-2">•</span>
                    <span>已加载 6 个文档</span>
                </div>
                <div class="flex items-center space-x-4">
                    <span id="word-count">字数统计: 计算中...</span>
                    <button id="feedback-btn" class="text-primary hover:text-primary/80">
                        <i class="fa fa-comment-o mr-1"></i> 反馈建议
                    </button>
                </div>
            </div>
        </footer>
    
        <!-- 上传文件模态框 -->
        <div id="upload-modal" class="fixed inset-0 flex items-center justify-center z-50 hidden">
            <div class="absolute inset-0 bg-black/50 backdrop-blur-sm"></div>
            <div class="bg-white rounded-xl shadow-xl p-6 max-w-md w-full mx-4 relative z-10 transform transition-all duration-300 scale-95 opacity-0" id="modal-content">
                <div class="flex justify-between items-center mb-4">
                    <h3 class="text-lg font-bold text-neutral-800">上传 Markdown 文件</h3>
                    <button id="close-modal" class="text-neutral-400 hover:text-neutral-600">
                        <i class="fa fa-times"></i>
                    </button>
                </div>
                <div class="border-2 border-dashed border-neutral-300 rounded-lg p-8 text-center hover:border-primary transition-colors cursor-pointer" id="drop-area">
                    <i class="fa fa-cloud-upload text-4xl text-neutral-400 mb-3"></i>
                    <p class="text-neutral-600 mb-2">拖放 Markdown 文件到此处，或点击上传</p>
                    <p class="text-xs text-neutral-500">支持 .md 格式文件</p>
                    <input type="file" accept=".md" class="hidden" id="modal-file-input">
                </div>
                <div class="mt-4">
                    <button id="modal-upload-btn" class="w-full bg-primary hover:bg-primary/90 text-white py-2 rounded-lg font-medium transition-colors">
                        选择文件上传
                    </button>
                </div>
            </div>
        </div>
    
        <script>
            // 初始化代码高亮
            document.addEventListener('DOMContentLoaded', () => {
                document.querySelectorAll('pre code').forEach((block) => {
                    hljs.highlightElement(block);
                });
                
                // 计算字数
                updateWordCount();
                
                // 初始化事件监听
                initEventListeners();
            });
            
            // 初始化所有事件监听
            function initEventListeners() {
                // 主题切换
                const themeToggle = document.getElementById('theme-toggle');
                const htmlElement = document.documentElement;
                let isDarkMode = false;
                
                themeToggle.addEventListener('click', () => {
                    isDarkMode = !isDarkMode;
                    if (isDarkMode) {
                        htmlElement.classList.add('dark');
                        themeToggle.innerHTML = '<i class="fa fa-sun-o text-yellow-400"></i>';
                    } else {
                        htmlElement.classList.remove('dark');
                        themeToggle.innerHTML = '<i class="fa fa-moon-o text-neutral-600"></i>';
                    }
                });
                
                // 上传文件按钮
                const uploadBtn = document.getElementById('upload-btn');
                const fileInput = document.getElementById('file-input');
                
                uploadBtn.addEventListener('click', () => {
                    fileInput.click();
                });
                
                // 文件选择处理
                fileInput.addEventListener('change', (e) => {
                    if (e.target.files.length > 0) {
                        const file = e.target.files[0];
                        if (file.name.endsWith('.md')) {
                            processMarkdownFile(file);
                        } else {
                            alert('请选择Markdown文件 (.md)');
                        }
                    }
                });
                
                // 移动端菜单
                const mobileMenuBtn = document.getElementById('mobile-menu-btn');
                const sidebar = document.getElementById('sidebar');
                const sidebarOverlay = document.getElementById('sidebar-overlay');
                
                mobileMenuBtn.addEventListener('click', () => {
                    sidebar.classList.toggle('hidden');
                    sidebar.classList.toggle('fixed');
                    sidebar.classList.toggle('inset-y-0');
                    sidebar.classList.toggle('left-0');
                    sidebar.classList.toggle('z-40');
                    sidebar.classList.toggle('w-64');
                    sidebarOverlay.classList.toggle('hidden');
                });
                
                sidebarOverlay.addEventListener('click', () => {
                    sidebar.classList.add('hidden');
                    sidebar.classList.remove('fixed', 'inset-y-0', 'left-0', 'z-40', 'w-64');
                    sidebarOverlay.classList.add('hidden');
                });
                
                // 上传模态框
                const uploadModal = document.getElementById('upload-modal');
                const modalContent = document.getElementById('modal-content');
                const closeModal = document.getElementById('close-modal');
                const dropArea = document.getElementById('drop-area');
                const modalFileInput = document.getElementById('modal-file-input');
                const modalUploadBtn = document.getElementById('modal-upload-btn');
                
                uploadBtn.addEventListener('click', () => {
                    uploadModal.classList.remove('hidden');
                    setTimeout(() => {
                        modalContent.classList.remove('scale-95', 'opacity-0');
                        modalContent.classList.add('scale-100', 'opacity-100');
                    }, 10);
                });
                
                closeModal.addEventListener('click', () => {
                    modalContent.classList.remove('scale-100', 'opacity-100');
                    modalContent.classList.add('scale-95', 'opacity-0');
                    setTimeout(() => {
                        uploadModal.classList.add('hidden');
                    }, 300);
                });
                
                dropArea.addEventListener('click', () => {
                    modalFileInput.click();
                });
                
                modalUploadBtn.addEventListener('click', () => {
                    modalFileInput.click();
                });
                
                modalFileInput.addEventListener('change', (e) => {
                    if (e.target.files.length > 0) {
                        const file = e.target.files[0];
                        if (file.name.endsWith('.md')) {
                            processMarkdownFile(file);
                            closeModal.click();
                        } else {
                            alert('请选择Markdown文件 (.md)');
                        }
                    }
                });
                
                // 拖放上传
                ['dragenter', 'dragover', 'dragleave', 'drop'].forEach(eventName => {
                    dropArea.addEventListener(eventName, preventDefaults, false);
                });
                
                function preventDefaults(e) {
                    e.preventDefault();
                    e.stopPropagation();
                }
                
                ['dragenter', 'dragover'].forEach(eventName => {
                    dropArea.addEventListener(eventName, highlight, false);
                });
                
                ['dragleave', 'drop'].forEach(eventName => {
                    dropArea.addEventListener(eventName, unhighlight, false);
                });
                
                function highlight() {
                    dropArea.classList.add('border-primary');
                    dropArea.classList.add('bg-primary/5');
                }
                
                function unhighlight() {
                    dropArea.classList.remove('border-primary');
                    dropArea.classList.remove('bg-primary/5');
                }
                
                dropArea.addEventListener('drop', handleDrop, false);
                
                function handleDrop(e) {
                    const dt = e.dataTransfer;
                    const file = dt.files[0];
                    
                    if (file && file.name.endsWith('.md')) {
                        processMarkdownFile(file);
                        closeModal.click();
                    } else {
                        alert('请拖放Markdown文件 (.md)');
                    }
                }
                
                // 文件项点击
                document.querySelectorAll('.file-item').forEach(item => {
                    item.addEventListener('click', () => {
                        document.querySelectorAll('.file-item').forEach(i => {
                            i.classList.remove('bg-primary/5', 'border-l-4', 'border-primary');
                        });
                        item.classList.add('bg-primary/5', 'border-l-4', 'border-primary');
                        
                        // 模拟加载新文档
                        const fileName = item.querySelector('span').textContent;
                        document.querySelector('h2').textContent = fileName;
                        
                        // 显示加载状态
                        const markdownContent = document.getElementById('markdown-content');
                        markdownContent.innerHTML = `
                            <div class="flex items-center justify-center py-12">
                                <div class="animate-spin rounded-full h-12 w-12 border-t-2 border-b-2 border-primary"></div>
                            </div>
                        `;
                        
                        // 模拟加载延迟
                        setTimeout(() => {
                            // 恢复示例内容
                            markdownContent.innerHTML = `
                                <h1>${fileName}</h1>
                                <p>这是 ${fileName} 的文档内容预览。</p>
                                
                                <h2>文档概述</h2>
                                <p>本文档包含了项目的详细说明和使用指南。</p>
                                
                                <h2>主要内容</h2>
                                <ul>
                                    <li>项目架构</li>
                                    <li>安装步骤</li>
                                    <li>使用方法</li>
                                    <li>API 参考</li>
                                    <li>常见问题</li>
                                </ul>
                                
                                <h2>代码示例</h2>
                                <pre><code class="language-javascript">// 示例代码
    function loadMarkdownFile(file) {
        const reader = new FileReader();
        
        reader.onload = function(event) {
            const content = event.target.result;
            const html = marked.parse(content);
            document.getElementById('markdown-content').innerHTML = html;
            
            // 重新应用代码高亮
            document.querySelectorAll('pre code').forEach((block) => {
                hljs.highlightElement(block);
            });
            
            // 更新字数统计
            updateWordCount();
        };
        
        reader.readAsText(file);
    }</code></pre>
                                
                                <p>感谢使用 Markdown 文档查看器！</p>
                            `;
                            
                            // 重新应用代码高亮
                            document.querySelectorAll('pre code').forEach((block) => {
                                hljs.highlightElement(block);
                            });
                            
                            updateWordCount();
                        }, 800);
                    });
                });
            }
            
            // 处理Markdown文件
            function processMarkdownFile(file) {
                const reader = new FileReader();
                
                reader.onload = function(event) {
                    const content = event.target.result;
                    const html = marked.parse(content);
                    const markdownContent = document.getElementById('markdown-content');
                    
                    // 显示加载状态
                    markdownContent.innerHTML = `
                        <div class="flex items-center justify-center py-12">
                            <div class="animate-spin rounded-full h-12 w-12 border-t-2 border-b-2 border-primary"></div>
                        </div>
                    `;
                    
                    // 延迟显示内容，模拟加载过程
                    setTimeout(() => {
                        markdownContent.innerHTML = html;
                        
                        // 应用代码高亮
                        document.querySelectorAll('pre code').forEach((block) => {
                            hljs.highlightElement(block);
                        });
                        
                        // 更新页面标题
                        document.querySelector('h2').textContent = file.name;
                        
                        // 更新字数统计
                        updateWordCount();
                        
                        // 更新文件列表
                        addFileToList(file);
                    }, 500);
                };
                
                reader.readAsText(file);
            }
            
            // 添加文件到列表
            function addFileToList(file) {
                const fileList = document.querySelector('#sidebar .space-y-1');
                const fileItem = document.createElement('div');
                
                // 格式化日期
                const date = new Date();
                const formattedDate = `${date.getFullYear()}-${String(date.getMonth() + 1).padStart(2, '0')}-${String(date.getDate()).padStart(2, '0')}`;
                
                fileItem.className = 'file-item px-3 py-2 rounded-lg cursor-pointer hover:bg-neutral-100 transition-colors';
                fileItem.innerHTML = `
                    <div class="flex items-center justify-between">
                        <span class="text-neutral-700 truncate">${file.name}</span>
                        <i class="fa fa-clock-o text-neutral-400 text-xs"></i>
                    </div>
                    <div class="text-xs text-neutral-500 mt-1">${formattedDate}</div>
                `;
                
                // 添加点击事件
                fileItem.addEventListener('click', () => {
                    document.querySelectorAll('.file-item').forEach(i => {
                        i.classList.remove('bg-primary/5', 'border-l-4', 'border-primary');
                    });
                    fileItem.classList.add('bg-primary/5', 'border-l-4', 'border-primary');
                    
                    // 处理文件加载
                    processMarkdownFile(file);
                });
                
                // 添加到列表顶部
                if (fileList.firstChild) {
                    fileList.insertBefore(fileItem, fileList.firstChild);
                } else {
                    fileList.appendChild(fileItem);
                }
            }
            
            // 更新字数统计
            function updateWordCount() {
                const content = document.getElementById('markdown-content').textContent;
                const wordCount = content.trim().split(/\s+/).filter(word => word.length > 0).length;
                document.getElementById('word-count').textContent = `字数统计: 约 ${wordCount} 字`;
            }
            
            // 平滑滚动
            document.querySelectorAll('a[href^="#"]').forEach(anchor => {
                anchor.addEventListener('click', function (e) {
                    e.preventDefault();
                    
                    const targetId = this.getAttribute('href');
                    const targetElement = document.querySelector(targetId);
                    
                    if (targetElement) {
                        window.scrollTo({
                            top: targetElement.offsetTop - 80,
                            behavior: 'smooth'
                        });
                    }
                });
            });
            
            // 导航栏滚动效果
            const header = document.querySelector('header');
            
            window.addEventListener('scroll', () => {
                if (window.scrollY > 50) {
                    header.classList.add('shadow-md');
                    header.classList.remove('shadow-sm');
                } else {
                    header.classList.add('shadow-sm');
                    header.classList.remove('shadow-md');
                }
            });
        </script>
    </body>
    </html>
        
</body>
</html>
    