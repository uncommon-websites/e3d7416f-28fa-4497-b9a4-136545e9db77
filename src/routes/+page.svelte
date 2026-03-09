<script lang="ts">
  // Icons
  import { Play, Mic, Music, Type, Video, ArrowRight } from 'lucide-svelte';
</script>

<main class="w-full overflow-hidden">
  <!-- Hero Section -->
  <section class="relative overflow-hidden">
      <div class="max-w-[1440px] mx-auto px-6 lg:px-12 pt-16 lg:pt-24 pb-16">
          
          <!-- Hero Content Grid -->
          <div class="grid grid-cols-1 lg:grid-cols-12 gap-10 lg:gap-8 items-start">
              
              <!-- Left Column: Headline & CTA -->
              <div class="col-span-1 lg:col-span-7 xl:col-span-7">
                  <h1 class="text-[52px] sm:text-6xl lg:text-[84px] leading-tight tracking-tight font-medium text-[#111111] animate-fade-in-up delay-100 text-balance">
                      From Set to Edit Bay in Seconds
                  </h1>
                  
                  <div class="mt-10 lg:mt-14 animate-fade-in-up delay-300">
                      <a href="#" class="inline-flex items-center justify-center px-6 py-3 rounded-full bg-[#0ea5e9] text-white text-[16px] font-medium hover:opacity-90 transition-colors duration-200 active:scale-[0.97]">
                          Start Organizing Free
                      </a>
                  </div>
              </div>

              <!-- Right Column: Description -->
              <div class="col-span-1 lg:col-span-5 xl:col-span-4 xl:col-start-9">
                  <p class="text-[17px] lg:text-[18px] leading-relaxed max-w-2xl text-[#444444] text-pretty animate-fade-in-up delay-200 mt-2 lg:mt-3">
                      Automate your ingest and syncing workflow. Cocreate delivers organized footage directly to your edit bay via automated slate reading, multi-camera grouping, and dialogue transcription.
                  </p>
              </div>

          </div>

          <!-- Hero Image Area with Framing -->
          <div class="mt-24 lg:mt-32 relative animate-scale-in delay-400">
              
              <!-- Framing Line & Ticks -->
              <div class="absolute top-0 left-0 right-0 h-px bg-gray-200"></div>
              <div class="absolute top-[-2px] left-0 w-px h-[5px] bg-black"></div>
              <div class="absolute top-[-2px] right-0 w-px h-[5px] bg-black"></div>

              <!-- Image Container -->
              <div class="pt-16 lg:pt-20">
                  <div class="relative w-full rounded-[32px] overflow-hidden shadow-[0_20px_40px_-15px_rgba(0,0,0,0.1)]">
                      <img 
                          src="https://imolwncbqxugevwmleed.supabase.co/storage/v1/object/public/public-assets/hero-images/e3d7416f-28fa-4497-b9a4-136545e9db77/hero-2-img-0-1773048221568.png" 
                          alt="Cocreate Studio Interface" 
                          class="w-full h-auto object-cover block"
                      />
                  </div>
              </div>

          </div>

      </div>
  </section>

  <!-- Intro Section -->
  <section class="max-w-[1000px] mx-auto px-6 py-24 text-center">
    <span class="text-sm font-medium text-gray-500 mb-4 block">Introducing Cocreate</span>
    <h2 class="text-4xl md:text-5xl font-medium tracking-tight mb-8 leading-tight">
      Modernize the workflow between set and the cutting room. Capture post-production pipelines and scale to studio-wide adoption via time-to-edit efficiency.
    </h2>
    
    <div class="flex flex-wrap justify-center gap-x-6 gap-y-3 text-sm text-gray-600 mb-10">
      <span class="flex items-center gap-2 px-3 py-1 bg-gray-50 rounded-full border border-gray-100"><Type size={14} /> Slate Reading</span>
      <span class="flex items-center gap-2 px-3 py-1 bg-gray-50 rounded-full border border-gray-100"><Video size={14} /> Multi-Camera Grouping</span>
      <span class="flex items-center gap-2 px-3 py-1 bg-gray-50 rounded-full border border-gray-100"><Mic size={14} /> Dialogue Transcription</span>
      <span class="flex items-center gap-2 px-3 py-1 bg-gray-50 rounded-full border border-gray-100"><Music size={14} /> Timecode Jamming</span>
      <span class="flex items-center gap-2 px-3 py-1 bg-gray-50 rounded-full border border-gray-100"><Type size={14} /> Script Notes Sync</span>
    </div>

    <button class="inline-flex items-center gap-2 bg-black text-white pl-3 pr-5 py-2 rounded-full text-sm font-medium hover:bg-gray-800 transition-colors">
      <div class="w-6 h-6 bg-white rounded-full flex items-center justify-center">
        <Play size={10} class="fill-black text-black ml-0.5" />
      </div>
      Watch demo
    </button>
  </section>

  <!-- Features List Section -->
  <section class="max-w-[1400px] mx-auto px-6 py-12 relative">
    <div class="grid grid-cols-1 md:grid-cols-2 gap-24">
        
        <!-- Feature 1 -->
        <div class="flex flex-col justify-center order-1 md:order-1">
            <h3 class="text-3xl font-medium mb-4">Automated Slate Reading</h3>
            <p class="text-gray-600 leading-relaxed mb-6">
                Stop manually logging clips. Cocreate uses computer vision to read clapperboards and automatically labels your footage with scene, shot, and take metadata.
            </p>
        </div>
        <div class="bg-gray-50 rounded-2xl p-6 border border-gray-100 order-2 md:order-2">
            <div class="text-xs text-gray-400 mb-4 font-medium uppercase tracking-wide">Clip Metadata</div>
            <div class="space-y-3">
                {#each [
                    {name: "A001_C001_0512", desc: "Scene 4A, Take 1", icon: Video},
                    {name: "A001_C002_0512", desc: "Scene 4A, Take 2", icon: Video},
                    {name: "B002_C014_0512", desc: "Scene 4B, Take 1", icon: Video},
                    {name: "C003_C005_0512", desc: "Scene 5, Take 1", icon: Video},
                    {name: "C003_C006_0512", desc: "Scene 5, Take 2", icon: Video},
                ] as clip}
                <div class="flex items-center gap-3 p-2 hover:bg-white rounded-lg transition-colors cursor-pointer group">
                    <div class="w-10 h-10 rounded-lg bg-gray-200 flex items-center justify-center text-gray-500">
                        <svelte:component this={clip.icon} size={20} />
                    </div>
                    <div>
                        <div class="text-sm font-medium text-gray-900">{clip.name}</div>
                        <div class="text-xs text-gray-500">{clip.desc}</div>
                    </div>
                </div>
                {/each}
            </div>
        </div>

        <!-- Feature 2 -->
        <div class="bg-gray-50 rounded-2xl p-6 border border-gray-100 min-h-[400px] flex items-center justify-center order-4 md:order-3 relative overflow-hidden">
             <!-- Abstract visualization for syncing -->
             <div class="absolute inset-0 flex items-center justify-center">
                 <div class="w-full h-full bg-[radial-gradient(circle_at_center,_var(--tw-gradient-stops))] from-blue-100 via-gray-50 to-gray-50"></div>
                 <div class="flex flex-col gap-4 w-full px-12">
                     <div class="h-8 bg-blue-500/20 rounded-md w-full animate-pulse"></div>
                     <div class="h-8 bg-blue-500/40 rounded-md w-3/4 animate-pulse delay-75"></div>
                     <div class="h-8 bg-blue-500/60 rounded-md w-5/6 animate-pulse delay-150"></div>
                 </div>
             </div>
        </div>
        <div class="flex flex-col justify-center order-3 md:order-4">
            <h3 class="text-3xl font-medium mb-4">Multi-Camera Grouping</h3>
            <p class="text-gray-600 leading-relaxed">
                Sync un-jammed timecodes effortlessly. Cocreate aligns audio and video from multiple cameras, creating perfect multicam sequences ready for your NLE.
            </p>
        </div>

        <!-- Feature 3 -->
        <div class="flex flex-col justify-center order-5 md:order-5">
            <h3 class="text-3xl font-medium mb-4">Script Supervisor Note Sync</h3>
            <p class="text-gray-600 leading-relaxed">
                Turn incoherent script notes into actionable metadata. We synchronize notes directly to the timeline, so editors have context exactly where they need it.
            </p>
        </div>
        <div class="bg-gray-50 rounded-2xl p-6 border border-gray-100 min-h-[300px] flex items-center justify-center order-6 md:order-6">
             <div class="w-full max-w-xs bg-white rounded-xl shadow-sm p-4 border border-gray-100">
                 <div class="flex items-center gap-3 mb-3">
                     <div class="w-8 h-8 bg-[#0ea5e9]/10 rounded-lg flex items-center justify-center text-[#0ea5e9]">
                         <Type size={16} />
                     </div>
                     <div class="text-sm font-medium">Script Notes</div>
                 </div>
                 <div class="h-2 bg-gray-100 rounded-full mb-2 w-full"></div>
                 <div class="h-2 bg-gray-100 rounded-full w-2/3"></div>
                 <div class="mt-4 text-xs text-gray-500 italic">"Good take, but camera bumped at 01:04:22:10"</div>
             </div>
        </div>

        <!-- Feature 4 -->
        <div class="bg-gray-50 rounded-2xl p-6 border border-gray-100 min-h-[300px] flex items-center justify-center order-8 md:order-7">
            <div class="relative w-full max-w-md bg-white rounded-xl shadow-sm p-6 border border-gray-100">
                <div class="text-lg font-medium mb-2">"We need to <span class="bg-gray-100 text-gray-800 px-1 rounded">cut to the wide</span> here."</div>
                <div class="flex items-center gap-2 mt-4 text-xs text-gray-500">
                    <span class="px-2 py-1 bg-gray-100 rounded">Audio</span>
                    <ArrowRight size={12} />
                    <span class="px-2 py-1 bg-blue-50 text-blue-700 border border-blue-100 rounded">Transcribed Text</span>
                </div>
            </div>
        </div>
        <div class="flex flex-col justify-center order-7 md:order-8">
            <h3 class="text-3xl font-medium mb-4">Dialogue Transcription</h3>
            <p class="text-gray-600 leading-relaxed">
                Generate accurate transcripts for every clip. Search through hours of footage instantly by typing a keyword, and jump straight to the exact frame.
            </p>
        </div>

    </div>
  </section>
  
  <!-- Floating Action Bar (Stickyish) -->
  <div class="sticky bottom-6 z-40 flex justify-center pointer-events-none">
      <div class="bg-white/80 backdrop-blur-md border border-gray-200 shadow-lg rounded-full py-3 px-6 flex items-center gap-6 pointer-events-auto">
          <span class="text-sm font-medium text-gray-900 hidden sm:block">NLE-ready project structures in under 20 minutes</span>
          <button class="bg-[#0ea5e9] text-white text-xs font-bold px-4 py-2 rounded-full hover:opacity-90 transition-colors">
              Get Started
          </button>
      </div>
  </div>

  <!-- Seamless Timeline Section -->
  <section class="max-w-[1400px] mx-auto px-6 py-24">
    <div class="text-center max-w-2xl mx-auto mb-16">
        <h2 class="text-4xl font-medium tracking-tight mb-4">Compatible with major Non-Linear Editors</h2>
        <p class="text-gray-600">Cocreate outputs completed project structures that drop straight into Premiere Pro, Avid Media Composer, and DaVinci Resolve.</p>
    </div>

    <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
        <!-- Card 1: Timeline (Wide) -->
        <div class="md:col-span-2 bg-gray-50 rounded-3xl p-8 border border-gray-100 overflow-hidden relative min-h-[300px]">
            <div class="relative z-10 max-w-md">
                <h3 class="text-xl font-medium mb-2">Stringout Creation</h3>
                <p class="text-sm text-gray-600 leading-relaxed">Automate menial tasks like stringout creation. We build your initial sequences so you can start cutting immediately.</p>
            </div>
            <div class="absolute right-0 bottom-0 w-2/3 h-2/3 translate-x-10 translate-y-10">
                 <div class="w-full h-full bg-white rounded-tl-xl shadow-lg border border-gray-100 p-4 transform -rotate-6">
                     <img src="/generated/image-a-modern-non-linear-editing-timeline-int-1773048570439-3.webp" alt="NLE Timeline" class="w-full h-full object-cover rounded-lg" />
                 </div>
            </div>
        </div>

        <!-- Card 2: Video Support -->
        <div class="bg-gray-50 rounded-3xl p-8 border border-gray-100 overflow-hidden relative min-h-[300px]">
             <div class="relative z-10">
                <h3 class="text-xl font-medium mb-2">Timecode Jamming</h3>
                <p class="text-sm text-gray-600 leading-relaxed">Fix un-jammed timecodes automatically. We align everything perfectly before you even open your editor.</p>
            </div>
            <div class="absolute inset-x-0 bottom-0 h-40 bg-gradient-to-t from-gray-200 to-transparent"></div>
            <div class="absolute bottom-4 right-4 left-4 h-32 bg-black rounded-lg shadow-lg overflow-hidden flex items-center justify-center font-mono text-white text-2xl">
                01:24:15:08
            </div>
        </div>
    </div>
  </section>

  <!-- Built for Every Creator -->
  <section class="max-w-[1400px] mx-auto px-6 py-24">
      <div class="text-center max-w-2xl mx-auto mb-16">
        <h2 class="text-4xl font-medium tracking-tight mb-4">Built for post-production professionals</h2>
        <p class="text-gray-600">Designed by direct collaboration with editors, DITs, and UPMs to address systemic inefficiencies in footage organization.</p>
    </div>

    <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
        <!-- Creator 1 -->
        <div class="group">
            <div class="aspect-square rounded-2xl overflow-hidden mb-6 relative">
                <img src="/generated/image-portrait-of-a-professional-assistant-edi-1773048563629-0.webp" class="w-full h-full object-cover transition-transform duration-500 group-hover:scale-105" alt="Assistant Editor" />
                <div class="absolute inset-0 bg-gradient-to-t from-gray-900/60 to-transparent mix-blend-multiply"></div>
            </div>
            <h3 class="text-lg font-medium mb-2">Assistant Editors</h3>
            <p class="text-xs text-gray-500 leading-relaxed">Eliminate days of manual ingest and syncing. Get straight to organizing the story instead of logging clips.</p>
        </div>

        <!-- Creator 2 -->
        <div class="group">
            <div class="aspect-square rounded-2xl overflow-hidden mb-6 relative">
                <img src="/generated/image-portrait-of-a-digital-imaging-technician-1773048566182-1.webp" class="w-full h-full object-cover transition-transform duration-500 group-hover:scale-105" alt="DIT" />
                <div class="absolute inset-0 bg-gradient-to-t from-gray-900/60 to-transparent mix-blend-multiply"></div>
            </div>
            <h3 class="text-lg font-medium mb-2">Digital Imaging Technicians</h3>
            <p class="text-xs text-gray-500 leading-relaxed">Ensure metadata flows seamlessly from set to post. Prevent lost information and incoherent notes.</p>
        </div>

        <!-- Creator 3 -->
        <div class="group">
            <div class="aspect-square rounded-2xl overflow-hidden mb-6 relative">
                <img src="/generated/image-portrait-of-a-post-production-supervisor-1773048568073-2.webp" class="w-full h-full object-cover transition-transform duration-500 group-hover:scale-105" alt="Post-Production Supervisor" />
                <div class="absolute inset-0 bg-gradient-to-t from-gray-900/60 to-transparent mix-blend-multiply"></div>
            </div>
            <h3 class="text-lg font-medium mb-2">Post-Production Supervisors</h3>
            <p class="text-xs text-gray-500 leading-relaxed">Scale to studio-wide adoption with improved time-to-edit efficiency. Keep your teams competitive and focused on creativity.</p>
        </div>
    </div>
  </section>

  <!-- Bottom CTA -->
  <section class="max-w-[1400px] mx-auto px-6 py-24 flex flex-col items-center text-center border-t border-gray-100">
      <h2 class="text-4xl font-medium tracking-tight mb-8">Ready to modernize your workflow?</h2>
      <div class="flex items-center gap-4">
          <button class="bg-[#0ea5e9] text-white px-6 py-3 rounded-full font-medium hover:opacity-90 transition-colors text-sm">
              Book a Demo
          </button>
          <button class="bg-white text-black border border-gray-200 px-6 py-3 rounded-full font-medium hover:bg-gray-50 transition-colors text-sm">
              Contact Sales
          </button>
      </div>
  </section>
</main>

<style>
    /* Custom scrollbar hide for clean look in some areas if needed */
    .no-scrollbar::-webkit-scrollbar {
        display: none;
    }
    .no-scrollbar {
        -ms-overflow-style: none;
        scrollbar-width: none;
    }
</style>

