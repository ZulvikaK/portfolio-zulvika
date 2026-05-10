<template>
  <div class="font-sans antialiased text-slate-100 selection:bg-emerald-500 selection:text-white overflow-x-hidden min-h-screen relative">
    
    <div class="fixed inset-0 z-0 overflow-hidden pointer-events-none">

      <!-- Base -->
      <div class="absolute inset-0 bg-[#020617]"></div>

      <!-- Galaxy Core (center glow) -->
      <div class="absolute top-[20%] left-[30%] w-[500px] h-[500px]
                  bg-gradient-radial from-purple-500/40 via-indigo-500/20 to-transparent
                  blur-[80px] opacity-80 animate-pulse-slow">
      </div>

      <!-- Emerald Galaxy -->
      <div class="absolute bottom-[10%] right-[20%] w-[600px] h-[600px]
                  bg-gradient-radial from-emerald-400/30 via-teal-500/20 to-transparent
                  blur-[90px] opacity-70 animate-float">
      </div>

      <!-- Blue Nebula -->
      <div class="absolute top-[0%] right-[0%] w-[500px] h-[500px]
                  bg-gradient-radial from-blue-500/30 via-cyan-500/20 to-transparent
                  blur-[80px] opacity-60 animate-pulse-slow">
      </div>

      <!-- Purple Accent -->
      <div class="absolute bottom-[0%] left-[0%] w-[400px] h-[400px]
                  bg-gradient-radial from-fuchsia-500/30 via-purple-500/20 to-transparent
                  blur-[70px] opacity-60 animate-float">
      </div>

      <!-- Noise -->
      <div class="absolute inset-0 opacity-[0.06] mix-blend-overlay"
           style="background-image: url('https://grainy-gradients.vercel.app/noise.svg');">
      </div>

    </div>

    <nav :class="['fixed top-4 left-4 right-4 md:left-10 md:right-10 rounded-2xl z-50 transition-all duration-500 border', scrolled ? 'bg-slate-900/60 backdrop-blur-xl border-white/10 shadow-lg shadow-emerald-900/20 py-3' : 'bg-transparent border-transparent py-5']">
      <div class="container mx-auto px-6 flex justify-between items-center">
        <a href="#" class="text-xl md:text-2xl font-bold tracking-tight group relative z-50 flex items-center gap-1">
          <div class="flex gap-1.5 mr-3 opacity-0 md:opacity-100 transition-opacity">
            <div class="w-3 h-3 rounded-full bg-red-500/80"></div>
            <div class="w-3 h-3 rounded-full bg-yellow-500/80"></div>
            <div class="w-3 h-3 rounded-full bg-emerald-500/80"></div>
          </div>
          <span class="text-white tracking-wide">ZKV</span>
          <span class="text-emerald-500 group-hover:text-emerald-400 transition-colors">.</span>
        </a>
        
        <div class="hidden md:flex items-center space-x-1">
          <a v-for="item in navLinks" :key="item.href" :href="item.href" 
             class="px-4 py-2 text-sm font-medium text-slate-300 hover:text-white transition-all duration-300 rounded-lg hover:bg-white/10 relative group overflow-hidden">
            {{ item.label }}
          </a>
        </div>

        <button @click="mobileMenuOpen = !mobileMenuOpen" class="md:hidden relative z-50 p-2 text-white focus:outline-none">
          <div class="w-6 h-5 relative flex flex-col justify-between">
            <span :class="['w-full h-0.5 bg-current rounded-full transition-all duration-300 origin-left', mobileMenuOpen ? 'rotate-45 translate-x-px' : '']"></span>
            <span :class="['w-full h-0.5 bg-current rounded-full transition-all duration-300', mobileMenuOpen ? 'opacity-0' : 'opacity-100']"></span>
            <span :class="['w-full h-0.5 bg-current rounded-full transition-all duration-300 origin-left', mobileMenuOpen ? '-rotate-45 translate-x-px' : '']"></span>
          </div>
        </button>

        <div :class="['fixed inset-0 bg-slate-900/95 backdrop-blur-3xl z-40 flex flex-col items-center justify-center space-y-8 transition-all duration-500 md:hidden', mobileMenuOpen ? 'opacity-100 visible' : 'opacity-0 invisible pointer-events-none']">
          <a v-for="item in navLinks" :key="item.href" :href="item.href" @click="mobileMenuOpen = false" class="text-2xl font-light text-white hover:text-emerald-500 transition-colors duration-300">
            {{ item.label }}
          </a>
        </div>
      </div>
    </nav>

    <main class="relative z-10">
      
      <section id="hero" class="relative w-full min-h-screen flex items-center overflow-hidden py-20">
        <div class="absolute top-[-10%] left-[-10%] w-[50%] h-[50%] bg-emerald-900/30 rounded-full blur-[120px] animate-pulse-slow"></div>
         <div class="absolute bottom-[-10%] right-[-10%] w-[50%] h-[50%] bg-teal-900/30 rounded-full blur-[120px] animate-pulse-slow delay-700"></div>

        <div class="container mx-auto px-4 md:px-12 relative z-10">
          <div class="grid md:grid-cols-2 gap-12 items-center">
            
            <div class="max-w-4xl relative z-20">
                <div class="inline-flex items-center space-x-2 px-4 py-1.5 bg-emerald-500/10 backdrop-blur-md border border-emerald-500/20 rounded-full text-emerald-300 text-xs font-semibold tracking-wider uppercase mb-8 shadow-lg shadow-emerald-500/10 animate-fade-in-up">
                  <span class="relative flex h-2 w-2">
                    <span class="animate-ping absolute inline-flex h-full w-full rounded-full bg-emerald-400 opacity-75"></span>
                    <span class="relative inline-flex rounded-full h-2 w-2 bg-emerald-500"></span>
                  </span>
                  <span>Project Manager @ Cekat.AI</span>
                </div>

                <h1 class="text-4xl md:text-7xl lg:text-8xl font-bold text-white tracking-tight mb-6 leading-tight animate-fade-in-up delay-100 drop-shadow-2xl">
                  Zulvika <br>
                  <span class="text-transparent bg-clip-text bg-gradient-to-r from-emerald-400 via-teal-300 to-cyan-200 drop-shadow-[0_0_25px_rgba(52,211,153,0.3)]">Kusumadevi</span>
                </h1>

                <p class="text-xl md:text-2xl text-slate-300 font-light mb-10 max-w-2xl leading-relaxed animate-fade-in-up delay-200">
                  Delivering 
                  <span class="text-emerald-500 font-mono font-bold text-3xl align-middle mx-1">{</span>
                  <span class="text-white font-medium">Structured Execution</span>
                  <span class="text-emerald-500 font-mono font-bold text-3xl align-middle mx-1">}</span>
                  in <br class="hidden md:block">
                  <span>
                    AI-Driven Innovation
                  </span>
                </p>

                <div class="flex flex-col sm:flex-row gap-4 animate-fade-in-up delay-300">
                  <a href="#projects" class="group relative px-8 py-4 bg-emerald-600/80 hover:bg-emerald-500 backdrop-blur-sm text-white font-semibold rounded-2xl shadow-[0_0_20px_rgba(16,185,129,0.3)] transition-all duration-300 transform hover:-translate-y-1 overflow-hidden text-center">
                    <span class="relative z-10">View Projects</span>
                    <div class="absolute inset-0 bg-gradient-to-r from-transparent via-white/20 to-transparent translate-x-[-100%] group-hover:translate-x-[100%] transition-transform duration-700"></div>
                  </a>
                  <a href="#contact" class="px-8 py-4 bg-white/5 border border-white/10 hover:border-emerald-500/50 backdrop-blur-md text-slate-300 hover:text-white font-semibold rounded-2xl transition-all duration-300 hover:bg-white/10 text-center shadow-lg">
                    Contact Me
                  </a>
                </div>

                <!-- Language Skills -->
                <div class="mt-10 animate-fade-in-up delay-300">
                  <h4 class="text-xs font-bold text-slate-500 uppercase tracking-[0.15em] mb-4 flex items-center gap-2">
                    <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4 text-emerald-500" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                      <path stroke-linecap="round" stroke-linejoin="round" d="M3 5h12M9 3v2m1.048 9.5A18.022 18.022 0 016.412 9m6.088 9h7M11 21l5-10 5 10M12.751 5C11.783 10.77 8.07 15.61 3 18.129" />
                    </svg>
                    Language Skills
                  </h4>
                  <div class="flex flex-wrap gap-3">
                    <div v-for="lang in languages" :key="lang.name" class="group/lang flex items-center gap-3 px-4 py-2.5 bg-white/5 backdrop-blur-md border border-white/10 rounded-xl hover:border-emerald-500/30 transition-all duration-300 cursor-default">
                      <span class="text-lg">{{ lang.flag }}</span>
                      <div class="flex flex-col">
                        <span class="text-sm font-semibold text-white leading-tight">{{ lang.name }}</span>
                        <span :class="['text-[10px] font-bold uppercase tracking-wider leading-tight', lang.level === 'Native Speaker' ? 'text-emerald-400' : 'text-teal-300/70']">{{ lang.level }}</span>
                      </div>
                      <div class="flex gap-0.5 ml-1">
                        <div v-for="n in 5" :key="n" :class="['w-1.5 h-4 rounded-full transition-all duration-500', n <= lang.dots ? 'bg-emerald-500 shadow-[0_0_6px_rgba(16,185,129,0.6)] group-hover/lang:shadow-[0_0_10px_rgba(16,185,129,0.8)]' : 'bg-white/10']"></div>
                      </div>
                    </div>
                  </div>
                </div>
            </div>

            <div class="hidden md:block relative h-[600px] w-full animate-fade-in-up delay-500 perspective-1000">
                
                <div class="absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 w-[80%] h-[80%] bg-gradient-to-tr from-emerald-600/30 via-teal-500/30 to-cyan-400/30 rounded-full blur-[100px] animate-pulse-slow mix-blend-screen"></div>

                <div class="relative h-full w-full animate-float-slow transform-style-3d">
                    
                    <div class="absolute top-10 right-10 w-64 h-80 bg-white/5 backdrop-blur-2xl border border-white/20 rounded-[3rem] shadow-2xl shadow-emerald-900/30 transform rotate-6 hover:rotate-0 transition-all duration-700 z-20 p-8 flex flex-col justify-between overflow-hidden">
                        <div class="absolute top-0 left-0 w-full h-full bg-gradient-to-br from-white/10 to-transparent opacity-50 pointer-events-none"></div>
                        <div class="w-16 h-16 bg-gradient-to-br from-emerald-400 to-cyan-300 rounded-2xl flex items-center justify-center shadow-lg shadow-emerald-500/20">
                             <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8 text-white" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                                <path stroke-linecap="round" stroke-linejoin="round" d="M9 3v2m6-2v2M9 19v2m6-2v2M5 9H3m2 6H3m18-6h-2m2 6h-2M7 19h10a2 2 0 002-2V7a2 2 0 00-2-2H7a2 2 0 00-2 2v10a2 2 0 002 2zM9 9h6v6H9V9z" />
                            </svg>
                        </div>
                        <div class="absolute bottom-0 right-0 opacity-30">
                            <svg width="120" height="120" viewBox="0 0 120 120" fill="none" xmlns="http://www.w3.org/2000/svg">
                                <path d="M10 110 C 30 80, 90 80, 110 10" stroke="url(#paint0_linear)" stroke-width="2" stroke-linecap="round"/>
                                <path d="M0 90 C 40 60, 80 60, 120 30" stroke="url(#paint0_linear)" stroke-width="2" stroke-linecap="round" opacity="0.6"/>
                                <defs>
                                    <linearGradient id="paint0_linear" x1="0" y1="0" x2="120" y2="120" gradientUnits="userSpaceOnUse">
                                        <stop stop-color="#34D399"/>
                                        <stop offset="1" stop-color="#22D3EE"/>
                                    </linearGradient>
                                </defs>
                            </svg>
                        </div>
                        <div>
                             <h4 class="text-white font-bold text-xl">AI Architect</h4>
                             <p class="text-emerald-200/70 text-sm">Workflow Design</p>
                        </div>
                    </div>

                    <div class="absolute bottom-20 left-0 w-72 h-64 bg-white/5 backdrop-blur-xl border border-white/10 rounded-[2.5rem] shadow-xl shadow-teal-900/20 transform -rotate-3 hover:rotate-0 transition-all duration-700 z-10 p-6 flex flex-col justify-between">
                        <div class="w-12 h-12 bg-gradient-to-br from-teal-400 to-emerald-500 rounded-xl flex items-center justify-center shadow-lg shadow-teal-500/20">
                             <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-white" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                                <path stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4" />
                            </svg>
                        </div>
                         <div>
                             <h4 class="text-white font-bold text-lg">Structured Execution</h4>
                             <p class="text-teal-200/70 text-sm">Agile Delivery</p>
                        </div>
                    </div>

                    <div class="absolute top-1/3 left-1/4 w-10 h-10 bg-cyan-500/30 backdrop-blur-md rounded-full border border-cyan-400/50 animate-pulse-slow z-30 flex items-center justify-center">
                        <div class="w-3 h-3 bg-cyan-300 rounded-full shadow-[0_0_15px_rgba(34,211,238,0.8)]"></div>
                    </div>
                </div>

            </div> </div>
        </div>
      </section>

      <section id="about" class="relative py-32">
        <div class="container mx-auto px-6 max-w-6xl relative z-10">
          <div class="bg-slate-900/40 backdrop-blur-xl border border-white/10 rounded-[2.5rem] p-8 md:p-16 shadow-2xl reveal">
              <div class="grid lg:grid-cols-2 gap-16 items-start">
                <div>
                  <h2 class="text-emerald-400 font-bold tracking-widest uppercase text-xs mb-4">About Me</h2>
                  <h3 class="text-4xl md:text-5xl font-bold text-white leading-tight mb-6">
                    Architecting <br>
                    <span class="text-transparent bg-clip-text bg-gradient-to-r from-emerald-400 to-teal-200">Reliable AI</span> Systems <br>
                    for Real-World Impact.
                  </h3>
                  <div class="h-1 w-20 bg-gradient-to-r from-emerald-500 to-transparent rounded-full"></div>
                </div>
                
                <div class="space-y-6 text-slate-300 text-lg leading-relaxed font-light">
                  <p>
                    As a <strong class="text-white">Project Manager at Cekat.AI</strong>, I bridge the gap between complex AI capabilities and strategic business goals. My expertise lies not just in managing timelines, but in <strong class="text-emerald-400">navigating the uncertainty</strong> of AI development.
                  </p>
                  <p>
                    Leveraging a strong foundation in <strong class="text-white">Quality Assurance & Automation</strong>, I bring a unique precision to project execution. I ensure that every innovation we build is not only powerful but also stable, scalable, and ready for deployment.
                  </p>
                  
                  <div class="pt-6">
                    <h4 class="font-bold text-white mb-4 text-sm uppercase tracking-wide opacity-80">Core Competencies</h4>
                    <div class="flex flex-wrap gap-2">
                        <span v-for="skill in skills" :key="skill" class="px-4 py-1.5 bg-white/5 border border-white/10 hover:border-emerald-500/30 text-slate-300 hover:text-emerald-300 text-sm rounded-full transition-colors cursor-default backdrop-blur-sm">
                            {{ skill }}
                        </span>
                    </div>
                  </div>
                </div>
              </div>
          </div>
        </div>
      </section>

      <section class="py-10">
        <div class="container mx-auto px-6 max-w-6xl">
          <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-6 stats-container">
            <div v-for="(stat, index) in stats" :key="stat.label" class="bg-white/5 backdrop-blur-md border border-white/5 rounded-3xl p-6 text-center group hover:bg-white/10 transition-all duration-300 reveal" :style="{ transitionDelay: `${index * 100}ms` }">
              <div class="mb-2 flex justify-center items-end">
                <span class="text-4xl md:text-5xl font-black text-white tracking-tighter group-hover:text-emerald-400 transition-colors duration-300 drop-shadow-md">
                    {{ displayStats[index] }}
                </span>
                <span class="text-xl md:text-2xl font-bold text-emerald-500 mb-1 md:mb-2 ml-0.5">{{ stat.symbol }}</span>
              </div>
              <p class="text-slate-400 font-medium text-xs md:text-sm tracking-wide uppercase">{{ stat.label }}</p>
            </div>
          </div>
        </div>
      </section>

      <section id="experience" class="py-32 relative overflow-hidden">
        <!-- Background Ambient Glow -->
        <div class="absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 w-[800px] h-[800px] bg-emerald-900/10 rounded-full blur-[120px] pointer-events-none"></div>

        <div class="container mx-auto px-6 max-w-5xl relative z-10">
          <div class="text-center mb-20 relative">
            <h2 class="text-xs font-bold tracking-[0.2em] text-emerald-500 uppercase mb-4">The Journey</h2>
            <h3 class="text-5xl md:text-6xl font-bold text-white tracking-tight">
              Career <span class="text-transparent bg-clip-text bg-gradient-to-r from-emerald-400 to-teal-300">Milestones</span>
            </h3>
          </div>

          <div class="relative">
             <!-- Vertical Timeline Line -->
             <div class="absolute left-6 md:left-1/2 top-0 bottom-0 w-px bg-gradient-to-b from-transparent via-emerald-500/30 to-transparent md:transform md:-translate-x-1/2"></div>
            
            <div class="space-y-16">
              <div v-for="(job, index) in experience" :key="index" :class="['relative flex items-start md:items-center w-full group perspective-1000 reveal', index % 2 === 0 ? 'md:flex-row' : 'md:flex-row-reverse']">
                
                <!-- Content Block -->
                <div :class="['w-full md:w-1/2 pl-16 md:pl-0 relative z-10', index % 2 === 0 ? 'md:pr-16 md:text-right' : 'md:pl-16 md:text-left']">
                    <div class="group-hover:-translate-y-1 transition-transform duration-500 ease-out">
                        <span class="inline-block text-sm font-mono text-emerald-400/80 mb-2 tracking-wide">{{ job.period }}</span>
                        <h4 class="text-2xl md:text-3xl font-bold text-white mb-1 group-hover:text-emerald-300 transition-colors duration-300">{{ job.title }}</h4>
                        <div class="text-base md:text-lg font-medium text-slate-300">{{ job.company }}</div>
                        <div class="text-xs md:text-sm text-slate-500 uppercase tracking-widest mb-4">{{ job.location }}</div>
                        <p :class="['text-slate-400 leading-relaxed font-light text-sm md:text-base md:max-w-md', index % 2 === 0 ? 'md:ml-auto' : '']">
                            {{ job.description }}
                        </p>
                    </div>
                </div>

                <!-- Central Timeline Node -->
                <div class="absolute left-6 md:relative md:left-0 transform -translate-x-1/2 md:translate-x-0 flex items-center justify-center z-20 md:mx-0">
                    <!-- Glowing Dot -->
                    <div :class="['w-4 h-4 rounded-full border-2 transition-all duration-500 z-30 relative', job.current ? 'bg-emerald-500 border-emerald-400 shadow-[0_0_15px_rgba(16,185,129,0.8)] scale-110' : 'bg-[#020617] border-slate-600 group-hover:border-emerald-500 group-hover:bg-emerald-500/20 group-hover:shadow-[0_0_15px_rgba(16,185,129,0.4)]']"></div>
                    <!-- Ripple Effect on Hover -->
                    <div class="absolute w-12 h-12 rounded-full border border-emerald-500/20 opacity-0 scale-50 group-hover:opacity-100 group-hover:scale-100 transition-all duration-700 ease-out"></div>
                </div>

                <!-- Spacer for Desktop (maintains 50% width on other side) -->
                <div class="hidden md:block md:w-1/2"></div>

              </div>
            </div>
          </div>
        </div>
      </section>

      <!-- Education Section -->
      <section id="education" class="py-24 relative overflow-hidden">
        <div class="absolute top-1/2 right-0 w-[600px] h-[600px] bg-teal-900/10 rounded-full blur-[120px] pointer-events-none"></div>

        <div class="container mx-auto px-6 max-w-5xl relative z-10">
          <div class="text-center mb-16 reveal">
            <h2 class="text-xs font-bold tracking-[0.2em] text-emerald-500 uppercase mb-4">Background</h2>
            <h3 class="text-4xl md:text-5xl font-bold text-white tracking-tight">
              Education <span class="text-transparent bg-clip-text bg-gradient-to-r from-emerald-400 to-teal-300">&amp; Degree</span>
            </h3>
          </div>

          <div class="grid gap-6 max-w-3xl mx-auto">
            <div v-for="(edu, index) in education" :key="index" class="group bg-white/5 backdrop-blur-xl border border-white/10 rounded-[2rem] p-8 md:p-10 hover:border-emerald-500/30 hover:bg-white/[0.08] transition-all duration-500 reveal relative overflow-hidden" :style="{ transitionDelay: `${index * 150}ms` }">
              
              <!-- Subtle corner glow on hover -->
              <div class="absolute -top-10 -right-10 w-40 h-40 bg-emerald-500/10 rounded-full blur-[60px] opacity-0 group-hover:opacity-100 transition-opacity duration-700 pointer-events-none"></div>

              <div class="flex items-start gap-5 md:gap-8 relative z-10">
                <!-- Icon -->
                <div class="shrink-0 w-14 h-14 md:w-16 md:h-16 rounded-2xl bg-gradient-to-br from-emerald-500/20 to-teal-500/20 border border-emerald-500/20 flex items-center justify-center group-hover:shadow-[0_0_25px_rgba(16,185,129,0.3)] transition-all duration-500">
                  <svg v-if="edu.icon === 'academic'" xmlns="http://www.w3.org/2000/svg" class="h-7 w-7 md:h-8 md:w-8 text-emerald-400" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5">
                    <path d="M4.26 10.147a60.438 60.438 0 0 0-.491 6.347A48.62 48.62 0 0 1 12 20.904a48.62 48.62 0 0 1 8.232-4.41 60.46 60.46 0 0 0-.491-6.347m-15.482 0a50.636 50.636 0 0 0-2.658-.813A59.906 59.906 0 0 1 12 3.493a59.903 59.903 0 0 1 10.399 5.84c-.896.248-1.783.52-2.658.814m-15.482 0A50.717 50.717 0 0 1 12 13.489a50.702 50.702 0 0 1 7.74-3.342M6.75 15a.75.75 0 1 0 0-1.5.75.75 0 0 0 0 1.5Zm0 0v-3.675A55.378 55.378 0 0 1 12 8.443m-7.007 11.55A5.981 5.981 0 0 0 6.75 15.75v-1.5" stroke-linecap="round" stroke-linejoin="round"/>
                  </svg>
                  <svg v-else xmlns="http://www.w3.org/2000/svg" class="h-7 w-7 md:h-8 md:w-8 text-teal-400" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5">
                    <path stroke-linecap="round" stroke-linejoin="round" d="M12 6.042A8.967 8.967 0 0 0 6 3.75c-1.052 0-2.062.18-3 .512v14.25A8.987 8.987 0 0 1 6 18c2.305 0 4.408.867 6 2.292m0-14.25a8.966 8.966 0 0 1 6-2.292c1.052 0 2.062.18 3 .512v14.25A8.987 8.987 0 0 0 18 18a8.967 8.967 0 0 0-6 2.292m0-14.25v14.25" />
                  </svg>
                </div>

                <!-- Content -->
                <div class="flex-1 min-w-0">
                  <div class="flex flex-col sm:flex-row sm:items-center sm:justify-between gap-1 mb-2">
                    <h4 class="text-xl md:text-2xl font-bold text-white group-hover:text-emerald-300 transition-colors duration-300">{{ edu.institution }}</h4>
                    <span class="text-sm font-mono text-emerald-400/70 tracking-wide shrink-0">{{ edu.period }}</span>
                  </div>
                  <p v-if="edu.degree" class="text-slate-300 text-sm md:text-base font-light leading-relaxed mb-3">{{ edu.degree }}</p>
                  <p v-if="edu.field" class="text-slate-500 text-xs md:text-sm font-light italic">{{ edu.field }}</p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>

      <section id="projects" class="py-32 relative">
        <div class="container mx-auto px-6 max-w-7xl">
          <div class="text-center mb-20">
            <h2 class="text-emerald-400 font-bold tracking-widest uppercase text-xs mb-4">Portfolio</h2>
            <h3 class="text-4xl md:text-5xl font-bold text-white">
              Selected <span class="text-emerald-500">Works</span>
            </h3>
          </div>

          <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
            <div v-for="(project, index) in projects" :key="index" @click="selectedProject = project" class="group bg-white/5 backdrop-blur-lg rounded-[2rem] overflow-hidden cursor-pointer border border-white/10 hover:border-emerald-500/30 hover:bg-white/10 transition-all duration-500 ease-out hover:shadow-[0_0_30px_rgba(16,185,129,0.15)] reveal" :style="{ transitionDelay: `${index * 150}ms` }">
              
              <!-- Custom Image Thumbnail -->
              <div v-if="project.image" class="h-56 w-full overflow-hidden relative group">
                  <img :src="project.image" 
                       :alt="project.title" 
                       class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-110"
                       style="filter: grayscale(100%) sepia(100%) hue-rotate(130deg) saturate(200%) brightness(0.7) contrast(1.1);">
                  
                  <div class="absolute inset-0 bg-gradient-to-t from-slate-900 via-slate-900/20 to-transparent opacity-90"></div>
                  
                  <div class="absolute top-5 left-5 z-10">
                    <span class="px-3 py-1 bg-black/40 backdrop-blur-md border border-white/20 text-[10px] font-bold text-white rounded-full uppercase tracking-wider">
                        {{ project.category }}
                    </span>
                 </div>
              </div>

              <!-- Default Gradient Thumbnail -->
              <div v-else class="h-56 overflow-hidden relative bg-slate-800">
                <div class="absolute inset-0 bg-slate-800 transition-transform duration-700 group-hover:scale-110"></div>
                <div class="absolute inset-0 bg-gradient-to-t from-slate-900 via-transparent to-transparent opacity-90"></div>
                
                <div class="absolute top-5 left-5">
                    <span class="px-3 py-1 bg-black/40 backdrop-blur-md border border-white/20 text-[10px] font-bold text-white rounded-full uppercase tracking-wider">
                        {{ project.category }}
                    </span>
                </div>
              </div>
              
              <div class="p-8">
                <h4 class="text-2xl font-bold text-white mb-3 group-hover:text-emerald-400 transition-colors">{{ project.title }}</h4>
                <p class="text-slate-400 leading-relaxed mb-6 text-sm font-light">{{ project.description }}</p>
                <div class="flex flex-wrap gap-2">
                    <span v-for="tag in project.tags" :key="tag" class="text-xs font-medium text-slate-300 bg-white/5 border border-white/5 px-3 py-1 rounded-full group-hover:border-emerald-500/30 group-hover:text-emerald-100 transition-colors">
                        {{ tag }}
                    </span>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>

      <section id="stack" class="py-24 relative overflow-x-hidden border-t border-b border-white/10 bg-[radial-gradient(circle_at_center,_var(--tw-gradient-stops))] from-indigo-950/30 via-slate-900 to-slate-950">
        <div class="container mx-auto px-6 max-w-6xl relative z-10 reveal">
          <div class="grid md:grid-cols-2 gap-16 md:gap-32 items-start">
            
            <!-- Methodology Column -->
            <div class="space-y-10">
              <div class="space-y-4">
                <h3 class="text-2xl md:text-3xl font-bold text-white tracking-tight">Methodology</h3>
                <p class="text-slate-400 text-sm leading-relaxed font-light max-w-md">
                  Proven frameworks to ensure structured project delivery, effective stakeholder collaboration, and proactive risk management.
                </p>
              </div>

              <div class="flex flex-wrap gap-3">
                <span v-for="item in methodology" :key="item" class="px-5 py-2 bg-transparent border border-white/30 text-white text-sm font-medium rounded-full hover:bg-white/10 transition-all cursor-default">
                  {{ item }}
                </span>
              </div>
            </div>

            <!-- Tools Stack Column -->
            <div class="space-y-10">
              <div class="space-y-4">
                <h3 class="text-2xl md:text-3xl font-bold text-white tracking-tight">Tools Stack</h3>
                <p class="text-slate-400 text-sm leading-relaxed font-light max-w-md">
                  Leveraging a high-performance stack to build, automate, and monitor complex AI-driven systems with precision.
                </p>
              </div>

              <div class="flex flex-wrap gap-3">
                <span v-for="item in toolsStack" :key="item" class="px-5 py-2 bg-transparent border border-white/30 text-white text-sm font-medium rounded-full hover:bg-white/10 transition-all cursor-default">
                  {{ item }}
                </span>
              </div>
            </div>

          </div>
        </div>
      </section>

      <section id="contact" class="relative py-32 overflow-hidden">
        <div class="container mx-auto px-6 max-w-4xl relative z-10">
          <div class="text-center mb-16">
            <span class="text-emerald-500 font-bold tracking-widest uppercase text-xs mb-4 block">Get In Touch</span>
            <h2 class="text-4xl md:text-5xl font-bold text-white leading-tight">
              Let's Build Impactful <br>
              <span class="text-transparent bg-clip-text bg-gradient-to-r from-emerald-400 to-teal-200">AI Projects Together</span>
            </h2>
          </div>

          <form @submit.prevent="sendEmail" class="bg-slate-800/40 backdrop-blur-2xl border border-white/10 rounded-[2.5rem] p-8 md:p-12 shadow-2xl relative overflow-hidden reveal">
            <div class="absolute -top-20 -right-20 w-64 h-64 bg-emerald-500/20 rounded-full blur-[80px] pointer-events-none"></div>

            <div class="grid md:grid-cols-2 gap-8 mb-8 relative z-10">
                <div class="space-y-2">
                    <label class="text-xs font-bold text-slate-400 ml-1 uppercase tracking-wide">Name</label>
                    <input v-model="form.name" type="text" required class="w-full bg-black/20 border border-white/10 rounded-2xl px-5 py-4 text-white placeholder-slate-600 focus:outline-none focus:border-emerald-500/50 focus:bg-black/40 transition-all duration-300" placeholder="John Doe">
                </div>
                <div class="space-y-2">
                    <label class="text-xs font-bold text-slate-400 ml-1 uppercase tracking-wide">Email</label>
                    <input v-model="form.email" type="email" required class="w-full bg-black/20 border border-white/10 rounded-2xl px-5 py-4 text-white placeholder-slate-600 focus:outline-none focus:border-emerald-500/50 focus:bg-black/40 transition-all duration-300" placeholder="john@example.com">
                </div>
            </div>
            <div class="space-y-2 mb-8 relative z-10">
                <label class="text-xs font-bold text-slate-400 ml-1 uppercase tracking-wide">Message</label>
                <textarea v-model="form.message" rows="5" required class="w-full bg-black/20 border border-white/10 rounded-2xl px-5 py-4 text-white placeholder-slate-600 focus:outline-none focus:border-emerald-500/50 focus:bg-black/40 transition-all duration-300 resize-none" placeholder="Tell me about your project context..."></textarea>
            </div>
            <button type="submit" :disabled="isLoading" class="w-full relative z-10 bg-gradient-to-r from-emerald-600 to-teal-500 hover:from-emerald-500 hover:to-teal-400 text-white font-bold py-5 rounded-2xl shadow-lg shadow-emerald-900/40 transform transition-all duration-300 hover:-translate-y-1 hover:shadow-emerald-500/20 disabled:opacity-50 disabled:cursor-not-allowed">
                {{ isLoading ? 'Sending...' : 'Send Message' }}
            </button>
          </form>
        </div>
      </section>
    </main>

    <!-- Project Detail Modal -->
    <Transition
        enter-active-class="transition duration-300 ease-out"
        enter-from-class="opacity-0"
        enter-to-class="opacity-100"
        leave-active-class="transition duration-200 ease-in"
        leave-from-class="opacity-100"
        leave-to-class="opacity-0"
    >
        <div v-if="selectedProject" class="fixed inset-0 z-[100] flex items-center justify-center p-4 md:p-8" @click.self="selectedProject = null">
            
            <!-- Backdrop -->
            <div class="absolute inset-0 bg-slate-900/80 backdrop-blur-xl"></div>

            <!-- Modal Content -->
            <div class="relative w-full max-w-5xl max-h-[90vh] bg-slate-800/60 backdrop-blur-2xl border border-white/10 rounded-3xl shadow-2xl overflow-y-auto custom-scrollbar flex flex-col animate-scale-up">
                
                <!-- Close Button -->
                <button @click="selectedProject = null" class="absolute top-6 right-6 p-2 rounded-full bg-white/5 hover:bg-white/10 border border-white/5 hover:border-white/20 transition-all z-50 group">
                    <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-slate-400 group-hover:text-white transition-colors" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                        <path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12" />
                    </svg>
                </button>

                <!-- Header Image/Banner (Optional) -->
                <div class="h-48 md:h-64 bg-slate-900 relative overflow-hidden shrink-0 group">
                    
                    <img v-if="selectedProject.image" 
                         :src="selectedProject.image" 
                         :alt="selectedProject.title" 
                         class="w-full h-full object-cover absolute inset-0 transition-transform duration-1000 group-hover:scale-105"
                         style="filter: grayscale(100%) sepia(100%) hue-rotate(130deg) saturate(200%) brightness(0.6) contrast(1.1);">

                    <div class="absolute inset-0 bg-gradient-to-t from-slate-900 via-slate-900/50 to-transparent z-10"></div>
                    
                    <div class="absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 w-[800px] h-[800px] bg-emerald-500/20 rounded-full blur-[100px] animate-pulse-slow z-0"></div>

                    <div class="absolute bottom-10 left-8 md:left-12 z-20">
                        <span class="inline-block px-3 py-1 bg-emerald-500/20 border border-emerald-500/30 text-emerald-300 text-xs font-bold rounded-full uppercase tracking-wider mb-3 backdrop-blur-md shadow-lg">
                            {{ selectedProject.category }}
                        </span>
                        <h2 class="text-3xl md:text-5xl font-bold text-white tracking-tight drop-shadow-2xl">{{ selectedProject.title }}</h2>
                    </div>
                </div>

                <!-- Body -->
                <div class="p-8 md:p-12 space-y-10">
                    
                    <!-- Overview & Description -->
                    <div class="space-y-6">
                        <p v-if="selectedProject.details?.overview" class="text-xl md:text-2xl text-slate-300 font-serif italic leading-relaxed border-l-4 border-emerald-500/50 pl-6">
                            "{{ selectedProject.details.overview }}"
                        </p>
                        <p class="text-slate-400 leading-loose text-base md:text-lg">
                            {{ selectedProject.details?.fullDescription || selectedProject.description }}
                        </p>
                    </div>

                    <!-- Features Grid -->
                    <div v-if="selectedProject.details?.features" class="grid md:grid-cols-2 gap-6">
                        <div v-for="feature in selectedProject.details.features" :key="feature.title" class="bg-white/5 border border-white/5 rounded-2xl p-6 hover:bg-white/10 transition-colors group">
                            <div class="flex items-start gap-4">
                                <div class="p-3 rounded-xl bg-gradient-to-br from-emerald-500/20 to-teal-500/20 text-emerald-400 shrink-0">
                                    <!-- Dynamic Icon Placeholder Logic based on Feature Title keywords -->
                                    <svg v-if="feature.icon === 'ChatBubbleBottomCenterTextIcon'" xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5">
                                        <path stroke-linecap="round" stroke-linejoin="round" d="M8 12h.01M12 12h.01M16 12h.01M21 12c0 4.418-4.03 8-9 8a9.863 9.863 0 01-4.255-.949L3 20l1.395-3.72C3.512 15.042 3 13.574 3 12c0-4.418 4.03-8 9-8s9 3.582 9 8z" />
                                    </svg>
                                    <svg v-else-if="feature.icon === 'ShieldCheckIcon'" xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5">
                                        <path stroke-linecap="round" stroke-linejoin="round" d="M9 12l2 2 4-4m5.618-4.016A11.955 11.955 0 0112 2.944a11.955 11.955 0 01-8.618 3.04A12.02 12.02 0 003 9c0 5.591 3.824 10.29 9 11.622 5.176-1.332 9-6.03 9-11.622 0-1.042-.133-2.052-.382-3.016z" />
                                    </svg>
                                    <svg v-else-if="feature.icon === 'CircleStackIcon'" xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5">
                                        <path stroke-linecap="round" stroke-linejoin="round" d="M20.25 6.375c0 2.278-3.694 4.125-8.25 4.125S3.75 8.653 3.75 6.375m16.5 0c0-2.278-3.694-4.125-8.25-4.125S3.75 4.097 3.75 6.375m16.5 0v11.25c0 2.278-3.694 4.125-8.25 4.125s-8.25-1.847-8.25-4.125V6.375m16.5 0v3.75m-16.5-3.75v3.75m16.5 0v3.75C20.25 16.153 16.556 18 12 18s-8.25-1.847-8.25-4.125v-3.75m16.5 0c0 2.278-3.694 4.125-8.25 4.125s-8.25-1.847-8.25-4.125" />
                                    </svg>
                                    <svg v-else-if="feature.icon === 'BanknotesIcon'" xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5">
                                        <path stroke-linecap="round" stroke-linejoin="round" d="M12 6v12m-3-2.818l.879.659c1.171.879 3.07.879 4.242 0 1.172-.879 1.172-2.303 0-3.182C13.536 12.219 12.768 12 12 12c-.725 0-1.45-.22-2.003-.659-1.106-.879-1.106-2.303 0-3.182s2.9-.879 4.006 0l.415.33M21 12a9 9 0 11-18 0 9 9 0 0118 0z" />
                                    </svg>
                                     <svg v-else-if="feature.icon === 'ClockIcon'" xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5">
                                        <path stroke-linecap="round" stroke-linejoin="round" d="M12 6v6h4.5m4.5 0a9 9 0 11-18 0 9 9 0 0118 0z" />
                                    </svg>
                                    <svg v-else-if="feature.icon === 'UserGroupIcon'" xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5">
                                        <path stroke-linecap="round" stroke-linejoin="round" d="M17 20h5v-2a3 3 0 00-5.356-1.857M17 20H7m10 0v-2c0-.656-.126-1.283-.356-1.857M7 20H2v-2a3 3 0 015.356-1.857M7 20v-2c0-.656.126-1.283.356-1.857m0 0a5.002 5.002 0 019.288 0M15 7a3 3 0 11-6 0 3 3 0 016 0zm6 3a2 2 0 11-4 0 2 2 0 014 0zM7 10a2 2 0 11-4 0 2 2 0 014 0z" />
                                    </svg>
                                    <svg v-else xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5">
                                        <path stroke-linecap="round" stroke-linejoin="round" d="M13 10V3L4 14h7v7l9-11h-7z" />
                                    </svg>
                                </div>
                                <div>
                                    <h4 class="text-white font-bold mb-1">{{ feature.title }}</h4>
                                    <p class="text-slate-400 text-sm leading-relaxed">{{ feature.desc }}</p>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Footer -->
                <div class="p-8 border-t border-white/5 flex gap-4 bg-black/20 backdrop-blur-md sticky bottom-0">
                    <a v-if="selectedProject.link" :href="selectedProject.link" target="_blank" class="flex-1 bg-emerald-600 hover:bg-emerald-500 text-white font-bold py-4 rounded-xl text-center transition-colors shadow-lg shadow-emerald-900/40 transform hover:-translate-y-0.5">
                        Read Case Study
                    </a>
                </div>
            </div>
        </div>
    </Transition>

    <footer class="bg-black/20 backdrop-blur-md border-t border-white/5 text-slate-500 py-12 relative z-10">
        <div class="container mx-auto px-6 text-center">
            
            <div class="mb-8 animate-fade-in-up">
                <a href="#hero" class="inline-block transition-transform duration-300 hover:scale-110 group cursor-pointer">
                    <span class="text-3xl font-bold tracking-tight text-white transition-colors duration-300">
                        Zulvika<span class="text-emerald-500 drop-shadow-[0_0_10px_rgba(52,211,153,0.8)]">.</span>
                    </span>
                </a>
                <p class="text-sm text-slate-300 font-light max-w-md mx-auto leading-relaxed mt-4">Delivering Structured Execution in AI-Driven Innovation.</p>
            </div>

            <div class="flex justify-center items-center space-x-4 mb-10 animate-fade-in-up delay-100">
                
                <a href="https://www.linkedin.com/in/zulvika-kusumadevi/" target="_blank" aria-label="LinkedIn" class="group">
                    <div class="w-12 h-12 rounded-full bg-white/5 border border-white/10 flex items-center justify-center text-slate-400 transition-all duration-300 group-hover:border-emerald-500 group-hover:text-emerald-500 group-hover:shadow-[0_0_20px_rgba(16,185,129,0.5)]">
                        <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="currentColor" viewBox="0 0 24 24">
                            <path d="M4.98 3.5c0 1.381-1.11 2.5-2.48 2.5s-2.48-1.119-2.48-2.5c0-1.38 1.11-2.5 2.48-2.5s2.48 1.12 2.48 2.5zm.02 4.5h-5v16h5v-16zm7.982 0h-4.968v16h4.969v-8.399c0-4.67 6.029-5.052 6.029 0v8.399h4.988v-10.131c0-7.88-8.922-7.593-11.018-3.714v-2.155z"/>
                        </svg>
                    </div>
                </a>

                <a href="mailto:zulvika.devi@gmail.com" aria-label="Email" class="group">
                    <div class="w-12 h-12 rounded-full bg-white/5 border border-white/10 flex items-center justify-center text-slate-400 transition-all duration-300 group-hover:border-emerald-500 group-hover:text-emerald-500 group-hover:shadow-[0_0_20px_rgba(16,185,129,0.5)]">
                         <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                            <path stroke-linecap="round" stroke-linejoin="round" d="M16 12a4 4 0 10-8 0 4 4 0 008 0zm0 0v1.5a2.5 2.5 0 005 0V12a9 9 0 10-9 9m4.5-1.206a8.959 8.959 0 01-4.5 1.207" />
                        </svg>
                    </div>
                </a>

                <a href="https://github.com/ZulvikaK" target="_blank" aria-label="GitHub" class="group">
                    <div class="w-12 h-12 rounded-full bg-white/5 border border-white/10 flex items-center justify-center text-slate-400 transition-all duration-300 group-hover:border-emerald-500 group-hover:text-emerald-500 group-hover:shadow-[0_0_20px_rgba(16,185,129,0.5)]">
                        <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="currentColor" viewBox="0 0 24 24">
                            <path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"/>
                        </svg>
                    </div>
                </a>

                <a href="https://medium.com/@zulvika-devi" target="_blank" aria-label="Medium" class="group">
                    <div class="w-12 h-12 rounded-full bg-white/5 border border-white/10 flex items-center justify-center text-slate-400 transition-all duration-300 group-hover:border-emerald-500 group-hover:text-emerald-500 group-hover:shadow-[0_0_20px_rgba(16,185,129,0.5)]">
                        <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="currentColor" viewBox="0 0 24 24">
                            <path d="M13.54 12a6.8 6.8 0 01-6.77 6.82A6.8 6.8 0 010 12a6.8 6.8 0 016.77-6.82A6.8 6.8 0 0113.54 12zM20.96 12c0 3.54-1.51 6.42-3.38 6.42-1.87 0-3.39-2.88-3.39-6.42s1.52-6.42 3.39-6.42 3.38 2.88 3.38 6.42M24 12c0 3.17-.53 5.75-1.19 5.75-.66 0-1.19-2.58-1.19-5.75s.53-5.75 1.19-5.75C23.47 6.25 24 8.83 24 12z"/>
                        </svg>
                    </div>
                </a>

                 <a href="https://www.behance.net/zulvikak" target="_blank" aria-label="Behance" class="group">
                    <div class="w-12 h-12 rounded-full bg-white/5 border border-white/10 flex items-center justify-center text-slate-400 transition-all duration-300 group-hover:border-emerald-500 group-hover:text-emerald-500 group-hover:shadow-[0_0_20px_rgba(16,185,129,0.5)]">
                        <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="currentColor" viewBox="0 0 24 24">
                            <path d="M22 7h-7v-2h7v2zm1.726 10c-.05.362-.156.721-.316 1.078-1.149 2.565-4.691 3.241-7.293 1.369-1.601-1.152-2.363-3.391-2.363-5.569 0-3.506 2.083-5.991 5.383-5.991 1.799 0 3.262.721 4.193 1.875.883 1.094 1.346 2.565 1.271 4.038h-7.293c.035 1.694.973 2.725 2.438 2.725 1.002 0 1.789-.446 2.321-1.314l3.659 1.789zm-3.632-5.342c-.152-1.211-.99-2.133-2.211-2.133-1.318 0-2.254.99-2.377 2.133h4.588zm-14.413 2.133h-3.181v-3.72h3.181c.84 0 1.396.586 1.396 1.86s-.556 1.86-1.396 1.86zm.497-5.787h-3.678v-3.488h3.678c.678 0 1.197.539 1.197 1.744s-.519 1.744-1.197 1.744zm-7.178 11.496h7.021c1.766 0 2.734-.805 2.734-2.27 0-1.113-.664-1.846-1.68-2.08 1.133-.41 1.895-1.211 1.895-2.354 0-1.553-1.25-2.393-2.949-2.393h-2.393v-4.346h-4.629v13.443z"/>
                        </svg>
                    </div>
                </a>

            </div>

            <p class="text-sm font-light text-slate-500 animate-fade-in-up delay-200">© 2026 Zulvika Kusumadevi.</p>
        </div>
    </footer>
  </div>
</template>

<script setup>
import { ref, reactive, watch, onMounted, onUnmounted } from 'vue'
import emailjs from '@emailjs/browser'

const mobileMenuOpen = ref(false)
const selectedProject = ref(null)
const scrolled = ref(false)

// Contact Form State
const form = reactive({ name: '', email: '', message: '' })
const isLoading = ref(false)

// EmailJS Send Function
const sendEmail = async () => {
    isLoading.value = true
    
    try {
        await emailjs.send(
            'service_qa0v678',
            'template_62rp39s',
            {
                name: form.name,
                email: form.email,
                message: form.message
            },
            'iKsTOvB0G9fDmQa-1'
        )
        
        alert('Message sent successfully!')
        
        // Clear form
        form.name = ''
        form.email = ''
        form.message = ''
    } catch (error) {
        console.error('EmailJS Error:', error)
        alert('Failed to send message. Please try again later.')
    } finally {
        isLoading.value = false
    }
}

watch(selectedProject, (newVal) => {
    if (newVal) {
        document.body.style.overflow = 'hidden'
    } else {
        document.body.style.overflow = 'auto'
    }
})

const navLinks = [
  { label: 'Home', href: '#hero' },
  { label: 'About', href: '#about' },
  { label: 'Experience', href: '#experience' },
  { label: 'Projects', href: '#projects' },
  { label: 'Contact', href: '#contact' }
]

const stats = [
    { target: 25, symbol: '+', label: 'Projects Delivered', decimals: 0 },
    { target: 10, symbol: '+', label: 'Cross-functional Teams', decimals: 0 },
    { target: 95, symbol: '%', label: 'On-time Rate', decimals: 0 },
    { target: 4.9, symbol: '/5', label: 'Client Satisfaction', decimals: 1 }
]

const displayStats = reactive(stats.map(() => 0))

const runCounter = (index, endValue, duration = 2000, decimals = 0) => {
    let startTimestamp = null;
    const step = (timestamp) => {
        if (!startTimestamp) startTimestamp = timestamp;
        const progress = Math.min((timestamp - startTimestamp) / duration, 1);
        
        const easeProgress = 1 - Math.pow(1 - progress, 3); 
        
        let current = endValue * easeProgress;
        
        if (decimals === 0) {
            displayStats[index] = Math.floor(current);
        } else {
            displayStats[index] = parseFloat(current.toFixed(decimals));
        }

        if (progress < 1) {
            window.requestAnimationFrame(step);
        } else {
            displayStats[index] = endValue;
        }
    };
    window.requestAnimationFrame(step);
}

// Core Competencies (4 items)
const skills = [
  'AI Project Management',
  'Agentic AI Development',
  'Workflow Automation (n8n)',
  'Quality Assurance Strategy'
]

// Language Skills
const languages = [
  { name: 'Indonesian', level: 'Native Speaker', flag: '🇮🇩', dots: 5 },
  { name: 'English', level: 'Medium', flag: '🇬🇧', dots: 3 }
]

// Education
const education = [
  {
    institution: 'Universitas Gadjah Mada',
    degree: 'Bachelor of Agricultural and Biosystem Engineering',
    field: 'Postharvest and Food Engineering',
    period: '2016 – 2020',
    icon: 'academic'
  },
  {
    institution: 'SMA Negeri 5 Yogyakarta',
    degree: null,
    field: null,
    period: 'Aug 2013 – Aug 2016',
    icon: 'school'
  }
]

// Methodology
const methodology = [
  'Agile & Scrum',
  'Stakeholder Alignment',
  'Risk Mitigation',
  'Technical Documentation'
]

// Tools Stack
const toolsStack = [
  'n8n',
  'JavaScript',
  'Jira',
  'Notion',
  'Postman',
  'Cypress',
  'Datadog'
]

// UPDATED DATA: Experience dengan deskripsi lengkap dan format yang benar
const experience = [
  {
    title: 'Project Manager',
    company: 'PT Teknologi Cekat Indonesia (Cekat.AI)',
    location: 'Yogyakarta, Indonesia',
    period: 'Sept 2025 – Present',
    current: true,
    description: 'Managing AI projects by translating business needs into technical solutions and automation workflows. Coordinating with clients and internal teams to ensure smooth delivery. Building automation workflows and handling API integrations to connect systems. Providing technical support and ensuring stable implementation of AI solutions.'
  },
  {
    title: 'Software Quality Assurance Intern',
    company: 'PT Jala Akuakultur Lestari Alamku',
    location: 'Yogyakarta, Indonesia',
    period: 'Mar 2025 – Aug 2025',
    current: false,
    description: 'Supported system testing by creating test cases and validating features based on requirements. Conducted User Acceptance Testing (UAT) and reported bugs. Worked with developers to resolve issues and improve system quality.'
  },
  {
    title: 'Jr. Strategic Risk Assessment Engineer',
    company: 'PT Privy Identitas Digital',
    location: 'Yogyakarta, Indonesia',
    period: 'Apr 2024 – Dec 2024',
    current: false,
    description: 'Monitored system performance and identified issues to maintain stability. Reported bugs and supported feature deployments for merchants. Collaborated with teams to resolve technical issues and reduce operational risks.'
  },
   {
    title: 'Data Validator',
    company: 'PT Privy Identitas Digital',
    location: 'Yogyakarta, Indonesia',
    period: 'Nov 2022 – Apr 2024',
    current: false,
    description: 'Validated customer e-KYC data to ensure accuracy and compliance. Supported merchant issue resolution and helped maintain service quality. Contributed to efficient and reliable verification processes.'
  },
  {
    title: 'Data Verifier',
    company: 'PT Privy Identitas Digital',
    location: 'Yogyakarta, Indonesia',
    period: 'May 2021 – Nov 2022',
    current: false,
    description: 'Verified and processed customer data according to SOPs. Identified and corrected data issues. Worked with internal teams to ensure accurate and efficient verification.'
  }
]

// Dummy Data untuk Projects (Silakan disesuaikan)
const projects = [
    {
        title: 'The Self-Operating Studio',
        category: 'n8n Automation',
        image: '/n8n_workflow.png',
        description: 'Orchestrated a full-cycle AI customer service workflow using n8n. Features intelligent intent detection, automated CRM data entry, and SLA-based follow-ups.',
        tags: ['n8n', 'AI Agents', 'CRM Integration', 'Webhooks'],
        link: 'https://medium.com/@zulvika-devi/the-self-operating-studio-a-full-cycle-automation-workflow-powered-by-n8n-c0427056d9af',
        details: {
            overview: 'AI-powered customer service automation using n8n to orchestrate AI agents, CRM, and order workflows.',
            fullDescription: 'This project focuses on building an AI-powered customer service automation for a fitness center using n8n as the workflow orchestrator. The system handles customer inquiries, educates users, collects data, and prepares orders before seamless human handoff. It integrates AI agents with CRM to ensure consistent documentation of leads and transactions.',
            features: [
                { title: 'AI-Guided Conversation', icon: 'ChatBubbleBottomCenterTextIcon', desc: 'Handle greetings, intent detection, and profiling using rule-based AI.' },
                { title: 'Progressive Validation', icon: 'ShieldCheckIcon', desc: 'Contextual step-by-step data collection to prevent invalid entries.' },
                { title: 'CRM Integration', icon: 'CircleStackIcon', desc: 'Automatically record leads, membership data, and history into the CRM.' },
                { title: 'Order Automation', icon: 'BanknotesIcon', desc: 'Trigger order creation and invoices upon membership confirmation.' },
                { title: 'SLA Follow-Up', icon: 'ClockIcon', desc: 'Auto-schedule reminders based on defined SLA rules.' },
                { title: 'Human Handoff', icon: 'UserGroupIcon', desc: 'Seamless transfer to agents for final payment processing.' }
            ]
        }
    },
    {
        title: 'Supply Chain Forecaster',
        category: 'Predictive Modeling',
        description: 'Built an end-to-end demand forecasting engine using LSTM networks to optimize inventory levels.',
        tags: ['TensorFlow', 'AWS', 'PostgreSQL']
    },
    {
        title: 'Legal Document Parser',
        category: 'NLP & Automation',
        description: 'Automated the extraction of critical clauses from complex legal contracts using custom NER models.',
        tags: ['Spacy', 'React', 'Node.js']
    }
]

const handleScroll = () => {
  scrolled.value = window.scrollY > 50
}

onMounted(() => {
  window.addEventListener('scroll', handleScroll)

  const observer = new IntersectionObserver((entries) => {
    entries.forEach((entry) => {
      if (entry.isIntersecting) {
        entry.target.classList.add('active')

        if (entry.target.classList.contains('stats-container')) {
            stats.forEach((stat, index) => {
                runCounter(index, stat.target, 2500, stat.decimals);
            });
            observer.unobserve(entry.target); 
        } else {
             observer.unobserve(entry.target)
        }
      }
    })
  }, {
    threshold: 0.1,
    rootMargin: "0px 0px -50px 0px"
  })

  setTimeout(() => {
    document.querySelectorAll('.reveal').forEach((el) => {
      observer.observe(el)
    })
    const statsContainer = document.querySelector('.stats-container');
    if (statsContainer) observer.observe(statsContainer);
  }, 100)
})

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll)
})
</script>

<style scoped>
/* Animasi Khusus */
@keyframes fadeInUp {
    from {
        opacity: 0;
        transform: translate3d(0, 40px, 0);
    }
    to {
        opacity: 1;
        transform: translate3d(0, 0, 0);
    }
}

.animate-fade-in-up {
    animation: fadeInUp 0.8s ease-out forwards;
    opacity: 0; 
}

/* Animasi Pulse yang lebih lambat untuk background */
@keyframes pulseSlow {
    0%, 100% { opacity: 0.4; transform: scale(1); }
    50% { opacity: 0.6; transform: scale(1.1); }
}

.animate-pulse-slow {
    animation: pulseSlow 8s cubic-bezier(0.4, 0, 0.6, 1) infinite;
}

@keyframes float {
    0%, 100% { transform: translateY(0) scale(1); }
    50% { transform: translateY(-20px) scale(1.05); }
}

.animate-float {
    animation: float 10s ease-in-out infinite;
}

.delay-100 { animation-delay: 0.1s; }
.delay-200 { animation-delay: 0.2s; }
.delay-300 { animation-delay: 0.3s; }
.delay-700 { animation-delay: 0.7s; }
</style>