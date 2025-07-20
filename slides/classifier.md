---
layout: two-cols
layoutClass: gap-16
---

# Why Explicit Classifiers?

<v-click>

## Topic modeling is inherently lossy

<div class="space-y-6 mt-6">
  <div class="flex items-center space-x-4">
    <div class="w-4 h-4 bg-red-400 rounded-full flex-shrink-0"></div>
    <span class="text-lg">Stochastic algorithms produce different results</span>
  </div>
  <div class="flex items-center space-x-4">
    <div class="w-4 h-4 bg-orange-400 rounded-full flex-shrink-0"></div>
    <span class="text-lg">Production needs consistent categorization</span>
  </div>
  <div class="flex items-center space-x-4">
    <div class="w-4 h-4 bg-yellow-400 rounded-full flex-shrink-0"></div>
    <span class="text-lg">Explicit classifiers provide reliability</span>
  </div>
</div>

</v-click>

::right::

<v-click>

<div class="flex items-center justify-center h-full">
  <img src="/ci-overlap.png" alt="Classifier overlap visualization" class="max-w-full max-h-80 rounded-lg shadow-lg" />
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

# Bootstrapping Training Data

<v-click>

## Clusters become labeled examples

<div class="space-y-6 mt-6">
  <div class="flex items-center space-x-4">
    <div class="w-4 h-4 bg-red-400 rounded-full flex-shrink-0"></div>
    <span class="text-lg">Clustered conversations are pre-labeled</span>
  </div>
  <div class="flex items-center space-x-4">
    <div class="w-4 h-4 bg-orange-400 rounded-full flex-shrink-0"></div>
    <span class="text-lg">LLMs use few-shot examples for classification</span>
  </div>
  <div class="flex items-center space-x-4">
    <div class="w-4 h-4 bg-yellow-400 rounded-full flex-shrink-0"></div>
    <span class="text-lg">Efficiently identify data for labeling</span>
  </div>
</div>

</v-click>

::right::

<v-click>

<div class="flex items-center justify-center h-full">
  <div class="text-center">
    <div class="text-2xl font-bold text-gray-700 mb-4">Discovery → Production</div>
    <div class="text-gray-500 mb-6">Topic modeling for exploration<br/>Classifiers for monitoring</div>
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
