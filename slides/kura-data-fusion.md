---
layout: two-cols
layoutClass: gap-16
---

# Enhanced Pattern Discovery

<v-click>

## Clusters + Feedback + Metadata = Actionable Insights

<div class="space-y-6 mt-6">
  <div class="flex items-center space-x-4">
    <div class="w-4 h-4 bg-red-400 rounded-full flex-shrink-0"></div>
    <span class="text-lg">Chat clusters reveal conversation themes</span>
  </div>
  <div class="flex items-center space-x-4">
    <div class="w-4 h-4 bg-orange-400 rounded-full flex-shrink-0"></div>
    <span class="text-lg">User feedback shows satisfaction levels</span>
  </div>
  <div class="flex items-center space-x-4">
    <div class="w-4 h-4 bg-yellow-400 rounded-full flex-shrink-0"></div>
    <span class="text-lg">Metadata enables smart prioritization</span>
  </div>
</div>

</v-click>

::right::

<v-click>

<div class="flex items-center justify-center h-full">
  <div class="w-full">

```sql
-- Cluster insights with user feedback
SELECT 
    cluster_id,
    cluster_name,
    COUNT(*) as conversations,
    AVG(thumbs_up) as avg_satisfaction,
    SUM(revenue_impact) as total_revenue_impact
FROM chat_clusters c
JOIN user_feedback f ON c.conversation_id = f.conversation_id
JOIN user_metadata u ON c.user_id = u.user_id
GROUP BY cluster_id, cluster_name
ORDER BY total_revenue_impact DESC;

-- Results:
-- API Issues     | 156 | 0.27 | $2.3M
-- Bulk Export    | 89  | 0.85 | $500K
-- UI Feedback    | 203 | 0.64 | $200K
```

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
