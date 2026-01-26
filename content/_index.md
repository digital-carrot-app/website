---
date: '2025-07-27T08:00:58-06:00'
layout: "hextra-home"
# title: 'Home'
---

<div class="flex flex-col md:flex-row items-center gap-8 pb-12 px-6">
  <!-- Text and buttons section (2/3) -->
  <div class="w-full md:w-2/3">
    <div class="flex flex-col md:flex-row items-center md:items-start gap-4 mb-6">
      <img src="/images/logo-icon.svg" width="80px" class="flex-shrink-0" alt="Digital Carrot" />
      <div>
{{< hextra/hero-headline >}}
  Turn your Digital Distractions into a Super Power
  {{< /hextra/hero-headline >}}
</div>
    </div>
    <div class="mb-4">
    <p class="text-lg text-gray-600 dark:text-gray-400">
      Build healthy habits by blocking apps, websites and video games until you meet your daily goals.
    </p>
    </div>
    <div class="mb-6 h-10">
      <p id="rotating-example" class="text-base text-gray-500 dark:text-gray-400 italic transition-opacity duration-500"></p>
    </div>
    <div class="mb-4">
      <div id="download-buttons" class="flex flex-wrap gap-4">
        <a id="btn-iphone" href="https://itunes.apple.com/app/id6749398240" class="download-btn inline-flex items-center gap-2 px-5 py-3 rounded-lg border border-gray-300 dark:border-neutral-700 bg-white dark:bg-neutral-800 text-gray-700 dark:text-gray-200 hover:border-blue-500 transition-colors" data-os="iphone">
          <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><rect x="5" y="2" width="14" height="20" rx="2" ry="2" stroke-width="2"/><line x1="12" y1="18" x2="12" y2="18" stroke-width="3" stroke-linecap="round"/></svg>
          iPhone
        </a>
        <a id="btn-android" href="https://forms.gle/JQr9sjcNNEQRaYNV8" class="download-btn inline-flex items-center gap-2 px-5 py-3 rounded-lg border border-gray-300 dark:border-neutral-700 bg-white dark:bg-neutral-800 text-gray-700 dark:text-gray-200 hover:border-blue-500 transition-colors" data-os="android">
          <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><rect x="5" y="2" width="14" height="20" rx="2" ry="2" stroke-width="2"/><line x1="12" y1="18" x2="12" y2="18" stroke-width="3" stroke-linecap="round"/></svg>
          Android
        </a>
        <a id="btn-macos" href="https://github.com/digital-carrot-app/release/releases/latest/download/Digital.Carrot.dmg" class="download-btn inline-flex items-center gap-2 px-5 py-3 rounded-lg border border-gray-300 dark:border-neutral-700 bg-white dark:bg-neutral-800 text-gray-700 dark:text-gray-200 hover:border-blue-500 transition-colors" data-os="macos">
          <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><rect x="2" y="3" width="20" height="14" rx="2" ry="2" stroke-width="2"/><line x1="8" y1="21" x2="16" y2="21" stroke-width="2"/><line x1="12" y1="17" x2="12" y2="21" stroke-width="2"/></svg>
          macOS
        </a>
        <a id="btn-windows" href="https://github.com/digital-carrot-app/release/releases/latest/download/digital-carrot-windows-x86_64.exe" class="download-btn inline-flex items-center gap-2 px-5 py-3 rounded-lg border border-gray-300 dark:border-neutral-700 bg-white dark:bg-neutral-800 text-gray-700 dark:text-gray-200 hover:border-blue-500 transition-colors" data-os="windows">
          <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><rect x="2" y="3" width="20" height="14" rx="2" ry="2" stroke-width="2"/><line x1="8" y1="21" x2="16" y2="21" stroke-width="2"/><line x1="12" y1="17" x2="12" y2="21" stroke-width="2"/></svg>
          Windows
        </a>
        <a id="btn-linux" href="https://forms.gle/ioAMHHMfGvCcTMMs8" class="download-btn inline-flex items-center gap-2 px-5 py-3 rounded-lg border border-gray-300 dark:border-neutral-700 bg-white dark:bg-neutral-800 text-gray-700 dark:text-gray-200 hover:border-blue-500 transition-colors" data-os="linux">
          <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><rect x="2" y="3" width="20" height="14" rx="2" ry="2" stroke-width="2"/><line x1="8" y1="21" x2="16" y2="21" stroke-width="2"/><line x1="12" y1="17" x2="12" y2="21" stroke-width="2"/></svg>
          Linux
        </a>
      </div>
    </div>
  </div>
  <!-- Hero image section (1/3) -->
  <div class="w-full md:w-1/3">
    <img src="/images/smaller_hero.png" alt="Digital Carrot" class="w-full h-auto" />
  </div>
</div>

<script>
(function() {
  // OS detection for download buttons
  const ua = navigator.userAgent;
  const platform = navigator.platform;
  let os = 'unknown';
  
  if (/iPhone|iPad|iPod/.test(ua)) {
    os = 'iphone';
  } else if (/Android/.test(ua)) {
    os = 'android';
  } else if (/Mac/.test(platform)) {
    os = 'macos';
  } else if (/Win/.test(platform)) {
    os = 'windows';
  } else if (/Linux/.test(platform)) {
    os = 'linux';
  }
  
  const container = document.getElementById('download-buttons');
  const buttons = container.querySelectorAll('.download-btn');
  
  buttons.forEach(btn => {
    if (btn.dataset.os === os) {
      // Highlight the current OS button
      btn.classList.remove('bg-white', 'dark:bg-neutral-800', 'text-gray-700', 'dark:text-gray-200', 'border-gray-300', 'dark:border-neutral-700');
      btn.classList.add('bg-blue-600', 'text-white', 'border-blue-600', 'font-semibold', );
      // Move to front
      container.prepend(btn);
    }
  });

  // Rotating examples
  const examples = [
    'Block <span class="text-orange-400 font-semibold">Instagram</span> until my Apple Watch says I\'ve walked <span class="text-emerald-600 font-semibold">6000 steps</span>',
    'Block <span class="text-orange-400 font-semibold">TikTok</span> until my GPS says I\'ve spent <span class="text-emerald-600 font-semibold">30 minutes at the gym</span>',
    'Block <span class="text-orange-400 font-semibold">Facebook</span> until I\'ve spent <span class="text-emerald-600 font-semibold">15 minutes tidying my kitchen</span>',
    'Block <span class="text-orange-400 font-semibold">X</span> until I\'ve checked off <span class="text-emerald-600 font-semibold">all my tasks in Todoist</span>',
    'Block <span class="text-orange-400 font-semibold">Netflix</span> from <span class="text-emerald-600 font-semibold">9 to 5 on weekdays</span>'
  ];
  
  const exampleEl = document.getElementById('rotating-example');
  let currentIndex = 0;
  
  function showExample() {
    exampleEl.style.opacity = '0';
    setTimeout(() => {
      exampleEl.innerHTML = examples[currentIndex];
      exampleEl.style.opacity = '1';
      currentIndex = (currentIndex + 1) % examples.length;
    }, 500);
  }
  
  showExample();
  setInterval(showExample, 4000);
})();
</script>


{{< hextra/hero-headline >}}
How it Works
{{< /hextra/hero-headline >}}
<div class="hx:mt-6 hx:mb-6"></div>

{{< hextra/feature-grid cols="3" >}}
  {{< hextra/feature-card
    title="1. Set up your goals"
    subtitle="Progress towards your goals is tracked automatically. Goals can be created from a premade template or fully programmed with a simple script."
    image="/images/goals.png"

    style="height: 400px"
    imageClass="hx:object-contain hx:w-full hx:h-auto"
  >}}

  {{< hextra/feature-card
    title="2. Select your distractions"
    subtitle="Pick the apps and websites that are the most distracting to you. These will all be blocked until you've completed your goals."
    image="/images/pick-distractions.png"

    style="height: 400px"
    imageClass="hx:object-contain hx:w-full hx:h-auto"
  >}}

  {{< hextra/feature-card
    title="3. Get s**t done"
    subtitle="Once you've finished your goals for the day your distracting apps will be unlocked and you can enjoy them guilt free."
    image="/images/complete-goals.png"

    style="height: 400px"
    imageClass="hx:object-contain hx:w-full hx:h-auto"
  >}}

{{< /hextra/feature-grid >}}
<div class="hx:mt-6 hx:mb-6"></div>

<div class="hx:mt-6 hx:mb-6">
{{< hextra/hero-headline >}}
  What do you want to achieve?
{{< /hextra/hero-headline >}}
</div>

<div class="hx:mt-6 hx:mb-6">
{{< hextra/hero-section >}}
  Get Healthy
{{< /hextra/hero-section >}}
{{< hextra/hero-subtitle >}}
  Block social media, games and online video until I...
{{< /hextra/hero-subtitle >}}

</div>


{{< hextra/feature-grid cols="3" >}}
  {{< hextra/feature-card
    title="Burn 300 calories"
    subtitle="Use your health data to verify that you've been active throughout the day."
    image="/images/goals/active_calories.jpeg"
    style="height: 300px"
    imageClass="hx:object-contain hx:w-full hx:h-auto"
  >}}

  {{< hextra/feature-card
    title="Go to the Gym"
    subtitle="Use your phone's GPS to verify that you actually went to the gym and spent enough time there."
    image="/images/goals/gym.jpeg"
    style="height: 300px"
    imageClass="hx:object-contain hx:w-full hx:h-auto"
  >}}

  {{< hextra/feature-card
    title="Spend 15 minutes Meditating"
    subtitle="Set a timer and meditate until it is done."
    image="/images/goals/meditate.jpeg"
    style="height: 300px"
    imageClass="hx:object-contain hx:w-full hx:h-auto"
  >}}
{{< /hextra/feature-grid >}}

<div class="hx:mt-6 hx:mb-6"></div>


<div class="hx:mt-6 hx:mb-6">
{{< hextra/hero-section >}}
  Cut down on Screentime
{{< /hextra/hero-section >}}
{{< hextra/hero-subtitle >}}
  Block apps, limit usage to certain hours or set a time limit.
{{< /hextra/hero-subtitle >}}
</div>

{{< hextra/feature-grid cols="3" >}}
  {{< hextra/feature-card
    title="Limit myself to 30 minutes of scrolling per day"
    subtitle="Set a timer that only grants access when it is running."
    image="/images/goals/social_media_limit.jpeg"
    style="height: 300px"
    imageClass="hx:object-contain hx:w-full hx:h-auto"
  >}}

  {{< hextra/feature-card
    title="Get out of Bed before using Social Media"
    subtitle="Create a 15 minute timed goal that you have to start as soon as you wake up."
    image="/images/goals/get_out_of_bed.jpeg"
    style="height: 300px"
    imageClass="hx:object-contain hx:w-full hx:h-auto"
  >}}

  {{< hextra/feature-card
    title="Block Distractions during work Hours"
    subtitle="Create a schedule to block or unblock apps during certain time windows."
    image="/images/goals/schedule.jpeg"
    style="height: 300px"
    imageClass="hx:object-contain hx:w-full hx:h-auto"
  >}}
{{< /hextra/feature-grid >}}

<div class="hx:mt-6 hx:mb-6"></div>


<div class="hx:mt-6 hx:mb-6">
{{< hextra/hero-section >}}
  Improve your Productivity
{{< /hextra/hero-section >}}
{{< hextra/hero-subtitle >}}
  Give yourself some extra motivation to finish your to-do list or learn a new skill.
{{< /hextra/hero-subtitle >}}
</div>

{{< hextra/feature-grid cols="3" >}}
  {{< hextra/feature-card
    title="Finish all the tasks on your To-Do List"
    subtitle="Track how many To-Do's you have to complete in Apple Reminders or Todoist."
    image="/images/goals/to_do.jpeg"
    style="height: 300px"
    imageClass="hx:object-contain hx:w-full hx:h-auto"
  >}}

  {{< hextra/feature-card
    title="Spend 45 minutes studying on Khan Academy"
    subtitle="Set goals to spend time on websites that help you learn new things."
    image="/images/goals/website_usage.png"
    style="height: 300px"
    imageClass="hx:object-contain hx:w-full hx:h-auto"
  >}}

  {{< hextra/feature-card
    title="Create Healthy Habits"
    subtitle="Set a goal that has to be manually checked off every day."
    image="/images/goals/healthy_habits.jpeg"
    style="height: 300px"
    imageClass="hx:object-contain hx:w-full hx:h-auto"
  >}}
{{< /hextra/feature-grid >}}


<!--<div class="hx:mt-6 hx:mb-6"></div>


<div class="hx:mt-6 hx:mb-6">
{{< hextra/hero-section >}}
  Get out and Socialize
{{< /hextra/hero-section >}}
</div>

{{< hextra/feature-grid cols="2" >}}
  {{< hextra/feature-card
    title="Leave your house for 1 hour Every Day"
    subtitle=""
    style="height: 300px"
    imageClass="hx:object-contain hx:w-full hx:h-auto"
  >}}

  {{< hextra/feature-card
    title="Disable your distractions at Social Events"
    subtitle=""
    style="height: 300px"
    imageClass="hx:object-contain hx:w-full hx:h-auto"
  >}}

{{< /hextra/feature-grid >}}-->
