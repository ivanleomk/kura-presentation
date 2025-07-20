Rules

- Make sure to have one clear idea per slide
- AT most 3 bullet points per slide
- Use consistent two-column layout for detailed slides

Slide Format Guidelines

**Standard Slide Structure:**
```
---
layout: two-cols
layoutClass: gap-16
---

# Title with Gradient Styling

<v-click>

## Descriptive subtitle

<div class="space-y-6 mt-6">
  <div class="flex items-center space-x-4">
    <div class="w-4 h-4 bg-[color] rounded-full flex-shrink-0"></div>
    <span class="text-lg">Bullet point text</span>
  </div>
  <!-- Repeat for up to 3 points -->
</div>

</v-click>

::right::

<v-click>

<div class="flex items-center justify-center h-full">
  <div class="text-center">
    <div class="text-6xl mb-4">[emoji or graphic]</div>
    <div class="text-2xl font-bold text-gray-700 mb-2">Key Concept</div>
    <div class="text-gray-500">Supporting description</div>
  </div>
</div>

</v-click>

<style>
h1 {
  background: linear-gradient(45deg, [color1] 10%, [color2] 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>
```

**Color Scheme:**
- Always use red/orange theme: `#ef4444 10%, #f97316 20%` 
- Bullet colors: red (#ef4444), orange (#f97316), yellow (#eab308)
- Keep consistent red/orange gradient styling across all slides

**Visual Elements:**
- Use emojis or simple graphics on the right side
- Keep bullet points concise (one line each)
- Use v-click for progressive disclosure
- Maintain consistent spacing and typography
