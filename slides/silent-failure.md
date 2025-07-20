---
layout: center
class: text-center
---

# Yesterday, 1,000 Users Couldn't Find Their Contracts

<v-click>

## Today, another 1,000 will fail the same way

<div class="text-xl text-gray-600 mt-8">
  Your logs show <span class="text-green-500 font-bold">"success"</span> but users are <span class="text-red-500 font-bold">quietly leaving</span>
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
This slide opens with a concrete scenario that technical audiences will immediately recognize.

Key talking points:
- This is happening right now in production systems
- Traditional monitoring shows "200 OK" responses
- But users can't actually accomplish their goals
- Unlike traditional software that crashes loudly, LLM apps fail silently
- Users get frustrated and leave without telling you why
- Your error logs are clean but your user satisfaction is declining
- This is the core problem: silent degradation that's invisible to traditional monitoring
- Sets up the need for new approaches to understand what's really happening
-->
