---
layout: center
class: text-center
---

# Traditional Methods Have Limitations

<v-click>

## BERTopic is excellent for many use cases

<div class="text-xl text-gray-600 mt-8">
  But LLM conversations need a different approach
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

---
layout: two-cols
layoutClass: gap-16
---

# BERTopic: Great Tool, Different Goals

<v-click>

## Why single-level clustering isn't enough

<div class="space-y-6 mt-6">
  <div class="flex items-center space-x-4">
    <div class="w-4 h-4 bg-red-400 rounded-full flex-shrink-0"></div>
    <span class="text-lg">Single granularity misses broader patterns</span>
  </div>
  <div class="flex items-center space-x-4">
    <div class="w-4 h-4 bg-orange-400 rounded-full flex-shrink-0"></div>
    <span class="text-lg">Can't navigate from high-level to specific needs</span>
  </div>
  <div class="flex items-center space-x-4">
    <div class="w-4 h-4 bg-yellow-400 rounded-full flex-shrink-0"></div>
    <span class="text-lg">Explanation comes after, not during clustering</span>
  </div>
</div>

</v-click>

::right::

<v-click>

<div class="flex items-center justify-center h-full">
  <img src="/bertopic_clusters.png" alt="BERTopic clusters visualization" class="max-w-full max-h-80 rounded-lg shadow-lg" />
  <div class="absolute bottom-4 text-center w-full">
    <div class="text-sm text-gray-600">Can we do better?</div>
  </div>
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
- BERTopic is genuinely excellent for academic research, document analysis, and many text mining tasks
- The limitation for LLM conversation analysis is the single-level clustering approach
- Example: You might get 50 clusters about "programming help" but miss that they're all capability gaps
- Can't see the forest for the trees - miss strategic patterns like "users need more integrations"
- Hierarchical clustering lets you zoom out to see capability vs inventory patterns
- LLM-first approach means explanations are built into the process, not retrofitted
- Sets up Kura's approach: understand semantically, then organize hierarchically
-->
