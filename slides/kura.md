---
layout: center
class: text-center
---

# Your AI Has Thousands of Daily Conversations

<v-click>

## But do you know what users actually need?

<div class="text-xl text-gray-600 mt-8">
  Kura reveals hidden patterns in chat data through a 5-step pipeline
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

# The Kura Pipeline

<v-click>

## 5 Steps from Chaos to Clarity

<div class="space-y-6 mt-6">
  <div class="flex items-center space-x-4">
    <div class="w-4 h-4 bg-red-400 rounded-full flex-shrink-0"></div>
    <span class="text-lg">Load & summarize conversations</span>
  </div>
  <div class="flex items-center space-x-4">
    <div class="w-4 h-4 bg-orange-400 rounded-full flex-shrink-0"></div>
    <span class="text-lg">Cluster by semantic similarity</span>
  </div>
  <div class="flex items-center space-x-4">
    <div class="w-4 h-4 bg-yellow-400 rounded-full flex-shrink-0"></div>
    <span class="text-lg">Visualize in 2D space</span>
  </div>
</div>

</v-click>

::right::

<v-click>

<div class="flex items-center justify-center h-full">
  <div class="w-full">

```python
# Complete Pipeline Overview
async def main():
    # 1. Load conversations
    conversations = Conversation.from_hf_dataset(
        "ivanleomk/synthetic-gemini-conversations"
    )
    
    # 2. Summarize conversations
    summaries = await summarise_conversations(conversations)
    
    # 3. Generate base clusters
    clusters = await generate_base_clusters_from_conversation_summaries(summaries)
    
    # 4. Create meta clusters
    reduced_clusters = await reduce_clusters_from_base_clusters(clusters)
    
    # 5. Project to 2D and visualize
    projected = await reduce_dimensionality_from_clusters(reduced_clusters)
    visualise_pipeline_results(projected)
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

---
layout: two-cols
layoutClass: gap-16
---

# Step 1: Load & Summarize

<v-click>

## Transform Raw Conversations

<div class="space-y-6 mt-6">
  <div class="flex items-center space-x-4">
    <div class="w-4 h-4 bg-red-400 rounded-full flex-shrink-0"></div>
    <span class="text-lg">Load from Hugging Face datasets</span>
  </div>
  <div class="flex items-center space-x-4">
    <div class="w-4 h-4 bg-orange-400 rounded-full flex-shrink-0"></div>
    <span class="text-lg">Custom prompts for summarization</span>
  </div>
  <div class="flex items-center space-x-4">
    <div class="w-4 h-4 bg-yellow-400 rounded-full flex-shrink-0"></div>
    <span class="text-lg">Disk caching for efficiency</span>
  </div>
</div>

</v-click>

::right::

<v-click>

<div class="flex items-center justify-center h-full">
  <div class="w-full">

```python
# Setup models with caching
summary_model = SummaryModel(
    console=console,
    cache=DiskCacheStrategy(cache_dir="./.summary")
)

checkpoint_manager = JSONLCheckpointManager(
    "./checkpoints", enabled=True
)

# Load conversations
conversations = Conversation.from_hf_dataset(
    "ivanleomk/synthetic-gemini-conversations", 
    split="train"
)

# Generate summaries with custom prompts
summaries = await summarise_conversations(
    conversations, 
    model=summary_model, 
    checkpoint_manager=checkpoint_manager
)
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

---
layout: two-cols
layoutClass: gap-16
---

# Step 2: Base Clustering

<v-click>

## Group by Semantic Similarity

<div class="space-y-6 mt-6">
  <div class="flex items-center space-x-4">
    <div class="w-4 h-4 bg-red-400 rounded-full flex-shrink-0"></div>
    <span class="text-lg">Embeddings capture meaning</span>
  </div>
  <div class="flex items-center space-x-4">
    <div class="w-4 h-4 bg-orange-400 rounded-full flex-shrink-0"></div>
    <span class="text-lg">K-means clustering by default</span>
  </div>
  <div class="flex items-center space-x-4">
    <div class="w-4 h-4 bg-yellow-400 rounded-full flex-shrink-0"></div>
    <span class="text-lg">Auto-generated cluster descriptions</span>
  </div>
</div>

</v-click>

::right::

<v-click>

<div class="flex items-center justify-center h-full">
  <div class="w-full">

```python
# Setup clustering model
cluster_model = ClusterDescriptionModel(
    console=console  # Uses K-means by default
)

# Generate base clusters with titles and descriptions
clusters = await generate_base_clusters_from_conversation_summaries(
    summaries, 
    model=cluster_model, 
    checkpoint_manager=checkpoint_manager
)

# Each cluster gets:
# - Semantic grouping based on embeddings
# - Descriptive title (e.g., "API Integration Issues")
# - Detailed description of common patterns
# - List of conversation summaries in cluster
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

---
layout: two-cols
layoutClass: gap-16
---

# Step 3: Meta Clustering

<v-click>

## Cluster the Clusters

<div class="space-y-6 mt-6">
  <div class="flex items-center space-x-4">
    <div class="w-4 h-4 bg-red-400 rounded-full flex-shrink-0"></div>
    <span class="text-lg">Reduce cluster count hierarchically</span>
  </div>
  <div class="flex items-center space-x-4">
    <div class="w-4 h-4 bg-orange-400 rounded-full flex-shrink-0"></div>
    <span class="text-lg">Find higher-level patterns</span>
  </div>
  <div class="flex items-center space-x-4">
    <div class="w-4 h-4 bg-yellow-400 rounded-full flex-shrink-0"></div>
    <span class="text-lg">Maintain meaningful granularity</span>
  </div>
</div>

</v-click>

::right::

<v-click>

<div class="flex items-center justify-center h-full">
  <div class="w-full">

```python
# Setup meta clustering
meta_cluster_model = MetaClusterModel(console=console)

# Reduce base clusters into meta clusters
reduced_clusters = await reduce_clusters_from_base_clusters(
    clusters, 
    model=meta_cluster_model, 
    checkpoint_manager=checkpoint_manager
)

# Example transformation:
# Base clusters (20):
# - "React Component Errors", "Vue.js Issues", "Angular Problems"
# - "API Rate Limiting", "Authentication Failures", "CORS Issues"
# 
# Meta clusters (5):
# - "Frontend Framework Issues" 
# - "API Integration Problems"
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

---
layout: two-cols
layoutClass: gap-16
---

# Step 4: Dimensionality Reduction

<v-click>

## Project to 2D Space

<div class="space-y-6 mt-6">
  <div class="flex items-center space-x-4">
    <div class="w-4 h-4 bg-red-400 rounded-full flex-shrink-0"></div>
    <span class="text-lg">HDBSCAN + UMAP algorithms</span>
  </div>
  <div class="flex items-center space-x-4">
    <div class="w-4 h-4 bg-orange-400 rounded-full flex-shrink-0"></div>
    <span class="text-lg">Preserve cluster relationships</span>
  </div>
  <div class="flex items-center space-x-4">
    <div class="w-4 h-4 bg-yellow-400 rounded-full flex-shrink-0"></div>
    <span class="text-lg">Enable interactive visualization</span>
  </div>
</div>

</v-click>

::right::

<v-click>

<div class="flex items-center justify-center h-full">
  <div class="w-full">

```python
# Setup dimensionality reduction
dimensionality_model = HDBUMAP()

# Project clusters into 2D space
projected_clusters = await reduce_dimensionality_from_clusters(
    reduced_clusters,
    model=dimensionality_model,
    checkpoint_manager=checkpoint_manager,
)

# High-dimensional embeddings → 2D coordinates
# Similar clusters appear close together
# Cluster density reflects conversation volume
# Interactive exploration of patterns
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

---
layout: two-cols
layoutClass: gap-16
---

# Step 5: Visualization

<v-click>

## Interactive Pattern Discovery

<div class="space-y-6 mt-6">
  <div class="flex items-center space-x-4">
    <div class="w-4 h-4 bg-red-400 rounded-full flex-shrink-0"></div>
    <span class="text-lg">2D scatter plot of clusters</span>
  </div>
  <div class="flex items-center space-x-4">
    <div class="w-4 h-4 bg-orange-400 rounded-full flex-shrink-0"></div>
    <span class="text-lg">Click to explore conversations</span>
  </div>
  <div class="flex items-center space-x-4">
    <div class="w-4 h-4 bg-yellow-400 rounded-full flex-shrink-0"></div>
    <span class="text-lg">Identify patterns and gaps</span>
  </div>
</div>

</v-click>

::right::

<v-click>

<div class="flex items-center justify-center h-full">
  <div class="w-full">

```python
# Generate final visualization
visualise_pipeline_results(
    projected_clusters, 
    style="basic"
)

# Creates interactive plot showing:
# - Each cluster as a point in 2D space
# - Cluster size proportional to conversation count
# - Hover for cluster descriptions
# - Click to drill down into conversations
# - Identify user pain points and opportunities
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

---
layout: two-cols
layoutClass: gap-16
---

# Expected Output

<v-click>

## Hierarchical Conversation Insights

<div class="space-y-6 mt-6">
  <div class="flex items-center space-x-4">
    <div class="w-4 h-4 bg-red-400 rounded-full flex-shrink-0"></div>
    <span class="text-lg">Clear hierarchical structure</span>
  </div>
  <div class="flex items-center space-x-4">
    <div class="w-4 h-4 bg-orange-400 rounded-full flex-shrink-0"></div>
    <span class="text-lg">10x performance with caching</span>
  </div>
  <div class="flex items-center space-x-4">
    <div class="w-4 h-4 bg-yellow-400 rounded-full flex-shrink-0"></div>
    <span class="text-lg">Actionable conversation patterns</span>
  </div>
</div>

</v-click>

::right::

<v-click>

<div class="flex items-center justify-center h-full">
  <div class="w-full">

```
Programming Assistance (190 conversations)
├── Data Analysis (38 conversations)
│   ├── "R plots for statistics"
│   ├── "Tableau performance"
│   └── "Excel to pandas"
├── Web Development (45 conversations)
│   ├── "React re-rendering"
│   ├── "Stripe API integration"
│   └── "CSS grid responsive"
└── ... (more clusters)

Performance: 21.9s → 2.1s (10x faster!)
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
