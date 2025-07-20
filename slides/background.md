---
layout: center
class: text-center

---

# LLM Apps Fail Silently

<div class="grid grid-cols-3 gap-8 pt-8">
  <div v-click class="text-center">
    <h3 class="text-xl font-bold text-white">Performance Drift</h3>
  </div>
  <div v-click class="text-center">
    <h3 class="text-xl font-bold text-white">Data Paralysis</h3>
  </div>
  <div v-click class="text-center">
    <h3 class="text-xl font-bold text-white">Missing the Forest</h3>
  </div>
</div>

<style>

</style>

<!--
Speaker notes:
- Performance drift: Small changes add up to big problems
- Data paralysis: We have data but don't know what matters most
- Missing the forest: Focus on individual issues instead of patterns
-->

---
layout: two-cols
layoutClass: gap-16
---

# Performance Drift

<v-click>

## Silent degradation kills apps

<div class="space-y-8 mt-8">
  <div class="flex items-center space-x-4">
    <div class="w-4 h-4 bg-red-400 rounded-full flex-shrink-0"></div>
    <span class="text-lg">Model updates change behavior</span>
  </div>
  <div class="flex items-center space-x-4">
    <div class="w-4 h-4 bg-orange-400 rounded-full flex-shrink-0"></div>
    <span class="text-lg">Prompt tweaks shift outputs</span>
  </div>
  <div class="flex items-center space-x-4">
    <div class="w-4 h-4 bg-yellow-400 rounded-full flex-shrink-0"></div>
    <span class="text-lg">Edge cases accumulate over time</span>
  </div>
</div>

</v-click>

::right::

<v-click>

<div class="flex items-center justify-center h-full">
  <img src="https://media4.giphy.com/media/v1.Y2lkPTc5MGI3NjExc3NtbHlxOW95OXQzdW5mZWFiYmxxZGl0Ynd6bnJhODIyNG9tZ2RwYSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/UKF08uKqWch0Y/giphy.gif" alt="This is fine" class="max-w-full max-h-96 rounded-lg" />
</div>

</v-click>

<style>
h1 {
  background: linear-gradient(45deg, #ef4444 10%, #f97316 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

<!--
Speaker notes:
- Like a slow gas leak - dangerous because you don't notice
- Each change seems harmless in isolation
- By the time you notice, significant damage is done
-->

---
layout: two-cols
layoutClass: gap-16
---

# Data Paralysis

<v-click>

## Too much data, no direction

<div class="space-y-8 mt-8">
  <div class="flex items-center space-x-4">
    <div class="w-4 h-4 bg-red-400 rounded-full flex-shrink-0"></div>
    <span class="text-lg">Terabytes of logs to analyze</span>
  </div>
  <div class="flex items-center space-x-4">
    <div class="w-4 h-4 bg-orange-400 rounded-full flex-shrink-0"></div>
    <span class="text-lg">User priorities buried deep</span>
  </div>
  <div class="flex items-center space-x-4">
    <div class="w-4 h-4 bg-yellow-400 rounded-full flex-shrink-0"></div>
    <span class="text-lg">Generic insights don't help</span>
  </div>
</div>

</v-click>

::right::

<v-click>

<div class="flex items-center justify-center h-full">
  <img src="https://media0.giphy.com/media/v1.Y2lkPTc5MGI3NjExa3NiMnpibHhwZ3M2ZGVsZW9wMmw5Z2J4YzN6MzFpY29ob2JpczI0eSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/LKTTAzGboJGzC/giphy.gif" alt="Overwhelmed" class="max-w-full max-h-96 rounded-lg" />
</div>

</v-click>

<style>
h1 {
  background: linear-gradient(45deg, #ef4444 10%, #f97316 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

<!--
Speaker notes:
- Classic advice with no actionable guidance
- User demands and goals are already there in the data
- Traditional methods give generic topics like "various technical discussions"
- We need to extract what users actually care about
-->

---
layout: two-cols
layoutClass: gap-16
---

# Missing the Forest

<v-click>

## Hyper-focus on specifics blinds us

<div class="space-y-8 mt-8">
  <div class="flex items-center space-x-4">
    <div class="w-4 h-4 bg-red-400 rounded-full flex-shrink-0"></div>
    <span class="text-lg">Build XX for YY specific use case</span>
  </div>
  <div class="flex items-center space-x-4">
    <div class="w-4 h-4 bg-orange-400 rounded-full flex-shrink-0"></div>
    <span class="text-lg">Miss broader capability patterns</span>
  </div>
  <div class="flex items-center space-x-4">
    <div class="w-4 h-4 bg-yellow-400 rounded-full flex-shrink-0"></div>
    <span class="text-lg">Reactive, not strategic</span>
  </div>
</div>

</v-click>

::right::

<v-click>

<div class="flex items-center justify-center h-full">
  <img src="https://media2.giphy.com/media/v1.Y2lkPTc5MGI3NjExMnBraXkyMHN1ZHo3NGt4dnN2M2duNHF5ZHlqZ3N1a3Z0cHo2ZzJ3ZSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/l0G18bja0mbTQVuxO/giphy.gif" alt="Missing the forest for the trees" class="max-w-full max-h-96 rounded-lg" />
</div>

</v-click>

<style>
h1 {
  background: linear-gradient(45deg, #ef4444 10%, #f97316 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

<!--
Speaker notes:
- Teams get stuck building specific features for individual requests
- Miss the underlying capability gaps that drive multiple use cases
- React to symptoms instead of addressing root needs
- This leads us to ask: what kind of feedback do users actually give?
-->

---
layout: center
class: text-center

---

# Every User Complaint Falls Into Two Buckets

<v-click>

<div class="text-xl text-gray-600 mt-8">
  Understanding this pattern changes everything
</div>

</v-click>
