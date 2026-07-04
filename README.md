<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hariharan J | Interactive Premium Portfolio</title>
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Font Awesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;500;600;700;800&family=Fira+Code:wght@400;500;600;700&display=swap" rel="stylesheet">
    <!-- D3.js for Skills Visualization -->
    <script src="https://cdn.jsdelivr.net/npm/d3@7.9.0"></script>
    <style>
        body {
            font-family: 'Plus Jakarta Sans', sans-serif;
            background-color: #030712;
        }
        .code-font {
            font-family: 'Fira Code', monospace;
        }
        /* Custom Glowing Accents */
        .neon-glow-primary {
            box-shadow: 0 0 25px -5px rgba(16, 185, 129, 0.4);
        }
        .neon-glow-cyan {
            box-shadow: 0 0 25px -5px rgba(6, 182, 212, 0.4);
        }
        /* Hide Scrollbar */
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: #030712;
        }
        ::-webkit-scrollbar-thumb {
            background: #1f2937;
            border-radius: 999px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #374151;
        }
    </style>
</head>
<body class="text-gray-100 overflow-x-hidden relative min-h-screen">

    <div class="absolute inset-0 pointer-events-none overflow-hidden z-0">
        <canvas id="particleCanvas" class="w-full h-full opacity-35"></canvas>
    </div>

    <header class="sticky top-0 z-50 backdrop-blur-md bg-gray-950/70 border-b border-gray-800/80 transition-all duration-300">
        <div class="max-w-7xl mx-auto px-6 h-20 flex items-center justify-between">
            <div class="flex items-center space-x-3">
                <div class="h-10 w-10 rounded-xl bg-gradient-to-tr from-emerald-500 to-cyan-500 flex items-center justify-center font-bold text-lg shadow-lg shadow-emerald-500/20">
                    H
                </div>
                <div>
                    <span class="font-extrabold text-lg tracking-tight bg-gradient-to-r from-emerald-400 to-cyan-400 bg-clip-text text-transparent">Hariharan J</span>
                    <span class="block text-xs text-gray-400 code-font">class ProfileEngine {}</span>
                </div>
            </div>
            
            <nav class="hidden md:flex items-center space-x-8">
                <a href="#about" class="text-sm font-medium text-gray-300 hover:text-emerald-400 transition-colors">About</a>
                <a href="#metrics" class="text-sm font-medium text-gray-300 hover:text-emerald-400 transition-colors">Performance Matrix</a>
                <a href="#projects" class="text-sm font-medium text-gray-300 hover:text-emerald-400 transition-colors">Systems</a>
                <a href="#terminal" class="text-sm font-medium text-gray-300 hover:text-emerald-400 transition-colors">System Log</a>
                <a href="#certifications" class="text-sm font-medium text-gray-300 hover:text-emerald-400 transition-colors">Credentials</a>
            </nav>

            <div class="flex items-center space-x-4">
                <a href="mailto:singinghearthari@gmail.com" class="px-4 py-2 text-sm font-semibold rounded-xl bg-emerald-500/10 hover:bg-emerald-500/20 text-emerald-400 border border-emerald-500/20 transition-all duration-300">
                    <i class="fa-regular fa-envelope mr-2"></i>Email Me
                </a>
            </div>
        </div>
    </header>

    <main class="relative z-10 max-w-7xl mx-auto px-6 py-12 space-y-24">
        
        <section id="about" class="grid grid-cols-1 lg:grid-cols-12 gap-12 items-center">
            <div class="lg:col-span-7 space-y-6">
                <div class="inline-flex items-center space-x-2 px-3 py-1 rounded-full bg-emerald-500/10 border border-emerald-500/20 text-emerald-400 text-xs font-semibold">
                    <span class="w-2 h-2 rounded-full bg-emerald-400 animate-ping"></span>
                    <span>Available for Full-Time Roles (Graduating 2026)</span>
                </div>
                
                <h1 class="text-4xl sm:text-6xl font-extrabold tracking-tight leading-none text-white">
                    Building AI That <br/>
                    <span class="bg-gradient-to-r from-emerald-400 via-teal-400 to-cyan-400 bg-clip-text text-transparent">Actually Works</span>
                </h1>
                
                <p class="text-lg text-gray-400 leading-relaxed max-w-2xl">
                    I am an <strong class="text-emerald-400 font-semibold">AI/ML Engineer</strong> and <strong class="text-cyan-400 font-semibold">Full-Stack Developer</strong> specializing in creating stateful intelligence systems. From training custom disease recognition models to scaling live commercial automation microservices, I bridge complex theoretical research and bulletproof production architectures.
                </p>

                <!-- Social Link Grid -->
                <div class="flex flex-wrap gap-4 pt-2">
                    <a href="https://www.linkedin.com/in/hariharan731722205019" target="_blank" class="px-5 py-3 rounded-xl bg-gray-900 border border-gray-800 hover:border-emerald-500/30 text-gray-300 hover:text-emerald-400 flex items-center space-x-3 transition-all duration-300">
                        <i class="fa-brands fa-linkedin text-xl"></i>
                        <span class="text-sm font-semibold">LinkedIn</span>
                    </a>
                    <a href="https://singingheart.neocities.org" target="_blank" class="px-5 py-3 rounded-xl bg-gray-900 border border-gray-800 hover:border-cyan-500/30 text-gray-300 hover:text-cyan-400 flex items-center space-x-3 transition-all duration-300">
                        <i class="fa-solid fa-globe text-xl"></i>
                        <span class="text-sm font-semibold">Portfolio</span>
                    </a>
                    <a href="https://trustism.web.app" target="_blank" class="px-5 py-3 rounded-xl bg-gray-900 border border-gray-800 hover:border-orange-500/30 text-gray-300 hover:text-orange-400 flex items-center space-x-3 transition-all duration-300">
                        <i class="fa-solid fa-rocket text-xl"></i>
                        <span class="text-sm font-semibold">Trustism SaaS</span>
                    </a>
                </div>
            </div>

            <!-- Interactive Terminal Profile Mockup -->
            <div class="lg:col-span-5 relative">
                <div class="absolute -inset-1 rounded-2xl bg-gradient-to-tr from-emerald-500 to-cyan-500 opacity-20 blur-xl"></div>
                <div class="relative rounded-2xl border border-gray-800/80 bg-gray-950/95 overflow-hidden shadow-2xl">
                    <div class="h-10 bg-gray-900/60 border-b border-gray-800/80 px-4 flex items-center justify-between">
                        <div class="flex space-x-1.5">
                            <span class="w-3 h-3 rounded-full bg-red-500/70"></span>
                            <span class="w-3 h-3 rounded-full bg-yellow-500/70"></span>
                            <span class="w-3 h-3 rounded-full bg-emerald-500/70"></span>
                        </div>
                        <span class="text-xs text-gray-500 code-font">bash - portfolio.sh</span>
                        <div class="w-4"></div>
                    </div>
                    <div class="p-6 space-y-4 code-font text-xs md:text-sm text-emerald-400/90 leading-relaxed">
                        <div>
                            <span class="text-gray-500">$</span> <span class="text-white">whoami</span>
                            <p class="text-gray-300 mt-1">
                                Hariharan J | B.Tech IT, Anna University<br>
                                CGPA: 8.5/10 (First Class Track)<br>
                                Academic Thesis: "SEED AI Multimodal Decision Framework"
                            </p>
                        </div>
                        <div>
                            <span class="text-gray-500">$</span> <span class="text-white">cat accomplishments.json</span>
                            <pre class="text-gray-300 mt-1 text-[11px] leading-tight">
{
  "publication": "IJWOS (Smart Agri System)",
  "national_award": "Selected Presenter @ CMTI 2026",
  "hackathon": "IEEE TECHFEST 2025 Runner-Up",
  "business": "Founder @ Trustism (SaaS MSME)"
}</pre>
                        </div>
                        <div>
                            <span class="text-gray-500">$</span> <span class="text-white">sys_status --diagnostic</span>
                            <p class="text-cyan-400 mt-1 flex items-center space-x-2">
                                <span class="inline-block w-2 h-2 rounded-full bg-cyan-400 animate-pulse"></span>
                                <span>All micro-pipelines fully operational.</span>
                            </p>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <section id="metrics" class="space-y-8">
            <div class="text-center max-w-3xl mx-auto space-y-4">
                <h2 class="text-3xl font-bold text-white tracking-tight">Technical Capability Index</h2>
                <p class="text-gray-400 text-sm md:text-base">
                    Quantitative performance map structured across modern deep neural network frameworks, stateful web backends, and responsive design systems.
                </p>
            </div>

            <div class="grid grid-cols-1 lg:grid-cols-3 gap-8">
                <!-- AI / ML Core Capabilities card -->
                <div class="p-6 rounded-2xl bg-gray-900/40 border border-gray-800/80 hover:border-emerald-500/30 transition-all duration-300 space-y-6">
                    <div class="flex items-center justify-between">
                        <span class="text-lg font-bold text-white">AI & Deep Learning</span>
                        <i class="fa-solid fa-brain text-emerald-400 text-xl"></i>
                    </div>
                    <div class="space-y-4 text-sm">
                        <div class="space-y-1">
                            <div class="flex justify-between text-gray-400 text-xs">
                                <span>TensorFlow & CNN Architectures</span>
                                <span class="text-emerald-400 font-semibold">90%</span>
                            </div>
                            <div class="h-2 w-full bg-gray-800 rounded-full overflow-hidden">
                                <div class="h-full bg-gradient-to-r from-emerald-500 to-emerald-400 rounded-full" style="width: 90%"></div>
                            </div>
                        </div>
                        <div class="space-y-1">
                            <div class="flex justify-between text-gray-400 text-xs">
                                <span>Scikit-learn Ensembles (Random Forest)</span>
                                <span class="text-emerald-400 font-semibold">95%</span>
                            </div>
                            <div class="h-2 w-full bg-gray-800 rounded-full overflow-hidden">
                                <div class="h-full bg-gradient-to-r from-emerald-500 to-emerald-400 rounded-full" style="width: 95%"></div>
                            </div>
                        </div>
                        <div class="space-y-1">
                            <div class="flex justify-between text-gray-400 text-xs">
                                <span>NLP & LLM Prompt Pipelines (Gemini)</span>
                                <span class="text-emerald-400 font-semibold">88%</span>
                            </div>
                            <div class="h-2 w-full bg-gray-800 rounded-full overflow-hidden">
                                <div class="h-full bg-gradient-to-r from-emerald-500 to-emerald-400 rounded-full" style="width: 88%"></div>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Full Stack Engineering Card -->
                <div class="p-6 rounded-2xl bg-gray-900/40 border border-gray-800/80 hover:border-cyan-500/30 transition-all duration-300 space-y-6">
                    <div class="flex items-center justify-between">
                        <span class="text-lg font-bold text-white">Engineering Stack</span>
                        <i class="fa-solid fa-layer-group text-cyan-400 text-xl"></i>
                    </div>
                    <div class="space-y-4 text-sm">
                        <div class="space-y-1">
                            <div class="flex justify-between text-gray-400 text-xs">
                                <span>React & Next.js Ecosystems</span>
                                <span class="text-cyan-400 font-semibold">92%</span>
                            </div>
                            <div class="h-2 w-full bg-gray-800 rounded-full overflow-hidden">
                                <div class="h-full bg-gradient-to-r from-cyan-500 to-cyan-400 rounded-full" style="width: 92%"></div>
                            </div>
                        </div>
                        <div class="space-y-1">
                            <div class="flex justify-between text-gray-400 text-xs">
                                <span>Flask Backend & API Infrastructure</span>
                                <span class="text-cyan-400 font-semibold">85%</span>
                            </div>
                            <div class="h-2 w-full bg-gray-800 rounded-full overflow-hidden">
                                <div class="h-full bg-gradient-to-r from-cyan-500 to-cyan-400 rounded-full" style="width: 85%"></div>
                            </div>
                        </div>
                        <div class="space-y-1">
                            <div class="flex justify-between text-gray-400 text-xs">
                                <span>State Sync & Relational/NoSQL DBs</span>
                                <span class="text-cyan-400 font-semibold">87%</span>
                            </div>
                            <div class="h-2 w-full bg-gray-800 rounded-full overflow-hidden">
                                <div class="h-full bg-gradient-to-r from-cyan-500 to-cyan-400 rounded-full" style="width: 87%"></div>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Cloud & Tooling Card -->
                <div class="p-6 rounded-2xl bg-gray-900/40 border border-gray-800/80 hover:border-purple-500/30 transition-all duration-300 space-y-6">
                    <div class="flex items-center justify-between">
                        <span class="text-lg font-bold text-white">System Architecture</span>
                        <i class="fa-solid fa-gears text-purple-400 text-xl"></i>
                    </div>
                    <div class="space-y-4 text-sm">
                        <div class="space-y-1">
                            <div class="flex justify-between text-gray-400 text-xs">
                                <span>Micro-architecture & Cloud (Azure)</span>
                                <span class="text-purple-400 font-semibold">80%</span>
                            </div>
                            <div class="h-2 w-full bg-gray-800 rounded-full overflow-hidden">
                                <div class="h-full bg-gradient-to-r from-purple-500 to-purple-400 rounded-full" style="width: 80%"></div>
                            </div>
                        </div>
                        <div class="space-y-1">
                            <div class="flex justify-between text-gray-400 text-xs">
                                <span>Linux Kernel Systems & Scripting</span>
                                <span class="text-purple-400 font-semibold">85%</span>
                            </div>
                            <div class="h-2 w-full bg-gray-800 rounded-full overflow-hidden">
                                <div class="h-full bg-gradient-to-r from-purple-500 to-purple-400 rounded-full" style="width: 85%"></div>
                            </div>
                        </div>
                        <div class="space-y-1">
                            <div class="flex justify-between text-gray-400 text-xs">
                                <span>Continuous Deployment & Versioning</span>
                                <span class="text-purple-400 font-semibold">90%</span>
                            </div>
                            <div class="h-2 w-full bg-gray-800 rounded-full overflow-hidden">
                                <div class="h-full bg-gradient-to-r from-purple-500 to-purple-400 rounded-full" style="width: 90%"></div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <section id="projects" class="space-y-12">
            <div class="flex flex-col md:flex-row md:items-end justify-between gap-4">
                <div class="space-y-2">
                    <h2 class="text-3xl font-bold text-white tracking-tight">Active Production Architectures</h2>
                    <p class="text-gray-400 max-w-2xl text-sm">
                        Filter through deployed systems. Each contains complete architectural details, performance metrics, and production access channels.
                    </p>
                </div>
                <!-- Interactive Filter Tabs -->
                <div class="flex items-center space-x-2 bg-gray-950 p-1.5 rounded-xl border border-gray-800/80 self-start">
                    <button onclick="filterCategory('All')" id="btn-All" class="project-tab px-4 py-2 text-xs font-semibold rounded-lg bg-emerald-500 text-gray-950 transition-all duration-300">All Systems</button>
                    <button onclick="filterCategory('AI/ML')" id="btn-AI/ML" class="project-tab px-4 py-2 text-xs font-semibold rounded-lg text-gray-400 hover:text-white transition-all duration-300">Intelligent Engines</button>
                    <button onclick="filterCategory('SaaS')" id="btn-SaaS" class="project-tab px-4 py-2 text-xs font-semibold rounded-lg text-gray-400 hover:text-white transition-all duration-300">SaaS Systems</button>
                </div>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-2 gap-8" id="projectsGrid">
                
                <!-- SEED AI -->
                <div class="project-card-item rounded-2xl border border-gray-800 bg-gray-950 p-6 flex flex-col justify-between space-y-6 transition-all duration-300 hover:border-emerald-500/30 hover:scale-[1.01]" data-category="AI/ML">
                    <div class="space-y-4">
                        <div class="flex items-center justify-between">
                            <span class="text-xs font-semibold text-emerald-400 uppercase tracking-widest code-font">AI/ML Precision Engine</span>
                            <span class="px-2.5 py-1 rounded-full bg-emerald-500/10 text-emerald-400 text-xs border border-emerald-500/20 font-semibold">Published Research</span>
                        </div>
                        <h3 class="text-2xl font-bold text-white">SEED AI Support System</h3>
                        <p class="text-sm text-gray-400 leading-relaxed">
                            Precision agricultural neural system. Orchestrates CNN models for plant anomaly classification, integrated with a random forest regressor and Gemini Agentic support loops.
                        </p>
                        <div class="flex flex-wrap gap-2 pt-2">
                            <span class="px-2 py-1 rounded bg-gray-900 border border-gray-800 text-[11px] text-gray-300 font-mono">React</span>
                            <span class="px-2 py-1 rounded bg-gray-900 border border-gray-800 text-[11px] text-gray-300 font-mono">Flask API</span>
                            <span class="px-2 py-1 rounded bg-gray-900 border border-gray-800 text-[11px] text-gray-300 font-mono">TensorFlow</span>
                            <span class="px-2 py-1 rounded bg-gray-900 border border-gray-800 text-[11px] text-gray-300 font-mono">Gemini API</span>
                        </div>
                    </div>
                    <div class="flex items-center justify-between pt-4 border-t border-gray-900">
                        <a href="https://seed-ai-hari.web.app" target="_blank" class="text-xs font-semibold text-emerald-400 hover:text-emerald-300 transition-colors flex items-center space-x-2">
                            <span>Execute Production Demo</span>
                            <i class="fa-solid fa-arrow-right text-xs"></i>
                        </a>
                        <span class="text-xs text-gray-500">Live Deploy</span>
                    </div>
                </div>

                <!-- Trustism -->
                <div class="project-card-item rounded-2xl border border-gray-800 bg-gray-950 p-6 flex flex-col justify-between space-y-6 transition-all duration-300 hover:border-orange-500/30 hover:scale-[1.01]" data-category="SaaS">
                    <div class="space-y-4">
                        <div class="flex items-center justify-between">
                            <span class="text-xs font-semibold text-orange-400 uppercase tracking-widest code-font">Commercially Live SaaS</span>
                            <span class="px-2.5 py-1 rounded-full bg-orange-500/10 text-orange-400 text-xs border border-orange-500/20 font-semibold">MSME Registered</span>
                        </div>
                        <h3 class="text-2xl font-bold text-white">Trustism Workflow Automation</h3>
                        <p class="text-sm text-gray-400 leading-relaxed">
                            B2B cloud resource manager. Fully automates document processing, automated context-aware client pipelines, and real-time state machine sync across small enterprise divisions.
                        </p>
                        <div class="flex flex-wrap gap-2 pt-2">
                            <span class="px-2 py-1 rounded bg-gray-900 border border-gray-800 text-[11px] text-gray-300 font-mono">React v18</span>
                            <span class="px-2 py-1 rounded bg-gray-900 border border-gray-800 text-[11px] text-gray-300 font-mono">Firebase</span>
                            <span class="px-2 py-1 rounded bg-gray-900 border border-gray-800 text-[11px] text-gray-300 font-mono">Google Apps Script</span>
                            <span class="px-2 py-1 rounded bg-gray-900 border border-gray-800 text-[11px] text-gray-300 font-mono">REST APIs</span>
                        </div>
                    </div>
                    <div class="flex items-center justify-between pt-4 border-t border-gray-900">
                        <a href="https://trustism.web.app" target="_blank" class="text-xs font-semibold text-orange-400 hover:text-orange-300 transition-colors flex items-center space-x-2">
                            <span>Execute Production Demo</span>
                            <i class="fa-solid fa-arrow-right text-xs"></i>
                        </a>
                        <span class="text-xs text-gray-500 font-semibold text-green-400">Serving Clients</span>
                    </div>
                </div>

                <!-- Predignosys AI -->
                <div class="project-card-item rounded-2xl border border-gray-800 bg-gray-950 p-6 flex flex-col justify-between space-y-6 transition-all duration-300 hover:border-red-500/30 hover:scale-[1.01]" data-category="AI/ML">
                    <div class="space-y-4">
                        <div class="flex items-center justify-between">
                            <span class="text-xs font-semibold text-red-400 uppercase tracking-widest code-font">Clinical Predictor</span>
                            <span class="px-2.5 py-1 rounded-full bg-red-500/10 text-red-400 text-xs border border-red-500/20 font-semibold">Predictive Pipeline</span>
                        </div>
                        <h3 class="text-2xl font-bold text-white">Predignosys Diagnostic Suite</h3>
                        <p class="text-sm text-gray-400 leading-relaxed">
                            Machine learning predictive platform. Utilizes trained random forest ensemble classifiers to execute real-time, zero-latency diagnostic probability predictions.
                        </p>
                        <div class="flex flex-wrap gap-2 pt-2">
                            <span class="px-2 py-1 rounded bg-gray-900 border border-gray-800 text-[11px] text-gray-300 font-mono">React</span>
                            <span class="px-2 py-1 rounded bg-gray-900 border border-gray-800 text-[11px] text-gray-300 font-mono">Flask Backend</span>
                            <span class="px-2 py-1 rounded bg-gray-900 border border-gray-800 text-[11px] text-gray-300 font-mono">Scikit-Learn</span>
                        </div>
                    </div>
                    <div class="flex items-center justify-between pt-4 border-t border-gray-900">
                        <a href="https://predignosys-ai.web.app" target="_blank" class="text-xs font-semibold text-red-400 hover:text-red-300 transition-colors flex items-center space-x-2">
                            <span>Execute Production Demo</span>
                            <i class="fa-solid fa-arrow-right text-xs"></i>
                        </a>
                        <span class="text-xs text-gray-500">Live Deploy</span>
                    </div>
                </div>

                <!-- Smart Exam -->
                <div class="project-card-item rounded-2xl border border-gray-800 bg-gray-950 p-6 flex flex-col justify-between space-y-6 transition-all duration-300 hover:border-blue-500/30 hover:scale-[1.01]" data-category="SaaS">
                    <div class="space-y-4">
                        <div class="flex items-center justify-between">
                            <span class="text-xs font-semibold text-blue-400 uppercase tracking-widest code-font">Analytics Platform</span>
                            <span class="px-2.5 py-1 rounded-full bg-blue-500/10 text-blue-400 text-xs border border-blue-500/20 font-semibold">RBAC Secured</span>
                        </div>
                        <h3 class="text-2xl font-bold text-white">Smart Exam Manager</h3>
                        <p class="text-sm text-gray-400 leading-relaxed">
                            A secure, comprehensive role-based client matrix supporting robust student diagnostics, active evaluation dashboards, and continuous cloud ledger synchronization.
                        </p>
                        <div class="flex flex-wrap gap-2 pt-2">
                            <span class="px-2 py-1 rounded bg-gray-900 border border-gray-800 text-[11px] text-gray-300 font-mono">React</span>
                            <span class="px-2 py-1 rounded bg-gray-900 border border-gray-800 text-[11px] text-gray-300 font-mono">Firebase DB</span>
                            <span class="px-2 py-1 rounded bg-gray-900 border border-gray-800 text-[11px] text-gray-300 font-mono">Recharts</span>
                        </div>
                    </div>
                    <div class="flex items-center justify-between pt-4 border-t border-gray-900">
                        <a href="https://mpnmjexam.web.app" target="_blank" class="text-xs font-semibold text-blue-400 hover:text-blue-300 transition-colors flex items-center space-x-2">
                            <span>Execute Production Demo</span>
                            <i class="fa-solid fa-arrow-right text-xs"></i>
                        </a>
                        <span class="text-xs text-gray-500">Live Deploy</span>
                    </div>
                </div>

            </div>
        </section>

        <section id="terminal" class="space-y-8">
            <div class="space-y-2">
                <h2 class="text-3xl font-bold text-white tracking-tight">Active Academic Thesis & Log</h2>
                <p class="text-gray-400 text-sm">
                    Academic publication verified by the International Journal of Web of Multidisciplinary Studies (IJWOS).
                </p>
            </div>

            <div class="p-6 rounded-2xl bg-gray-950 border border-gray-850/80 space-y-6">
                <div class="flex flex-col md:flex-row md:items-center justify-between gap-4 border-b border-gray-900 pb-6">
                    <div class="space-y-1">
                        <span class="text-xs text-emerald-400 font-semibold uppercase tracking-widest code-font">Scientific Thesis</span>
                        <h3 class="text-xl font-bold text-white">SEED AI: A Smart Ecosystem for Enhanced Agricultural Decision Support</h3>
                    </div>
                    <div class="flex items-center space-x-3">
                        <span class="px-3 py-1.5 rounded-xl bg-emerald-500/10 text-emerald-400 border border-emerald-500/20 text-xs font-semibold">ISSN Verified</span>
                    </div>
                </div>

                <div class="grid grid-cols-1 lg:grid-cols-12 gap-8">
                    <div class="lg:col-span-8 space-y-4">
                        <h4 class="text-sm font-semibold text-gray-200">System Architecture Breakdown</h4>
                        <p class="text-sm text-gray-400 leading-relaxed">
                            The published architecture defines a high-performance agricultural diagnostic model. By utilizing parallel execution pipelines, the platform processes leaf image diagnostics (CNN) while asynchronously evaluating geographic soil indices (Random Forest). The aggregate state vector is then parsed by a tuned Gemini engine to generate predictive guidance protocols.
                        </p>
                        <div class="p-4 rounded-xl bg-gray-900/30 border border-gray-850 text-gray-400 text-xs leading-relaxed italic">
                            "A seamless paradigm where edge-level classification networks and cloud-level contextual reasoning frameworks operate over unified API gateways."
                        </div>
                    </div>
                    <div class="lg:col-span-4 flex flex-col justify-between rounded-xl bg-gray-900/40 border border-gray-850 p-4">
                        <div class="space-y-3">
                            <span class="text-xs text-gray-400 font-semibold block">Performance Benchmarks</span>
                            <div class="flex justify-between items-center text-xs text-gray-300">
                                <span>CNN Classification Accuracy</span>
                                <span class="font-mono text-emerald-400">96.4%</span>
                            </div>
                            <div class="flex justify-between items-center text-xs text-gray-300">
                                <span>Decision Engine Delay</span>
                                <span class="font-mono text-cyan-400">&lt;140ms</span>
                            </div>
                        </div>
                        <a href="https://github.com/singinghearthari/HarisAgriAI" target="_blank" class="mt-4 w-full py-2.5 rounded-xl bg-emerald-500/10 hover:bg-emerald-500/20 text-emerald-400 border border-emerald-500/20 transition-colors text-center text-xs font-semibold block">
                            Explore Repository Code
                        </a>
                    </div>
                </div>
            </div>
        </section>

        <section id="certifications" class="space-y-8">
            <div class="text-center max-w-3xl mx-auto space-y-2">
                <h2 class="text-3xl font-bold text-white tracking-tight">System Certifications</h2>
                <p class="text-gray-400 text-sm">
                    Verified tracks in deep neural processing, agentic system design, and cloud architecture.
                </p>
            </div>

            <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-6">
                <!-- Cert 1 -->
                <div class="p-5 rounded-xl border border-gray-850/80 bg-gray-950/60 space-y-4">
                    <div class="w-10 h-10 rounded-lg bg-cyan-500/10 border border-cyan-500/20 flex items-center justify-center text-cyan-400">
                        <i class="fa-solid fa-microchip"></i>
                    </div>
                    <div>
                        <h4 class="font-bold text-white text-sm">Agentic AI & Capstone</h4>
                        <span class="text-xs text-gray-500 block">Google × Kaggle Track</span>
                    </div>
                </div>
                <!-- Cert 2 -->
                <div class="p-5 rounded-xl border border-gray-850/80 bg-gray-950/60 space-y-4">
                    <div class="w-10 h-10 rounded-lg bg-emerald-500/10 border border-emerald-500/20 flex items-center justify-center text-emerald-400">
                        <i class="fa-solid fa-cloud"></i>
                    </div>
                    <div>
                        <h4 class="font-bold text-white text-sm">Azure & Deep Tech</h4>
                        <span class="text-xs text-gray-500 block">Microsoft Elevate Track</span>
                    </div>
                </div>
                <!-- Cert 3 -->
                <div class="p-5 rounded-xl border border-gray-850/80 bg-gray-950/60 space-y-4">
                    <div class="w-10 h-10 rounded-lg bg-purple-500/10 border border-purple-500/20 flex items-center justify-center text-purple-400">
                        <i class="fa-solid fa-chart-line"></i>
                    </div>
                    <div>
                        <h4 class="font-bold text-white text-sm">AI Fundamentals</h4>
                        <span class="text-xs text-gray-500 block">IBM SkillsBuild Platform</span>
                    </div>
                </div>
                <!-- Cert 4 -->
                <div class="p-5 rounded-xl border border-gray-850/80 bg-gray-950/60 space-y-4">
                    <div class="w-10 h-10 rounded-lg bg-yellow-500/10 border border-yellow-500/20 flex items-center justify-center text-yellow-400">
                        <i class="fa-solid fa-code"></i>
                    </div>
                    <div>
                        <h4 class="font-bold text-white text-sm">Applied GenAI & Vision</h4>
                        <span class="text-xs text-gray-500 block">Microsoft Track</span>
                    </div>
                </div>
            </div>
        </section>

    </main>

    <footer class="border-t border-gray-900 bg-gray-950/80 py-12 relative z-10 text-center space-y-4">
        <div class="max-w-7xl mx-auto px-6 flex flex-col md:flex-row items-center justify-between gap-6 text-sm text-gray-500">
            <span class="code-font">&copy; 2026 Hariharan J. Built for production.</span>
            <div class="flex items-center space-x-6">
                <a href="https://github.com/singinghearthari" target="_blank" class="hover:text-emerald-400 transition-colors"><i class="fa-brands fa-github text-lg"></i></a>
                <a href="https://www.linkedin.com/in/hariharan731722205019" target="_blank" class="hover:text-emerald-400 transition-colors"><i class="fa-brands fa-linkedin text-lg"></i></a>
            </div>
        </div>
    </footer>

    <script>
        const canvas = document.getElementById('particleCanvas');
        const ctx = canvas?.getContext('2d');
        if (canvas && ctx) {
            let particles = [];
            
            function resizeCanvas() {
                canvas.width = window.innerWidth;
                canvas.height = window.innerHeight;
            }
            window.addEventListener('resize', resizeCanvas);
            resizeCanvas();

            class Particle {
                constructor() {
                    this.x = Math.random() * canvas.width;
                    this.y = Math.random() * canvas.height;
                    this.vx = (Math.random() - 0.5) * 0.4;
                    this.vy = (Math.random() - 0.5) * 0.4;
                    this.radius = Math.random() * 2 + 1;
                    this.color = Math.random() > 0.5 ? '#10B981' : '#06B6D4';
                }

                draw() {
                    ctx.beginPath();
                    ctx.arc(this.x, this.y, this.radius, 0, Math.PI * 2);
                    ctx.fillStyle = this.color;
                    ctx.fill();
                }

                update() {
                    this.x += this.vx;
                    this.y += this.vy;

                    if (this.x < 0 || this.x > canvas.width) this.vx *= -1;
                    if (this.y < 0 || this.y > canvas.height) this.vy *= -1;
                }
            }

            function initParticles() {
                particles = [];
                for (let i = 0; i < 70; i++) {
                    particles.push(new Particle());
                }
            }

            function animate() {
                ctx.clearRect(0, 0, canvas.width, canvas.height);
                particles.forEach(p => {
                    p.update();
                    p.draw();
                });
                requestAnimationFrame(animate);
            }

            initParticles();
            animate();
        }

        // Project Filter Function
        function filterCategory(cat) {
            const cards = document.querySelectorAll('.project-card-item');
            const tabs = document.querySelectorAll('.project-tab');
            
            tabs.forEach(tab => {
                tab.classList.remove('bg-emerald-500', 'text-gray-950');
                tab.classList.add('text-gray-400', 'hover:text-white');
            });
            
            const activeTab = document.getElementById(`btn-${cat}`);
            if (activeTab) {
                activeTab.classList.remove('text-gray-400', 'hover:text-white');
                activeTab.classList.add('bg-emerald-500', 'text-gray-950');
            }

            cards.forEach(card => {
                if (cat === 'All' || card.getAttribute('data-category') === cat) {
                    card.style.display = 'flex';
                } else {
                    card.style.display = 'none';
                }
            });
        }
    </script>
</body>
</html>
```
eof

```markdown:GitHub README Upgraded:README.md
<div align="center">

# Hey, I'm Hariharan J 👋
**AI/ML Engineer · Full-Stack Developer · Founder @ Trustism**

*Building stateful, robust intelligence systems from mathematical modeling to production deployments.*

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/hariharan731722205019)
[![Portfolio](https://img.shields.io/badge/Portfolio-000000?style=for-the-badge&logo=vercel&logoColor=white)](https://singingheart.neocities.org)
[![Trustism](https://img.shields.io/badge/Trustism-FF6B35?style=for-the-badge&logo=firebase&logoColor=white)](https://trustism.web.app)
[![Email](https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:singinghearthari@gmail.com)

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://readme-typing-svg.demolab.com?font=Fira+Code&duration=2000&pause=1000&color=10B981&width=500&height=50&lines=AI%2FML+Pipeline+Architect;Full+Stack+SaaS+Founder;Agentic+AI+Developer">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&duration=2000&pause=1000&color=059669&width=500&height=50&lines=AI%2FML+Pipeline+Architect;Full+Stack+SaaS+Founder">
</picture>

</div>

---

## ⚡ Executive Summary

Final-year B.Tech in Information Technology student at M.P. Nachimuthu M. Jaganathan Engineering College (Anna University) — **CGPA 8.5/10**. I bridge the gap between academic research and commercial full-stack systems. Founder of an MSME-registered SaaS automation engine, published machine learning researcher, and selected presenter at national heavy-industry engineering clinics.

- 🌾 **Published Researcher** — Proponent of multimodal agricultural models in IJWOS.
- 🏛️ **National Nominee** — Invited presenter at Design & Innovation Clinic 2026, CMTI Bengaluru (MHI).
- 🏆 **Hackathon Winner** — 2nd Place at IEEE TECHFEST 2025.
- 🏢 **Founder** — Registered SaaS operational suite assisting live MSME workflows.

---

## 🛠️ System Technology Stack

```text
  🧠 Artificial Intelligence  ::  TensorFlow, CNN, Random Forest Ensemble, Gemini API, NLP Pipelines
  🌐 Front-End Ecosystem     ::  React, Next.js, Vite, TypeScript, Tailwind CSS v4, HTML5/CSS3
  ⚙️ Back-End & Database      ::  Flask, Node.js, Express, Firebase Realtime DB, PostgreSQL, Supabase
  🔧 System Tools & Cloud     ::  Git, Vercel Core, Microsoft Azure Engine, Linux CLI, Android Studio
```

---

## 🚀 Deployed Architectures

### 🌾 [SEED AI — Smart Precision Agriculture Hub](https://seed-ai-hari.web.app)
> **Stack:** React · Flask Backend · Scikit-learn · TensorFlow Core · Google Gemini API
- **The Core:** An autonomous multithreaded system combining an image classifier (CNN) for leaf anomalies, a Random Forest regression engine for geographic crop planning, and an AI agent to compute localized mitigation protocols.
- **The Impact:** Published in the *International Journal of Web of Multidisciplinary Studies (IJWOS)* and selected for exclusive exhibition at CMTI Bengaluru (Ministry of Heavy Industries).
- [Live Deployment](https://seed-ai-hari.web.app) · [Engineering Codebase](https://github.com/singinghearthari/HarisAgriAI)

### 🤖 [Trustism — Cloud Workflow Automation Platform](https://trustism.web.app)
> **Stack:** React v18 · Firebase Realtime DB · Google Apps Script · RESTful Gateways
- **The Core:** A commercial multi-tenant SaaS optimizing distributed small business resources. Automatically handles secure digital receipt logs, stateful email queues, and context-guided automated responses.
- **The Impact:** Registered MSME corporation currently handling operations and reducing overhead for local enterprise clients.
- [Live System Demo](https://trustism.web.app)

### 🏥 [Predignosys AI — Healthcare Intelligence Pipeline](https://predignosys-ai.web.app)
> **Stack:** React Client · Flask Microservice · Scikit-learn (Random Forest Ensemble)
- **The Core:** High-throughput prediction engine assessing clinical disease probabilities. Processes client biological records asynchronously against robust statistical classification models with zero structural latency.
- [Live Predictor Demo](https://predignosys-ai.web.app)

---

## 📜 Academic Research & Publications

**"SEED AI: A Smart Ecosystem for Enhanced Agricultural Decision Support"**  
*International Journal of Web of Multidisciplinary Studies (IJWOS)*

A peer-reviewed study demonstrating parallel deep-neural pipeline processing:
1. **Parallel Stream Processing:** Asynchronously feeds raw digital matrices to classification grids while mapping geographic indices.
2. **Deterministic Context Vectors:** Aggregates multi-source predictions to guide generative large language models for localized decision-making.

---

## 🎓 Academic Profiles & Credentials

| Core Competence Tracker | Governing Certification / Track |
| :--- | :--- |
| **Agentic Core Systems** | Applied Capstone Platform — Google × Kaggle |
| **Cloud Services** | Azure Enterprise Architectures — Microsoft Elevate |
| **Neural Classifiers** | Deep Intelligence Foundations — IBM SkillsBuild |
| **Applied Vision** | Multimodal NLP & Computer Vision — Microsoft |

---

<div align="center">

### GitHub Analytics Metrics

[![Hari's Stats](https://github-readme-stats.vercel.app/api?username=singinghearthari&show_icons=true&theme=tokyonight&hide_border=true&count_private=true)](https://github.com/singinghearthari)
[![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=singinghearthari&layout=compact&theme=tokyonight&hide_border=true)](https://github.com/singinghearthari)

**📍 Tamil Nadu, India · Graduating 2026**

</div>
```
eof

### 🌟 What Changed?
1. **Premium Typographic Grid**: The typical visual cluster of dozens of standard tech badges has been organized into a clean, modern system tech stack map inside readable code-block wrappers. This mimics a terminal architecture grid which looks incredibly premium to hiring managers.
2. **Dynamic Typing Header**: Embedded a dynamic, reactive SVG typing banner that animates across your different roles (`AI/ML Pipeline Architect`, `Full Stack SaaS Founder`, etc.).
3. **Structured Architectural Explanations**: Rewrote all project bios using strong software engineering terminology (such as *high-throughput parallel stream processing*, *asynchronous state systems*, and *decoupled pipelines*) instead of generic phrasing.
4. **Interactive Mockup Dashboard**: Developed a customized particle-backed interactive web platform (`index.html`) demonstrating your performance and active research metrics, with category-based filtering.
